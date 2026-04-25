# Rules — Index

> Master index of the **PF2e mechanical rules reference** for our project.
> Two layers:
>
> 1. **Untouched PF2e Remaster rules** — the canonical baseline as
>    published by Paizo, transcribed and cleanly indexed for our use.
> 2. **Project-reworked rules** — our adaptations (real-time combat
>    translation, alchemical magic resource model, etc.).
>
> *Design discussion* lives in `DESIGN/`. *This folder is the mechanic
> reference* — what a player or developer looks at when they need to
> know how a rule actually works in our game.

---

## Conventions

- File naming: `Rules - <Sub> (<Layer>).md` where `<Layer>` is one of:
  - `(Untouched)` — PF2e Remaster RAW transcription.
  - `(Project)` — our reworked version of the same scope.
  - When no rework exists, only `(Untouched)` is needed.
- Cross-references use *italic Sub Name (Layer)*.
- Each rules file ends with an **Open Questions** section using prefix
  `RULES-Q*`.
- When a `(Project)` file exists, it must explicitly state which
  `(Untouched)` text it replaces or supplements, and link to the
  relevant `DESIGN - <Domain>.md` for rationale.
- Source citation: every `(Untouched)` rule cites its source book and
  page (e.g., "Player Core p.412, Remaster").

## Top-Level Structure (planned)

(Files created as content is imported per the extract-by-extract
import workflow.)

### Core Mechanics

| File | Scope |
|---|---|
| `Rules - The Basics (Untouched).md` | Proficiency, level, attribute mods, DC by level |
| `Rules - Dice and Rolling (Untouched).md` | d20 mechanics, success tiers, crits |
| `Rules - Action Economy (Untouched).md` | 3-action turn, reactions, free actions |
| `Rules - Action Economy (Project).md` | Real-time hybrid (stamina + cooldown + MAP-as-swing-rate) |
| `Rules - Conditions (Untouched).md` | Frightened, off-guard, slowed, etc. |
| `Rules - Damage Types (Untouched).md` | Physical, energy, void, vitality, etc. |
| `Rules - Saving Throws (Untouched).md` | Fortitude, Reflex, Will |
| `Rules - Initiative (Untouched).md` | (May not surface in real-time; see Project layer) |

### Combat

| File | Scope |
|---|---|
| `Rules - Combat Actions (Untouched).md` | Strike, Step, Stride, Sustain, etc. |
| `Rules - Combat Actions (Project).md` | Real-time mappings |
| `Rules - Weapons (Untouched).md` | Weapon traits, groups, runes |
| `Rules - Armor (Untouched).md` | Light/medium/heavy, traits |
| `Rules - Multi-Attack-Penalty (Untouched).md` | RAW MAP |
| `Rules - Multi-Attack-Penalty (Project).md` | Continuous swing-rate translation |
| `Rules - Reactions (Untouched).md` | Attack of Opportunity etc. |
| `Rules - Reactions (Project).md` | Real-time interrupt translation |
| `Rules - Critical Specialization (Untouched).md` | |
| `Rules - Cover and Concealment (Untouched).md` | |
| `Rules - Flanking and Off-Guard (Untouched).md` | |

### Magic

| File | Scope |
|---|---|
| `Rules - Magic Overview (Untouched).md` | Traditions, schools, ranks |
| `Rules - Spell Slots (Untouched).md` | Daily, prepared, spontaneous |
| `Rules - Spell Slots (Project).md` | RAW slots + essence-tier reagents (M-Q2) |
| `Rules - Cantrips (Untouched).md` | |
| `Rules - Focus Spells (Untouched).md` | |
| `Rules - Rituals (Untouched).md` | |
| `Rules - Rituals (Project).md` | Real-time / scheduled diegetic events |
| `Rules - Counterspell and Dispel (Project).md` | Real-time interaction |
| `Rules - Metamagic (Untouched).md` | |
| `Rules - Reagents (Project).md` | Essence tiers, sourcing, costs |

