# DESIGN — Index

> Master index of the design corpus. Update whenever a new domain doc is
> added or a section is promoted out of *Open Questions*.

---

## Conventions

- All design docs live in `DESIGN/<Sub-Folder>/` at the project root.
- File naming: `DESIGN - <Domain>.md`, capitalized, with spaces around
  the dash and inside multi-word domain names.
- Sub-folder layout (resolved IDX-Q1 → Option A): six folders by
  layer — `Foundation/`, `Systems/`, `World/`, `People/`, `Tech/`,
  `Art/`.
- Sibling project folders use `<Folder>/<Folder> - <Sub>.md` (per
  W-Q1).
- Cross-references use *italic Domain Name* (matching the
  `DESIGN - <Domain>.md` filename minus prefix and extension).
- Every doc ends with an **Open Questions** section using a
  per-doc prefix. Prefix registry:

| Prefix | Doc | Folder |
|---|---|---|
| `V-Q` | Vision | Foundation |
| `R-Q` | Rules and Edition | Foundation |
| `L-Q` | Core Loop and Structure | Foundation |
| `LR-Q` | Lore Reworks | Foundation |
| `W-Q` | Workflow | Foundation |
| `IDX-Q` | Index | Foundation |
| `NC-Q` | Naming Conventions | Foundation |
| `GL-Q` | Glossary | Foundation |
| `C-Q` | Combat | Systems |
| `M-Q` | Magic | Systems |
| `SK-Q` | Skill Checks and Exploration | Systems |
| `CR-Q` | Crafting | Systems |
| `IE-Q` | Inventory and Equipment | Systems |
| `SU-Q` | Survival and Body Needs | Systems |
| `DR-Q` | Drugs and Substances | Systems |
| `Q-Q` | Quests and Activities | Systems |
| `EC-Q` | Economy | Systems |
| `WS-Q` | World Simulation | World |
| `LW-Q` | Locations and Worldspace | World |
| `TR-Q` | Travel | World |
| `RD-Q` | Religion and Devotion | World |
| `FR-Q` | Factions and Reputation | World |
| `CJ-Q` | Crime and Justice | World |
| `LG-Q` | Languages | World |
| `MC-Q` | Mass Combat | World |
| `NA-Q` | Naval and Aerial | World |
| `PT-Q` | Planar Travel | World |
| `DA-Q` | Death and Afterlife | World |
| `PI-Q` | Politics and Intrigue | World |
| `TF-Q` | Tournaments and Festivals | World |
| `MA-Q` | Mounts and Animals | World |
| `PR-Q` | Property and Businesses | World |
| `NPC-Q` | NPCs and Companions | People |
| `RR-Q` | Romance and Relationships | People |
| `BI-Q` | Body and Identity | People |
| `DC-Q` | Dialogue and Conversation | People |
| `N-Q` | NSFW | People |
| `T-Q` | Tech and Engine | Tech |
| `CP-Q` | Content Pipeline | Tech |
| `SP-Q` | Save and Persistence | Tech |
| `PB-Q` | Performance Budget | Tech |
| `MD-Q` | Modding and Extensibility | Tech |
| `A-Q` | Art and Presentation | Art |
| `CC-Q` | Camera and Cinematography | Art |
| `AN-Q` | Animation Pipeline | Art |
| `AU-Q` | Audio | Art |
| `LORE-Q` | `Lore/` files | (sibling) |
| `RULES-Q` | `Rules/` files | (sibling) |
| `BL-Q` | `Backlog/` files | (sibling) |

- The cross-doc consolidated open-question registry lives in
  `Foundation/DESIGN - Open Questions.md`.

## Workflow Reminder

The project operates under a **mandatory Q&A loop** (see *Workflow*):
the assistant asks, the user decides, the assistant proposes options
when the user is unsure. **No autonomous defaults, even on low-stakes
questions** — except `Backlog/` files, which the assistant edits
autonomously per *Workflow* §1.1 carve-out.

## Folder Map

