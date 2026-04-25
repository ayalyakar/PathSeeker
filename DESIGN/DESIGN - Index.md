# DESIGN — Index

> Master index of the design corpus. Update whenever a new domain doc is
> added or a section is promoted out of *Open Questions*.

---

## Conventions

- All design docs live in `DESIGN/` at the project root.
- File naming: `DESIGN - <Domain>.md`, capitalized, with spaces around
  the dash and inside multi-word domain names.
- Folders elsewhere in the project follow the same capitalization
  convention (e.g., `Source/`, `Content/`, `Engine/`, `Tools/`,
  `Assets/`, `Tests/`, `Docs/`).
- Cross-references use *italic Domain Name* (matching the
  `DESIGN - <Domain>.md` filename minus prefix and extension).
- Every doc ends with an **Open Questions** section using a
  per-doc prefix: `V-Q*` Vision, `R-Q*` Rules and Edition, `L-Q*`
  Core Loop and Structure, `C-Q*` Combat, `M-Q*` Magic, `N-Q*` NSFW,
  `A-Q*` Art and Presentation, `T-Q*` Tech and Engine, `W-Q*`
  Workflow, etc.
- The cross-doc consolidated open-question registry lives in
  `DESIGN - Open Questions.md`.

## Workflow Reminder

The project operates under a **mandatory Q&A loop** (see *Workflow*):
the assistant asks, the user decides, the assistant proposes options
when the user is unsure. **No autonomous defaults, even on low-stakes
questions.** Read *Workflow* before any working session.

## Status of the Corpus

| Domain | File | Status |
|---|---|---|
| Vision | `DESIGN - Vision.md` | First draft (Q1–Q4 captured) |
| Rules and Edition | `DESIGN - Rules and Edition.md` | First draft (Q5–Q10 captured) |
| Core Loop and Structure | `DESIGN - Core Loop and Structure.md` | First draft (Q11–Q15 captured) |
| Combat | `DESIGN - Combat.md` | First draft (Q16–Q18 stub) |
| Magic | `DESIGN - Magic.md` | Stub (rework directive only) |
| NSFW | `DESIGN - NSFW.md` | First draft (Q19–Q24 captured) |
| Art and Presentation | `DESIGN - Art and Presentation.md` | First draft (Q25–Q29 captured) |
| Tech and Engine | `DESIGN - Tech and Engine.md` | First draft (Q30–Q44 captured) |
| Workflow | `DESIGN - Workflow.md` | First draft (Q40 + Q44 codified) |
| Open Questions | `DESIGN - Open Questions.md` | First consolidated draft |

## Domain Docs Pending Creation

(Will be added as their parent domain matures.)

- `DESIGN - Lore Reworks.md` — what we change about Golarion canon.
- `DESIGN - Quests and Activities.md` — quest authoring + procgen.
- `DESIGN - NPCs and Companions.md` — schedules, memory, AI.
- `DESIGN - Romance and Relationships.md` — emotional layer of NSFW.
- `DESIGN - Crafting.md` — alchemy/forge/scribe/etc.
- `DESIGN - Economy.md` — money, work, trade, businesses.
- `DESIGN - Factions and Reputation.md` — factional graph.
- `DESIGN - Religion and Devotion.md` — divine relationships.
- `DESIGN - Body and Identity.md` — body progression, transformation.
- `DESIGN - World Simulation.md` — time, weather, ecology.
- `DESIGN - Audio.md` — music, sfx, voice handling.
- `DESIGN - Content Pipeline.md` — Pathfinder data → game data flow.
- `DESIGN - Modding and Extensibility.md`
- `DESIGN - Save and Persistence.md`

## Sibling Project Docs (Pending User Decision on Layout — W-Q1)

The user has indicated **LORE**, **RULES**, and **BACKLOG** are
welcome. Layout (single files vs folders with sub-files) is **not yet
decided** — see *Workflow* W-Q1.

## Reading Order for a New Reader

1. `DESIGN - Workflow.md` (mandatory project rules)
2. `DESIGN - Vision.md`
3. `DESIGN - Rules and Edition.md`
4. `DESIGN - Core Loop and Structure.md`
5. `DESIGN - NSFW.md` (load-bearing across many subsystems)
6. `DESIGN - Art and Presentation.md`
7. `DESIGN - Combat.md`
8. `DESIGN - Magic.md`
9. `DESIGN - Tech and Engine.md`
10. `DESIGN - Open Questions.md`
