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
- **BL-0016** - [x] **Decide: V-Q10-followup** — RETCONNED.
  Originally Sarenrae's chapel; re-resolved this turn to **Church
  of Iomedae (Falcon's Hollow)** per
  `module:hlh:01-adventure-background` D-004.
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
- **BL-0023** - [x] **Decide: V-Q11** — scene/clip/storyboard
  export tooling. Resolved: **Yes**, multiple exporters in scope
  (screenshot, clip, panel, episode), sequencing pending
  V-Q11-followup. Spawns BL-0023a.
- **BL-0023a** - [x] **Decide: V-Q11-followup** — resolved:
  **all four exporters built in parallel** (screenshot, clip,
  panel/storyboard, episode). No sequencing. Spawns BL-0049–0052
  for individual exporter design + build.
- **BL-0024** - [x] **Decide: V-Q12** — no archetype, surface-level
  only.
- **BL-0025** - [x] **Decide: V-Q13** — looks human, modern outfit,
  pervasive "wrongness." → *Vision* §4.4.
- **BL-0026** - [ ] **Lore: Falcon's Hollow / Darkmoon Vale**
  reference research — pull canonical material (settlement, NPCs,
  Lumber Consortium, Foam River). **Partially advanced this turn**
  via the HLH adventure-background extract (5 lore stubs created:
  Falcon's Hollow, Blackscour, Laurel, Constabulary, Church of
  Iomedae FH chapter). Remaining work: full settlement profile,
  remaining NPCs, Lumber Consortium rework decision (LORE-FH-Q1),
  district map, Sitting Duck inn, etc.

## Tasks added this turn (Apr-Sep)

- **BL-0027** - [x] **Anime / manga / light-novel inspirations
  list (V-Q14).** Initial batch resolved: Hell's Paradise,
  Fate Zero/Stay Night/Heaven's Feel, Bleach, Redo of Healer,
  Demon Slayer, My Dress-Up Darling, Berserk, Goblin Slayer.
  Open-ended for further additions. → *Vision* §7.3.
- **BL-0028** - [x] **Decide: V-Q15** — cinematic density:
  **BG3-frequent and more** (anime-grade upper-bound). Spawns
  BL-0057 for numeric anchor.
- **BL-0029** - [x] **Decide: V-Q16** — two-channel wrongness:
  **Magnetism** (variable pull, especially women, single or
  partnered) + **Aura** (ambiguous good/bad polarity). See
  *Vision* §4.4.1. Spawns BL-0058–0061 for implementation work
  and follow-up decisions.
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
- **BL-0033** - [x] **Decide: T-Q5** — plugin folder layout
  per *Content Pipeline* §4 confirmed; manifest format = TOML.
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
- **BL-0040** - [x] **Re-pose: BI-Q1 and RD-Q1** — re-explained
  next turn; both resolved: BI-Q1 = composed subsystems, RD-Q1 =
  mixed patrons / Gherman has none.
- **BL-0041** - [x] **Decide: V-Q17** — Gherman is openly atheist
  (Rahadoumi-style). Implications captured in *Religion and
  Devotion* §3.1.
- **BL-0042** - [ ] **Decide: CP-Q3 implementation** — define the
  YAML decisions-block schema (timestamp, question-ID, answer,
  rationale fields). → *Content Pipeline* §2.2.
- **BL-0043** - [ ] **Build: `Content/Source/_raw/` gitignore
  entry** when the Content/ folder is created.
- **BL-0044** - [x] **Decide: CP-Q1 / T-Q15** — re-confirmed this
  turn (hybrid format).
- **BL-0045** - [x] **Decide: CP-Q3** — inline YAML decisions
  block (Option a).
- **BL-0046** - [x] **Decide: CP-Q5** — paste / file-drop hybrid.
- **BL-0047** - [x] **Decide: BI-Q1** — composed subsystems.
- **BL-0048** - [x] **Decide: RD-Q1** — mixed patron model;
  Gherman has none.
- **BL-0049** - [ ] **Build: in-game screenshot mode** (anime-
  composed pause-and-frame; cel-shaded output). One of four
  parallel exporters per V-Q11-followup. → *Camera and
  Cinematography*, *Tech and Engine*.
- **BL-0050** - [ ] **Build: in-game clip recorder** (record N
  seconds of locked-camera scene; export as video). One of four
  parallel exporters. → *Camera and Cinematography*, *Tech and
  Engine*.
- **BL-0051** - [ ] **Build: storyboard / panel exporter**
  (multi-frame manga-panel layout from a scene with dialogue
  overlay). One of four parallel exporters. → *Camera and
  Cinematography*, *Dialogue and Conversation*.
- **BL-0052** - [ ] **Build: episode exporter** (editor-level
  scene export for splicing into a pre-produced anime episode).
  One of four parallel exporters. Largest-scope; likely depends
  on the other three landing first in some form. → *Camera and
  Cinematography*, *Animation Pipeline*, *Audio*, *Tech and
  Engine*.
- **BL-0053** - [ ] **Decide: RD-Q-followup** (atheist healing
  edge case) — when a Sarenrae cleric attempts to heal an
  unwilling-by-philosophy atheist (Gherman), what happens
  mechanically? RAW *unwilling target* Will save vs partial
  heal? Custom rule? Diegetic friction with no mechanic? →
  *Religion and Devotion* §3.1, *Magic*, *Combat*.
- **BL-0054** - [ ] **Lore: Rahadoum** reference research and
  rework register entry. Pure Legion, Laws of Mortality,
  atheist-society practices. Newly load-bearing per Gherman's
  V-Q17 atheist stance (potential late-game faction destination).
  → *Lore Reworks*.
- **BL-0055** - [ ] **Build: anime-inspirations citation
  convention** — implement the `[insp: <Title>]` shorthand and
  apply it backwards across existing docs where a tonal claim
  could be grounded in one of the V-Q14 inspirations. → *Vision*
  §7.3.
- **BL-0057** - [ ] **Decide: V-Q15-followup** — numeric anchor
  for cinematic density (e.g., 3+ micro-moments per in-game hour,
  1 episode-set-piece per N hours). Drives *Performance Budget*.
- **BL-0058** - [ ] **Build: Magnetism mechanic** — `Magnetism`
  modifier per NPC↔Gherman edge, four-band outcomes (subliminal /
  noticed / infatuation / obsession), per-NPC growth curves,
  decay rules. → *NPCs and Companions* §4.1, *Romance and
  Relationships* §3.1, *NSFW* §5.2.
- **BL-0059** - [ ] **Build: Aura mechanic** — `Aura` read
  polarity per NPC↔Gherman first-contact, modulated by
  detection-trained NPCs, drift over interaction history. →
  *NPCs and Companions* §4.1.
- **BL-0060** - [ ] **Decide: V-Q16-followup-A** — Magnetism scale
  details (band thresholds, growth curves, decay, simultaneous-
  obsession cap).
- **BL-0061** - [ ] **Decide: V-Q16-followup-B** — Magnetism on
  straight-male NPCs (non-sexual admiration channel vs orientation-
  gated).
- **BL-0062** - [ ] **Decide: V-Q16-followup-C** — Aura first-meet
  randomness (RNG / personality-deterministic / hybrid).
- **BL-0063** - [ ] **Decide: V-Q16-followup-D** — Aura player
  visibility (diegetic-only vs surfaced).
- **BL-0064** - [ ] **Magnetism + Consent axis design** — the
  Magnetism is *not* consent-conferring (per *NSFW* §5.2 / *Vision*
  §4.4.1). Define the consent-axis interaction so dub-con / non-con
  scenes triggered by obsession-band NPCs render with full
  mechanical fidelity (transgressive grounding per *Berserk* /
  *Heaven's Feel* / *Redo of Healer* inspirations).

## Tasks added this turn (HLH first-extract import)

- **BL-0065** - [x] **Import: HLH p.3 Adventure Background** —
  source-tier file written at
  `Content/Source/Modules/Hollow's Last Hope/01 - Adventure Background.md`
  with 10 decisions logged (D-001 through D-010).
- **BL-0066** - [x] **Lore stubs created from HLH p.3 import**
  — Falcon's Hollow, Blackscour, Laurel, Constabulary, Church of
  Iomedae (FH chapter). 5 files in `Lore/`.
- **BL-0067** - [ ] **Decide: V-Q18 — Heroes NPC roster** —
  count, identity, composition, introduction timing, Gherman
  default-relationship, mutability. **Single largest pending
  design item** spawned by D-009 secondary-PC directive.
  → *Vision* §4.6, *NPCs and Companions* §2.1.
- **BL-0068** - [ ] **Decide: V-Q19 — Module-PC slot policy** —
  do heroes always fill canonical "PC slots" rigidly, pre-emptively,
  or as role-vacancy?
- **BL-0069** - [ ] **Decide: V-Q20 — Hero permadeath cycling** —
  replace / retire / revive when an MC NPC dies.
- **BL-0070** - [ ] **Resolve deferred D-003** — failed-prayer
  framing for Iomedae's chapter blackscour-cure attempts. Awaits
  full HLH sourcebook injection. Leaning Option C (local-capacity
  + disease-resistance combined).
- **BL-0071** - [ ] **Open follow-ups from new lore stubs** —
  LORE-FH-Q1 (Lumber Consortium rework), LORE-FH-Q3 (Sarenrae
  presence after retcon), LORE-IFH-Q1 (senior cleric identity —
  Hero/MC NPC promotion candidate), LORE-IFH-Q5 (atheism-void +
  Aura ambiguous compound mechanic), LORE-BS-Q1/Q2 (blackscour
  stat block + cure recipe).
- **BL-0072** - [ ] **Workflow / Content Pipeline doc update** —
  fold the secondary-PC directive into *Content Pipeline* §3
  (extract-by-extract import protocol now records *who fills the
  module's "PC" slot* — heroes by default, not Gherman).
- **BL-0056** - [ ] **Per-domain anime-inspirations pass**
  (extension of BL-0022): for each of *Combat*, *Magic*,
  *Animation Pipeline*, *Camera and Cinematography*, *Dialogue
  and Conversation*, *Audio*, *NPCs and Companions*, *NSFW*,
  *Religion and Devotion*, *Death and Afterlife* — add a
  "Tonal Anchors" subsection citing the relevant V-Q14
  inspirations.

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