```
DESIGN/
├── Foundation/                        9 files
│   ├── DESIGN - Index.md              (this file)
│   ├── DESIGN - Open Questions.md
│   ├── DESIGN - Workflow.md
│   ├── DESIGN - Vision.md
│   ├── DESIGN - Glossary.md
│   ├── DESIGN - Naming Conventions.md
│   ├── DESIGN - Lore Reworks.md
│   ├── DESIGN - Rules and Edition.md
│   └── DESIGN - Core Loop and Structure.md
│
├── Systems/                           9 files
│   ├── DESIGN - Combat.md
│   ├── DESIGN - Magic.md
│   ├── DESIGN - Skill Checks and Exploration.md
│   ├── DESIGN - Crafting.md
│   ├── DESIGN - Inventory and Equipment.md
│   ├── DESIGN - Survival and Body Needs.md
│   ├── DESIGN - Drugs and Substances.md
│   ├── DESIGN - Quests and Activities.md
│   └── DESIGN - Economy.md
│
├── World/                             15 files
│   ├── DESIGN - World Simulation.md
│   ├── DESIGN - Locations and Worldspace.md
│   ├── DESIGN - Travel.md
│   ├── DESIGN - Religion and Devotion.md
│   ├── DESIGN - Factions and Reputation.md
│   ├── DESIGN - Crime and Justice.md
│   ├── DESIGN - Languages.md
│   ├── DESIGN - Mass Combat.md
│   ├── DESIGN - Naval and Aerial.md
│   ├── DESIGN - Planar Travel.md
│   ├── DESIGN - Death and Afterlife.md
│   ├── DESIGN - Politics and Intrigue.md
│   ├── DESIGN - Tournaments and Festivals.md
│   ├── DESIGN - Mounts and Animals.md
│   └── DESIGN - Property and Businesses.md
│
├── People/                            5 files
│   ├── DESIGN - NPCs and Companions.md
│   ├── DESIGN - Romance and Relationships.md
│   ├── DESIGN - Body and Identity.md
│   ├── DESIGN - Dialogue and Conversation.md
│   └── DESIGN - NSFW.md
│
├── Tech/                              5 files
│   ├── DESIGN - Tech and Engine.md
│   ├── DESIGN - Content Pipeline.md
│   ├── DESIGN - Save and Persistence.md
│   ├── DESIGN - Performance Budget.md
│   └── DESIGN - Modding and Extensibility.md
│
└── Art/                               4 files
    ├── DESIGN - Art and Presentation.md
    ├── DESIGN - Camera and Cinematography.md
    ├── DESIGN - Animation Pipeline.md
    └── DESIGN - Audio.md
```

Total: **47 design docs** across 6 sub-folders.

## Status of the Corpus

### Foundation

| Domain | File | Latest |
|---|---|---|
| Index | `Foundation/DESIGN - Index.md` | Reorg this turn |
| Open Questions | `Foundation/DESIGN - Open Questions.md` | Updated this turn |
| Workflow | `Foundation/DESIGN - Workflow.md` | §1.1 Backlog carve-out |
| Vision | `Foundation/DESIGN - Vision.md` | All V-Qs resolved + §7 Anime Story Basis |
| Glossary | `Foundation/DESIGN - Glossary.md` | Stub |
| Naming Conventions | `Foundation/DESIGN - Naming Conventions.md` | Stub |
| Lore Reworks | `Foundation/DESIGN - Lore Reworks.md` | LR-001 alignment, LR-002 magic |
| Rules and Edition | `Foundation/DESIGN - Rules and Edition.md` | Honor Remaster |
| Core Loop and Structure | `Foundation/DESIGN - Core Loop and Structure.md` | Fresh world per save |

### Systems

| Domain | File |
|---|---|
| Combat | `Systems/DESIGN - Combat.md` |
| Magic | `Systems/DESIGN - Magic.md` |
| Skill Checks and Exploration | `Systems/DESIGN - Skill Checks and Exploration.md` |
| Crafting | `Systems/DESIGN - Crafting.md` |
| Inventory and Equipment | `Systems/DESIGN - Inventory and Equipment.md` |
| Survival and Body Needs | `Systems/DESIGN - Survival and Body Needs.md` |
| Drugs and Substances | `Systems/DESIGN - Drugs and Substances.md` |
| Quests and Activities | `Systems/DESIGN - Quests and Activities.md` |
| Economy | `Systems/DESIGN - Economy.md` |

### World

