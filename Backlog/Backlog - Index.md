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
- **BL-0002** - [x] **Decide: language polyglot baseline (T-Q2).**
  Confirmed: C# core + GDScript glue + C/C++/Rust reserved
  + Python tooling. → *Tech and Engine* §2.
- **BL-0003** - [x] **Decide: data-layer hybrid stack (T-Q3).**
  Confirmed: JSON/YAML source → SQLite runtime → in-memory +
  graph projection. → *Tech and Engine* §3.
- **BL-0004** - [x] **Decide: source format (T-Q15).** Hybrid:
  Markdown+YAML-frontmatter (prose) + pure YAML (stats).
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
- **BL-0016** - [x] **Decide: V-Q10-followup** — Sarenrae's chapel
  in Falcon's Hollow.
- **BL-0017** - [x] **Decide: V-Q2-followup** — effectively unclassed
  (hidden + emergent). → *Vision* §4.3.1.
- **BL-0018** - [ ] **Decide: V-Q3-followup + V-Q3-mechanism** —
  source world and transport mechanism. **Currently deferred**
  (both "unspecified/unknown") — task remains open as a back-pocket
  decision when the relevant arc surfaces.
- **BL-0019** - [ ] **Decide: V-Q7-followup** — meaning of tattoo
  `08`. **Currently deferred to play-discovery.** Task remains open.
- **BL-0020** - [ ] **Design: Gherman canonical face concept art**
  — locked to **after BL-0001** cel-shader spike. Blocks-on: BL-0001.
- **BL-0021** - [x] **Design: Gherman voice profile — V-Q8-followup**
  — synthetic-from-prompts confirmed. Implementation still pending
  T-Q9 TTS toolchain choice (split off as BL-0021a).
- **BL-0021a** - [ ] **Decide: T-Q9** — TTS toolchain choice (cloud /
  local / hybrid; specific tool: ElevenLabs / XTTS-v2 / Bark / RVC /
  OpenVoice / mix). → *Audio* AU-Q16, *Tech and Engine* §7.
- **BL-0022** - [ ] **Anime story basis: per-domain conventions
  pass.** Visit *Art and Presentation*, *Animation Pipeline*,
  *Camera and Cinematography*, *Dialogue and Conversation*,
  *Audio*, *NPCs and Companions* and add anime-conventions
  guidance sections (per *Vision* §7). **Elevated priority** since
  anime focus is now main project intent.
- **BL-0023** - [ ] **Decide: V-Q11 (re-posed)** — scene / clip /
  storyboard export tooling commitment. **Promoted from "deferred"
  to "likely-needed"** per *Vision* §7 elevation.
- **BL-0024** - [x] **Decide: V-Q12** — no archetype, surface-level
  only.
- **BL-0025** - [x] **Decide: V-Q13** — looks human, modern outfit,
  pervasive "wrongness." → *Vision* §4.4.
- **BL-0026** - [ ] **Lore: Falcon's Hollow / Darkmoon Vale**
  reference research — pull canonical material (settlement, NPCs,
  Sitting Duck, Sarenrae chapel, Lumber Consortium, Foam River).
  Decide reworks per *Lore Reworks* protocol when imported.
  **Newly load-bearing** since BL-0016 confirmed Sarenrae's chapel
  as the opening location.

## Tasks added this turn (Apr-Sep)

- **BL-0027** - [ ] **Anime / manga / light-novel inspirations
  list (V-Q14).** User to enumerate "tons of inspirations." Each
  reference becomes a tonal-vocabulary entry citable from relevant
  docs. → *Vision* §7.
- **BL-0028** - [ ] **Decide: V-Q15** — cinematic density budget
  (one-per-quest-beat / BG3-frequent / episode-set-piece / scaled).
- **BL-0029** - [ ] **Decide: V-Q16** — "wrongness" mechanism
  (smell / aura / mannerisms / divinatory / deity-detectable /
  pure narrative).
- **BL-0030** - [ ] **Build: anime-archetype-FREE writing
  guidance** — per V-Q12 resolution, document the "no archetype"
  writing rule as a guidance section in *Romance and Relationships*,
  *NPCs and Companions*, and *Dialogue and Conversation*.
- **BL-0031** - [ ] **Build: "wrongness" mechanic shell** —
  per *Vision* §4.4, define the tracking fields on Gherman
  (visible-anachronism flag, modern-outfit equipped, perceptibility
  modifiers) and how NPC reactions consult them.
- **BL-0032** - [ ] **Build: session-start ritual prompt**
  per *Workflow* §11. Optional: a session-start template the
  assistant follows automatically.
- **BL-0033** - [ ] **Decide: T-Q5** — plugin folder layout
  + manifest format (now that MD-Q1 = TOML).
- **BL-0034** - [ ] **Decide: SP-Q2 / SP-Q3** — auto-save cadence
  details + history semantics (log preserved across loads vs
  classical undo). → *Save and Persistence*.
- **BL-0035** - [ ] **Decide: NPC-Q1** — memory model (perfect /
  decaying / summary / hybrid / salience-graph).
- **BL-0036** - [ ] **Decide: WS-Q2** — off-screen NPC simulation
  depth (full vs summarized-and-reconstructed).
- **BL-0037** - [ ] **Lore: enumerate all canonical Golarion
  deities** with "rational/empirical" rework framings per LR-003.
- **BL-0038** - [ ] **Lore: cosmology / planar structure rework
  proposal** per LR-004 (LR-Q5–LR-Q8).
- **BL-0039** - [ ] **Backfill: italics + first-mention links
  pass** across existing docs per IDX-Q2 resolution.
- **BL-0040** - [ ] **Re-pose: BI-Q1 and RD-Q1** — user asked
  "What?" — assistant to re-explain in clearer terms (handled
  in next-turn response).

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