### Skills and Exploration

| File | Scope |
|---|---|
| `Rules - Skills (Untouched).md` | All 16 PF2e skills, untrained → legendary |
| `Rules - Skill DCs (Untouched).md` | |
| `Rules - Exploration Activities (Untouched).md` | |
| `Rules - Exploration Activities (Project).md` | First-person real-time mapping |
| `Rules - Recall Knowledge (Untouched).md` | |
| `Rules - Diplomacy (Untouched).md` | |
| `Rules - Stealth (Untouched).md` | |
| `Rules - Perception (Untouched).md` | |

### Downtime and Crafting

| File | Scope |
|---|---|
| `Rules - Downtime (Untouched).md` | |
| `Rules - Crafting (Untouched).md` | |
| `Rules - Crafting (Project).md` | |
| `Rules - Earn Income (Untouched).md` | |

### Character

| File | Scope |
|---|---|
| `Rules - Ancestries Index (Untouched).md` | |
| `Rules - Ancestry - <Name> (Untouched).md` | One per ancestry |
| `Rules - Classes Index (Untouched).md` | |
| `Rules - Class - <Name> (Untouched).md` | One per class |
| `Rules - Class - <Name> (Project).md` | Project rework where applicable |
| `Rules - Backgrounds (Untouched).md` | |
| `Rules - Feats Index (Untouched).md` | |
| `Rules - Archetypes Index (Untouched).md` | |
| `Rules - Heritage and Bloodlines (Untouched).md` | |
| `Rules - Languages (Untouched).md` | |

### Equipment

| File | Scope |
|---|---|
| `Rules - Equipment Overview (Untouched).md` | |
| `Rules - Currency and Wealth (Untouched).md` | |
| `Rules - Magic Items (Untouched).md` | |
| `Rules - Runes (Untouched).md` | |
| `Rules - Consumables (Untouched).md` | |
| `Rules - Alchemical Items (Untouched).md` | |

### Variant Rules

| File | Scope |
|---|---|
| `Rules - Variant Rules Index (Untouched).md` | Free Archetype, ABP, PWL, etc. |
| `Rules - Variant Rules (Project).md` | Which variants we adopt as baseline (R-Q1) |

### Adventure-specific

| File | Scope |
|---|---|
| `Rules - Mythic (Untouched).md` | |
| `Rules - Kingdom (Untouched).md` | |
| `Rules - War / Mass Combat (Untouched).md` | |
| `Rules - Vehicles (Untouched).md` | |
| `Rules - Sieges (Untouched).md` | |
| `Rules - Hazards (Untouched).md` | |
| `Rules - Diseases and Poisons (Untouched).md` | |
| `Rules - Curses (Untouched).md` | |

## Cross-References

- *DESIGN - Rules and Edition* — high-level decisions and faithfulness
  stance.
- *DESIGN - Combat* — for `(Project)` combat reworks rationale.
- *DESIGN - Magic* — for `(Project)` magic reworks rationale.

## Open Questions (Rules-Index-Local)

- RULES-Q1. Confirm the file enumeration above (granularity, names).
- RULES-Q2. Sourcing policy for `(Untouched)` — verbatim transcription
  vs faithful summary vs structured table extract?
- RULES-Q3. How tightly should `(Untouched)` files cite source page
  numbers and edition years?
- RULES-Q4. When a rule changes between Paizo printings (errata), how
  do we record version history?
- RULES-Q5. Tiered file split — at what point does a single file
  become so large that it splits (e.g., one `Rules - Spells -
  <Tradition>.md` per tradition)?
- RULES-Q6. Cross-link format to `DESIGN/` and `Lore/` files
  (Markdown links, plain references, both).
- RULES-Q7. Machine-readable mirror — does each `Rules - X (Untouched).md`
  also have a `Content/Core/<x>.json` machine-readable counterpart, or
  are these two pipelines independent?