| Domain | File |
|---|---|
| World Simulation | `World/DESIGN - World Simulation.md` |
| Locations and Worldspace | `World/DESIGN - Locations and Worldspace.md` |
| Travel | `World/DESIGN - Travel.md` |
| Religion and Devotion | `World/DESIGN - Religion and Devotion.md` |
| Factions and Reputation | `World/DESIGN - Factions and Reputation.md` |
| Crime and Justice | `World/DESIGN - Crime and Justice.md` |
| Languages | `World/DESIGN - Languages.md` |
| Mass Combat | `World/DESIGN - Mass Combat.md` |
| Naval and Aerial | `World/DESIGN - Naval and Aerial.md` |
| Planar Travel | `World/DESIGN - Planar Travel.md` |
| Death and Afterlife | `World/DESIGN - Death and Afterlife.md` |
| Politics and Intrigue | `World/DESIGN - Politics and Intrigue.md` |
| Tournaments and Festivals | `World/DESIGN - Tournaments and Festivals.md` |
| Mounts and Animals | `World/DESIGN - Mounts and Animals.md` |
| Property and Businesses | `World/DESIGN - Property and Businesses.md` |

### People

| Domain | File |
|---|---|
| NPCs and Companions | `People/DESIGN - NPCs and Companions.md` |
| Romance and Relationships | `People/DESIGN - Romance and Relationships.md` |
| Body and Identity | `People/DESIGN - Body and Identity.md` |
| Dialogue and Conversation | `People/DESIGN - Dialogue and Conversation.md` |
| NSFW | `People/DESIGN - NSFW.md` |

### Tech

| Domain | File |
|---|---|
| Tech and Engine | `Tech/DESIGN - Tech and Engine.md` |
| Content Pipeline | `Tech/DESIGN - Content Pipeline.md` |
| Save and Persistence | `Tech/DESIGN - Save and Persistence.md` |
| Performance Budget | `Tech/DESIGN - Performance Budget.md` |
| Modding and Extensibility | `Tech/DESIGN - Modding and Extensibility.md` |

### Art

| Domain | File |
|---|---|
| Art and Presentation | `Art/DESIGN - Art and Presentation.md` |
| Camera and Cinematography | `Art/DESIGN - Camera and Cinematography.md` |
| Animation Pipeline | `Art/DESIGN - Animation Pipeline.md` |
| Audio | `Art/DESIGN - Audio.md` |

## Sibling Project Folders

| Folder | Index | Status |
|---|---|---|
| `Lore/` | `Lore/Lore - Index.md` | Index drafted; sub-files pending content import |
| `Rules/` | `Rules/Rules - Index.md` | Index drafted; sub-files pending content import |
| `Backlog/` | `Backlog/Backlog - Index.md` | 26 seed tasks; autonomously edited (per *Workflow* §1.1) |

## Reading Order for a New Reader

1. `Foundation/DESIGN - Workflow.md` (mandatory project rules)
2. `Foundation/DESIGN - Vision.md`
3. `Foundation/DESIGN - Rules and Edition.md`
4. `Foundation/DESIGN - Core Loop and Structure.md`
5. `People/DESIGN - NSFW.md` (load-bearing across many subsystems)
6. `Art/DESIGN - Art and Presentation.md`
7. `Systems/DESIGN - Combat.md`
8. `Systems/DESIGN - Magic.md`
9. `Tech/DESIGN - Tech and Engine.md`
10. `Tech/DESIGN - Content Pipeline.md`
11. `World/DESIGN - World Simulation.md`
12. `People/DESIGN - NPCs and Companions.md`
13. Other domain docs as relevant.
14. `Foundation/DESIGN - Open Questions.md` (current state of unresolved decisions)

## Open Questions (Index-Local)

- ~~IDX-Q1.~~ **Resolved.** DESIGN/ split into 6 sub-folders per
  Option A (Foundation, Systems, World, People, Tech, Art).
- **IDX-Q2.** Cross-reference link format — should the italic
  `*Foo*` cross-reference convention be supplemented with actual
  relative Markdown links (e.g., `[*Combat*](../Systems/DESIGN -
  Combat.md)`) now that there's sub-folder navigation? Tradeoff:
  real links work in IDE / GitHub preview but become brittle to
  further reorgs.
