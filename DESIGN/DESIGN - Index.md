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
  `A-Q*` Art and Presentation, `T-Q*` Tech and Engine, etc.
- The cross-doc consolidated open-question registry lives in
  `DESIGN - Open Questions.md`.

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
| Tech and Engine | _pending Q30–Q44_ | Not started |
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
- `DESIGN - Tech and Engine.md` — engine choice, data pipeline, AI/LLM.
- `DESIGN - Content Pipeline.md` — Pathfinder data → game data flow.
- `DESIGN - Modding and Extensibility.md`
- `DESIGN - Save and Persistence.md`

## Reading Order for a New Reader

1. `DESIGN - Vision.md`
2. `DESIGN - Rules and Edition.md`
3. `DESIGN - Core Loop and Structure.md`
4. `DESIGN - NSFW.md` (load-bearing across many subsystems)
5. `DESIGN - Art and Presentation.md`
6. `DESIGN - Combat.md`
7. `DESIGN - Magic.md`
8. `DESIGN - Open Questions.md`
