# Backlog — Index

> Master index of **actionable tasks only**. No design discussion, no
> rationale debates — those live in `DESIGN/`. This is the to-do list.
>
> Format proposal pending **W-Q2**. Below is a starter format used until
> the user confirms or replaces it.

---

## Conventions (Provisional — pending W-Q2)

- File naming: `Backlog - <Sub>.md`, capitalized, spaces around the dash.
- Each task has:
  - A short ID: `BL-<NNNN>`, monotonically increasing across the corpus.
  - A status tag: `[todo] [doing] [blocked] [done]`.
  - A 1-line title.
  - Optional 1–3 line "definition of done."
  - Optional link(s) to relevant `DESIGN - <Domain>.md` section(s)
    or `Open Questions` IDs that gate it.
- One file per high-level domain: engine, content pipeline, art,
  rules conversion, lore reworks, spikes, etc.
- Files end with a per-file open-questions section (`BL-Q*`).

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
files once W-Q2 confirms the format.

- **BL-0001** `[todo]` **Spike: Godot 4 anime/cel-shader stack
  feasibility.** Validate the *Art and Presentation* §1.1 three-way
  blend (Genshin ramp + HSR warmth + Hades silhouette) is achievable
  in Godot 4 within reasonable shader budget. Time-box: 1–2 weeks.
  Blocks: most rendering decisions. → *Tech and Engine* §1.1, *Art
  and Presentation* §1.1.
- **BL-0002** `[todo]` **Decide: language polyglot baseline (T-Q2).**
  Confirm or revise the C# core + GDScript glue + C/C++/Rust reserved
  + Python tooling proposal. → *Tech and Engine* §2.
- **BL-0003** `[todo]` **Decide: data-layer hybrid stack (T-Q3).**
  Confirm or revise the JSON source → SQLite runtime → in-memory +
  graph projection proposal. → *Tech and Engine* §3.
- **BL-0004** `[todo]` **Decide: source format (T-Q15).** YAML / JSON
  / TOML / Markdown-with-frontmatter for content extracts.
- **BL-0005** `[todo]` **Decide: Backlog format (W-Q2).** Confirm or
  revise the format used in this very file.
- **BL-0006** `[todo]` **Decide: variant rules baseline (R-Q1).**
  Free Archetype, ABP, PWL, etc.
- **BL-0007** `[todo]` **Build: content pipeline skeleton.** YAML/JSON
  source → validator → SQLite builder → engine loader, end-to-end
  smoke test on one trivial spell record. Blocks: all content import.
- **BL-0008** `[todo]` **Build: PF2e dice expression evaluator
  (rules engine spike).** Standalone library that parses and rolls
  arbitrary PF2e dice expressions, including conditional bonuses
  and trait-derived modifiers.
- **BL-0009** `[todo]` **Decide: protagonist V-Q-followups.** Opening
  framing (V-Q3), orientation (V-Q4), aging (V-Q5), language set
  (V-Q6), distinctive marks (V-Q7), voice profile (V-Q8), face
  customization (V-Q9), starting location (V-Q10).
- **BL-0010** `[todo]` **Decide: NSFW asset-generation filter
  policy confirmation (N-Q13).** Confirm every NSFW generation
  pipeline includes a minor-content filter at gen time.
- **BL-0011** `[todo]` **Stand up: testing harness for the rules
  engine.** xUnit / NUnit / Godot test runner; first tests on dice
  evaluator (BL-0008).
- **BL-0012** `[todo]` **Decide: repo strategy for generated assets
  (T-Q12).** Git-LFS in main repo / separate assets repo / external
  store with manifest references.

## Cross-References

- *DESIGN - Workflow* §7 — spike lifecycle policy.
- *DESIGN - Tech and Engine* — most engine/data-layer tasks live here.
- *DESIGN - Open Questions* — every `[todo] Decide:` task references
  one or more open question IDs.

## Open Questions (Backlog-Index-Local)

- BL-Q1. **(W-Q2 mirror)** Confirm or replace the format used above
  (ID prefix, status tags, definition-of-done convention, file split).
- BL-Q2. Should the backlog have **priority tags** (P0/P1/P2/P3) on
  top of status tags?
- BL-Q3. Should `[blocked]` tasks include a `blocks-on:` field
  pointing to the resolution dependency?
- BL-Q4. Should `[done]` tasks be archived to a per-file
  `Backlog - <Sub> (Archive).md` after some threshold?
- BL-Q5. Auto-numbering policy — is `BL-NNNN` global or per-file?
- BL-Q6. Should backlog files embed the Open Questions registry
  cross-reference, or rely on the user to read both?
