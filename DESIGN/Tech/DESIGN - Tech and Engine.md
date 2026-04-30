# DESIGN — Tech and Engine

> Living document. Captures engine choice, language strategy, data layer,
> AI/LLM dev-time tooling, platform target, plugin system stance, and
> licensing posture. Heavy on options still pending the user's decisions.

> **Workflow note:** per *Workflow*, no choice in this doc is finalized
> until the user explicitly approves it. Where the user wrote "best for
> the project" or "best of all worlds," this doc lays out options and
> a recommended blueprint, but does **not** treat any option as default-
> decided.

---

## 1. Engine (resolved T-Q1)

> **Godot 4 (latest stable).** Confirmed.

### 1.1 Immediate consequences

- Build, prototype, and ship target is **Godot 4.x** — the latest
  stable release at decision time, with rolling upgrades as new
  stable releases land.
- **Anime/cel-shader spike scheduled** as a top backlog item: 1–2
  weeks of focused shader work to validate that the *Art and
  Presentation* §1.1 three-way blend (Genshin ramp + HSR warmth +
  Hades silhouette) is achievable in Godot 4. This is the largest
  unknown-unknown for the engine choice.
- **C# support** in Godot 4 is the assumed scripting baseline (per
  the polyglot proposal in §2, pending T-Q2 confirmation).
- **Plugin / mod system** uses Godot's native `addons` + `.pck`
  loading conventions (per T-Q5 proposal, pending confirmation).
- **Render pipeline**: Forward+ for our target hardware (per T-Q4,
  Windows-only, pending hardware-floor confirmation).

### 1.2 Reference table (kept for record)

| Aspect | Godot 4 | Unity 6 |
|---|---|---|
| License | MIT (free, no royalty, no telemetry) | Proprietary, EULA changes possible |
| NSFW posture | No content policy on the engine | No content policy, but Asset Store ToS restrict |
| Cel-shading prior art | Growing, less mature than Unity | Very mature (UTS2, Synty, etc.) |
| 3D production tooling | Improving but behind Unity | Mature (Animation Rigging, Cinemachine, Timeline) |
| Scripting languages | GDScript, C#, GDExtension (C++/Rust/Swift/...) | C#, IL2CPP |
| Plugin / mod system | First-class via `.pck`, addons, GDExtension | Mature but more friction |
| Iteration speed | Very fast (lightweight, instant reloads) | Slower domain reload, but improving |
| First-person FPS-grade rendering | Capable, less optimized | Highly optimized |
| Anime PBR / cel-shaders | Custom shaders required; community packs exist | UTS2 / Synty / many off-the-shelf |
| Build target | Windows native, single binary | Windows native |
| File size of project | Tiny | Heavier (Library/, Temp/, etc.) |
| Fit for "forever project" + solo | Excellent (tight, free, portable) | Acceptable (vendor risk) |

**Recommendation (pending approval):** Godot 4 (latest stable), with the
caveat that the **anime/cel-shader stack** will require custom shader
work or a community pack — this is the largest "what could surprise us"
risk vs Unity. Worth a 1–2 week shader spike before committing.

→ See **T-Q1** below.

## 2. Language Strategy

User direction: *"Best language and most-adapted to project."*

Languages available inside Godot 4:

| Lang | Strengths | Weaknesses |
|---|---|---|
| **GDScript** | Native, instant reload, minimal boilerplate, tight engine integration, good for UI and gameplay glue | Dynamic typing (optional static), slower for heavy compute, smaller ecosystem |
| **C# (Mono / .NET)** | Statically typed, fast, huge ecosystem (NuGet), modern language features, great IDE | Slightly heavier reload cycle, larger build, requires .NET runtime |
| **C++ (GDExtension)** | Maximum performance, full Godot API, integrates with native libs | Slow iteration, more friction, more bugs |
| **Rust (godot-rust)** | Safety + performance, modern, growing ecosystem | Smaller community in Godot, GDExtension still maturing |

**Polyglot proposal (pending approval):**

| Layer | Recommended language |
|---|---|
| **Rules engine** (PF2e math, conditions, effects, dice, turn translation) | **C#** — typed, testable, ecosystem |
| **Game systems** (quests, factions, NPCs, schedules, economy) | **C#** |
| **Gameplay glue and UI scripting** | **GDScript** |
| **Hot-path simulation** (world tick, NPC scheduling for thousands of NPCs, pathing, perception broadcasting) | **C++ or Rust via GDExtension**, only if profiling demands |
| **Content conversion / data pipeline tooling** (Pathfinder source → game data) | **Python** (off-engine; rich ecosystem for parsing, regex, scraping, LLM tooling) |
| **Build / scripting / CI** | **Python** + a small Bash/PowerShell layer |

Rationale: C# is the load-bearing core because the rules engine, NPC
behavior trees, and economy/quest systems will be the most-touched code
in the project. GDScript stays for things where iteration speed matters
more than rigor. C++/Rust stays in reserve for measured bottlenecks
only — premature performance work is a known trap.

→ See **T-Q2**.

## 3. Data Layer

User direction: *"Best-of-all-world for the data layer given the
enormous scope."*

