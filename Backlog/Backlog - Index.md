# Backlog — Index

> Master index of **actionable tasks only**. No design discussion, no
> rationale debates — those live in `DESIGN/`. This is the to-do list.
>
> **The assistant updates and edits Backlog files autonomously**
> (per *Workflow* §1.1 carve-out). Other folders still require user
> approval per task.

---

## Conventions

- File naming: `Backlog - <Sub>.md`, capitalized, spaces around the dash.
- Each task has:
  - A short ID: `BL-<NNNN>`, monotonically increasing across the corpus
    (global, not per-file).
  - A checkbox: `- [ ]` (open) or `- [x]` (done). **No status tags.**
  - A 1-line title.
  - Optional 1–3 line "definition of done."
  - Optional link(s) to relevant `DESIGN - <Domain>.md` section(s)
    or `Open Questions` IDs that gate it.
- One file per high-level domain: engine, content pipeline, art,
  rules conversion, lore reworks, spikes, etc.
- Files end with a per-file open-questions section (`BL-Q*`).
- The assistant adds, edits, completes, and removes tasks autonomously
  as work proceeds; the user reviews via diffs at commit time.

## Top-Level Files (planned)

| File | Scope |
|---|---|
| `Backlog - Engine.md` | Godot setup, build, platform plumbing |
| `Backlog - Content Pipeline.md` | PF source → game data flow |
| `Backlog - Rules Conversion.md` | PF2e Remaster rule transcription |
| `Backlog - Lore.md` | Lore content writing and reworks |
| `Backlog - Art.md` | Shader, character, environment, animation |
| `Backlog - Audio.md` | Voice, music, sfx |
| `Backlog - Systems.md` | Combat, magic, NPC AI, simulation |
| `Backlog - NSFW.md` | Body, scene, intimate-system tasks |
| `Backlog - Tools.md` | Editor tools, build tools, content tools |
| `Backlog - Spikes.md` | Time-boxed exploratory tasks |
| `Backlog - Decisions Pending.md` | Tasks that require a user decision before they can begin |

## Seed Tasks (this turn — first batch)

The seed tasks below are illustrative and will be split into per-domain
files in a subsequent autonomous Backlog edit.

- **BL-0001** - [ ] **Spike: Godot 4 anime/cel-shader stack
  feasibility.** Validate the *Art and Presentation* §1.1 three-way
  blend (Genshin ramp + HSR warmth + Hades silhouette) is achievable
  in Godot 4 within reasonable shader budget. Time-box: 1–2 weeks.
  Blocks: most rendering decisions. → *Tech and Engine* §1.1, *Art
  and Presentation* §1.1.
- **BL-0002** - [ ] **Decide: language polyglot baseline (T-Q2).**
  Confirm or revise the C# core + GDScript glue + C/C++/Rust reserved
  + Python tooling proposal. → *Tech and Engine* §2.
- **BL-0003** - [ ] **Decide: data-layer hybrid stack (T-Q3).**
  Confirm or revise the JSON source → SQLite runtime → in-memory +
  graph projection proposal. → *Tech and Engine* §3.
- **BL-0004** - [ ] **Decide: source format (T-Q15).** YAML / JSON
  / TOML / Markdown-with-frontmatter for content extracts.
- **BL-0005** - [x] **Decide: Backlog format (W-Q2).** Resolved this
  turn — checkbox style `[ ]`/`[x]`, no status tags, autonomous
  edits.
- **BL-0006** - [ ] **Decide: variant rules baseline (R-Q1).**
  Free Archetype, ABP, PWL, etc.
- **BL-0007** - [ ] **Build: content pipeline skeleton.** YAML/JSON
  source → validator → SQLite builder → engine loader, end-to-end
  smoke test on one trivial spell record. Blocks: all content import.
- **BL-0008** - [ ] **Build: PF2e dice expression evaluator
  (rules engine spike).** Standalone library that parses and rolls
  arbitrary PF2e dice expressions, including conditional bonuses
  and trait-derived modifiers.