The Pathfinder content surface is enormous: every spell, feat, ancestry,
class, archetype, item, monster, deity, location, NPC, AP encounter,
society scenario, etc., from PF1e + PF2e + Remaster + third-party,
plus all our original content. This is hundreds of thousands of records.

**Recommended hybrid stack (pending approval):**

```
                    ┌────────────────────────┐
                    │  SOURCE (text/JSON)    │   ← human-edited,
                    │  in repo, per-extract  │     git-versioned,
                    │  YAML or JSON          │     modder-friendly
                    └────────────┬───────────┘
                                 │  build pipeline
                                 ▼
                    ┌────────────────────────┐
                    │  CANONICAL JSON        │   ← Remaster-shaped,
                    │  validated, schemed    │     single normalization
                    └────────────┬───────────┘
                                 │
                                 ▼
                    ┌────────────────────────┐
                    │  RUNTIME DB (SQLite)   │   ← indexed for queries
                    │  read-mostly           │     ("all spells of trait
                    └────────────┬───────────┘     fire ≤ rank 5")
                                 │
                                 ▼
                    ┌────────────────────────┐
                    │  IN-MEMORY HOT CACHE   │   ← gameplay reads
                    │  (game-side structs)   │
                    └────────────┬───────────┘
                                 │
                    ┌────────────▼────────────┐
                    │  GRAPH PROJECTION       │   ← faction graphs,
                    │  (in-memory, derived)   │     lore links, NPC
                    └─────────────────────────┘     relationships
```

**Save data** lives in a separate per-save SQLite (or LMDB) database,
schema-versioned so save migrations are tractable.

**Why this shape:**
- **JSON/YAML source-of-truth in git** = perfect history of every
  conversion decision, diffable, modder-friendly, supports the
  extract-by-extract import workflow.
- **SQLite runtime** = indexed queries are fast, single-file, no
  daemon, ACID, well-known.
- **In-memory cache** = gameplay never queries SQL; tables of
  records loaded once at boot.
- **Graph projection** = faction relationships, lore links, NPC
  affinities, and the simulation graph need traversal queries that
  are awkward in SQL.

→ See **T-Q3**.

## 4. Licensing / Distribution / Censoring

User direction:

- **Personal project. No redistribution.**
- **No copyright concerns.** Free use of community datasets (Archives
  of Nethys, Foundry `pf2e` system data, third-party SRDs, scraped
  rulebook content).
- **No license concerns.** Free use of AI models regardless of stated
  license or usage policy, at dev-time.
- **No censoring concerns** at any layer.

The single hard line remains the *NSFW* doc's Section 6 (no explicit
sexual content involving minors). Beyond that, no constraints.

This dramatically simplifies the toolchain: we can use the best tool
for each job without licensing detours, and we can use uncensored
local models freely.

## 5. Platform Target

**Windows-only.**

Implications:
- Build, test, and ship matrix is single-platform — drastically
  reduces project complexity.
- Native Windows APIs (DirectX 12, WASAPI, etc.) are fair game.
- We don't need to worry about Linux/Mac/Steam-Deck/console
  compatibility unless the user re-scopes.
- Path separators, case sensitivity, and locale assumptions can be
  Windows-shaped throughout.

→ See **T-Q4** for Windows-version baseline.

## 6. Solo Dev + Plugin System

User direction: *Solo dev with the assistant. A first-class plugin
system would benefit the project given its scope.*

**Plugin system rationale:** even though there are no external
modders, the project's own content is so vast that **treating our
own content as plugins** keeps the codebase modular. Each AP, each
faction, each piece of original content can live in its own plugin
folder; the engine loads them at startup.

**Proposed plugin shape (pending approval):**

```
PathSeeker/
├── Engine/         # core game code (engine + rules + systems)
├── Content/
│   ├── Core/       # Player Core / GM Core / Monster Core
│   ├── APs/
│   │   ├── Rise of the Runelords/
│   │   ├── Curse of the Crimson Throne/
│   │   ├── ...
│   ├── Society/
│   ├── Modules/
│   ├── Third-Party/
│   ├── Lore Reworks/
│   └── Original/
├── Plugins/        # optional modules (e.g., NSFW expansions, mood packs)
├── Tools/          # build/conversion tools
├── Tests/
└── DESIGN/
```

Each leaf folder is a self-contained plugin: data, scripts, assets,
manifest. The engine discovers them at boot.

→ See **T-Q5**.

## 7. AI / LLM at Dev-Time

User direction:
- **LLM-driven content is dev-time only.** (Possible runtime caveat
  later; flagged as a future consideration.)
- **All content generation uses AI under the user's supervision;
  nothing ships without explicit approval.**
- **A mix of generation modalities at dev-time** (text, image, audio,
  voice, possibly 3D).

**Implied dev-time stack (pending approval):**

| Modality | Candidate tools |
|---|---|
| **Text / dialogue / lore generation** | Local LLMs (Llama 3.x, Mistral Large, Mixtral, Qwen, DeepSeek, command-R, behemoth-tier models for taste); cloud LLMs where they don't refuse content |
| **Image (concept art, portraits, NSFW reference)** | Stable Diffusion XL, Pony Diffusion, Illustrious, NoobAI, ControlNet, ComfyUI pipelines |
| **Character 3D (sculpts, body templates)** | Koikatsu / HoneySelect 2 export pipelines; CharacterCreator; Daz; Stable Diffusion + photogrammetry; eventually custom |
| **Animation** | Mixamo, retargeted to our rig; Cascadeur; AI motion-capture (RADiCAL, etc.); hand-keyed in Blender |
| **Voice / TTS** | ElevenLabs (cloud, high quality); XTTS-v2 (local, voice cloning); Bark; RVC for voice conversion; possibly OpenVoice |
| **Audio / SFX / music** | Stable Audio, Suno, Udio, MusicGen, hand-composed where needed |
| **Code assistance** | This Claude session; local code models for offline work |

All generation is **dev-time**, **supervised**, and **approved before
shipment** — runtime stays deterministic. The runtime distribution
contains only pre-baked assets and pre-written content.

**Possible runtime LLM caveat (deferred):** the user may later allow
runtime LLM generation for some content (NPC barks, ambient dialogue,
procedural quests, scene composition). This would add an entire
runtime-LLM subsystem (local model, GPU budget, prompt caching,
content filter) — out of scope until explicitly requested.

→ See **T-Q6 through T-Q12** for specific AI-stack decisions.

## 8. Speculative / Throwaway Code

User direction: *Throwaway prototypes are fine, but must be removed
once real code is written and shipped.*

Proposed convention:
- Throwaway code lives in `Tools/Spikes/<topic>/` or, when bigger,
  in branch `spike/<topic>` not merged to main.
- Every spike has a `SPIKE.md` describing the question it answers
  and the disposition (kept / archived / deleted).
- A `BACKLOG` entry is created the moment a spike survives long
  enough to risk forgetting to remove it.

→ See **T-Q13**.

## 9. Cross-References

- *Vision* — forever-project bias toward modular foundations.
- *Workflow* — mandatory Q&A loop (especially for content extracts).
- *Rules and Edition* — content surface that drives the data layer.
- *NSFW* — drives generation pipeline including age-verification
  filter (N-Q13).
- *Art and Presentation* — render stack constrains engine choice.

## 10. Open Questions (Tech-Local)

- ~~T-Q1.~~ **Resolved.** Godot 4 (latest stable). See §1.
- **T-Q2.** Language polyglot: confirm proposal in §2 (C# core +
  GDScript glue + C++/Rust reserved + Python tooling) or pick a
  single-language stance (e.g., all-C# / all-GDScript).
- **T-Q3.** Data layer: confirm hybrid stack in §3 (JSON source →
  SQLite runtime → in-memory + graph projection) or specify another
  shape (pure SQLite, pure JSON, document store, custom binary).
- **T-Q4.** Windows version baseline (10? 11?) and minimum hardware
  target.
- **T-Q5.** Plugin system: confirm folder layout in §6 or specify
  another shape; first-class plugin manifest format (TOML, JSON,
  YAML, custom).
- **T-Q6.** Local LLM stack: which inference backend (llama.cpp,
  vLLM, koboldcpp, Ollama, ExLlamaV2, custom)?
- **T-Q7.** Local LLM model lineup: which models for narrative /
  rules-conversion / NSFW? (e.g., Llama 3.3 / Behemoth / Mixtral /
  Qwen-2.5 / DeepSeek-v3.)
- **T-Q8.** Image-gen stack: ComfyUI workflows hand-built, or use
  prebuilt UI like Forge, A1111, InvokeAI? Image checkpoints
  (PonyXL, Illustrious, NoobAI, custom merges)?
- **T-Q9.** TTS: which exact tool(s) get the budget? Cloud-only
  (ElevenLabs) vs local-only (XTTS) vs hybrid?
- **T-Q10.** Voice cloning sources: how do we acquire voices? (Public
  domain, paid services, custom samples, AI-synthetic-from-scratch?)
- **T-Q11.** 3D character pipeline: build on Koikatsu/HoneySelect/
  CharacterCreator/Daz exports, or build a fully custom rig from
  day one?
- **T-Q12.** Repo strategy for generated assets: where do they live?
  (Git-LFS in main repo, separate assets repo, external store with
  manifest references)? — important for repo size as the project
  grows.
- **T-Q13.** Spike lifecycle policy: time-box and removal rules
  (e.g., spike older than 30 days must be either promoted to real
  code or deleted)?
- **T-Q14.** Test strategy: do we want unit tests on the rules
  engine specifically (high ROI given PF2e math), and integration
  tests for content pipeline?
- **T-Q15.** Content-pipeline format choice: YAML vs JSON vs TOML
  vs Markdown-with-frontmatter for source files (the things you'll
  edit by hand and that I'll write during extract-by-extract import).
- **T-Q16.** "Future runtime LLM" — do you want me to keep that door
  open by sketching an interface now, or genuinely defer until later?
- **T-Q17.** Source-control branching: do we work on `main` directly,
  or feature branches with regular merges? (Currently on
  `claude/pathfinder-game-design-hhWTr`.)