- **BL-0009** - [x] **Decide: protagonist V-Q-followups.** Opening
  framing (V-Q3), orientation (V-Q4), aging (V-Q5), language set
  (V-Q6), distinctive marks (V-Q7), voice profile (V-Q8), face
  customization (V-Q9), starting location (V-Q10). All resolved
  this turn except V-Q10-followup (specific Falcon's Hollow room).
- **BL-0010** - [ ] **Decide: NSFW asset-generation filter
  policy confirmation (N-Q13).** Confirm every NSFW generation
  pipeline includes a minor-content filter at gen time.
- **BL-0011** - [ ] **Stand up: testing harness for the rules
  engine.** xUnit / NUnit / Godot test runner; first tests on dice
  evaluator (BL-0008).
- **BL-0012** - [ ] **Decide: repo strategy for generated assets
  (T-Q12).** Git-LFS in main repo / separate assets repo / external
  store with manifest references.
- **BL-0013** - [x] **Decide: DESIGN sub-folder layout (IDX-Q1).**
  Resolved this turn: Option A (6 folders — Foundation, Systems,
  World, People, Tech, Art).
- **BL-0014** - [x] **Reorg: split DESIGN/ into sub-folders**
  per IDX-Q1 resolution. Executed this turn. Index updated.
- **BL-0015** - [ ] **Reorg: split Backlog/ seed tasks into per-domain
  files** once enough tasks accumulate to warrant the split.
- **BL-0016** - [ ] **Decide: V-Q10-followup** — specific Falcon's
  Hollow waking location (inn / tavern / temple / private healer /
  communal hall). → *Vision* §4.2 / §4.3.
- **BL-0017** - [ ] **Decide: V-Q2-followup** — concrete shape of
  Gherman's "flexible class with unique quirks." → *Vision* §4.3.
- **BL-0018** - [ ] **Decide: V-Q3-followup** — isekai source world
  (Golarion plane / Earth / unspecified-late) and transport
  mechanism. → *Vision* §4.2.
- **BL-0019** - [ ] **Decide: V-Q7-followup** — meaning of tattoo
  `08`. Pick now or defer to play. → *Vision* §4.3.
- **BL-0020** - [ ] **Design: Gherman canonical face concept art**
  — V-Q9-followup timing (now vs after BL-0001 cel-shader spike).
- **BL-0021** - [ ] **Design: Gherman voice profile — V-Q8-followup**
  — clone-from-reference vs synthetic-from-prompt; pick a TTS
  pipeline target (after T-Q9). → *Audio*.
- **BL-0022** - [ ] **Anime story basis: per-domain conventions
  pass.** Visit *Art and Presentation*, *Animation Pipeline*,
  *Camera and Cinematography*, *Dialogue and Conversation*,
  *Audio*, *NPCs and Companions* and add anime-conventions
  guidance sections (per *Vision* §7).
- **BL-0023** - [ ] **Decide: V-Q11** — scene / clip / storyboard
  export tooling commitment + fidelity (still / video / panel /
  full storyboard).
- **BL-0024** - [ ] **Decide: V-Q12** — anime-archetype starter
  templates as writing convention vs light garnish.
- **BL-0025** - [ ] **Decide: V-Q13** — is Gherman's isekai-
  outsider status perceptible to NPCs?
- **BL-0026** - [ ] **Lore: Falcon's Hollow / Darkmoon Vale**
  reference research — pull canonical material (settlement, NPCs,
  Sitting Duck, Sarenrae chapel, Lumber Consortium, Foam River).
  Decide reworks per *Lore Reworks* protocol when imported.

## Cross-References

- *DESIGN - Workflow* §1.1 — Backlog autonomy carve-out.
- *DESIGN - Workflow* §7 — spike lifecycle policy.
- *DESIGN - Tech and Engine* — most engine/data-layer tasks live here.
- *DESIGN - Open Questions* — every `Decide:` task references one or
  more open question IDs.

## Open Questions (Backlog-Index-Local)

- ~~BL-Q1.~~ **Resolved.** Format = checkbox `[ ]`/`[x]`, BL-NNNN
  global IDs, autonomous edits. See §Conventions.
- **BL-Q2.** Should the backlog include **priority** tags (P0/P1/
  P2/P3) on individual tasks?
- **BL-Q3.** Should blocked tasks include an explicit `blocks-on:`
  pointer to the resolution dependency, or is the inline cross-
  reference enough?
- **BL-Q4.** Should completed (`[x]`) tasks be archived to a per-file
  `Backlog - <Sub> (Archive).md` after some threshold, or kept
  inline?
- **BL-Q5.** Backlog file split threshold — at what task count does
  a file split into sub-files?
- **BL-Q6.** Should backlog files embed the Open Questions registry
  cross-reference inline (with a current-snapshot list), or rely on
  the user to read both files?
