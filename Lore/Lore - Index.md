# Lore — Index

> Master index of the **in-fiction Golarion content corpus** as we use it
> in the project. This folder contains canon as deployed (with our
> reworks merged in-place), not design discussion about the reworks.
>
> The *design discussion* about what we rework lives in
> `DESIGN/DESIGN - Lore Reworks.md`. The *content* — the actual reworked
> cosmology, factions, regions, deities, etc. — lives here.

---

## Conventions

- File naming: `Lore - <Sub>.md`, capitalized, spaces around the dash.
- Cross-references use *italic Sub Name*.
- Each lore file is **canon-as-played** — what is true in our Golarion.
  Differences from upstream Paizo canon are marked inline with a callout
  block tagged `> **Rework note:**`.
- Each lore file ends with an **Open Questions** section using prefix
  `LORE-Q*` for lore-local questions.
- Major reworks reference the relevant `DESIGN - <Domain>.md` doc.

## Top-Level Structure (planned)

(Files will be created as content is imported and decided per the
extract-by-extract import workflow.)

### Imported so far

| File | Source | Status |
|---|---|---|
| `Lore - Falcon's Hollow.md` | `module:hlh:01-adventure-background` | Stub (this turn) |
| `Lore - Disease - Blackscour.md` | `module:hlh:01-adventure-background` | Stub (this turn) |
| `Lore - NPC - Laurel.md` | `module:hlh:01-adventure-background` | Stub (this turn) |
| `Lore - Faction - Falcon's Hollow Constabulary.md` | `module:hlh:01-adventure-background` | Stub (this turn) |
| `Lore - Faction - Church of Iomedae (Falcon's Hollow).md` | `module:hlh:01-adventure-background` | Stub (this turn) |

| File | Scope |
|---|---|
| `Lore - Cosmology.md` | The Great Beyond, planes, deities, souls, Pharasma's Boneyard |
| `Lore - Calendar and Time.md` | Absalom Reckoning, holidays, seasons, lunar cycles |
| `Lore - Languages.md` | Common, regional, secret, planar, dead languages |
| `Lore - Ancestries.md` | Index of ancestries with project-specific notes |
| `Lore - Inner Sea Region.md` | Avistan + Garund overview |
| `Lore - Absalom.md` | The City at the Center of the World |
| `Lore - Cheliax.md` | Imperial House Thrune Cheliax |
| `Lore - Andoran.md` | Eagle Knights, freedom, etc. |
| `Lore - Taldor.md` | Old empire, courtly intrigue |
| `Lore - Varisia.md` | Frontier, Shoanti, Korvosa |
| `Lore - Ustalav.md` | Gothic horror |
| `Lore - Brevoy and Stolen Lands.md` | Kingmaker territory |
| `Lore - Mwangi Expanse.md` | Magaambya, Mzali |
| `Lore - Osirion.md` | Pharaohs, deserts |
| `Lore - Katapesh.md` | Trade and slavery |
| `Lore - Galt.md` | Revolutionary cycles |
| `Lore - Nidal.md` | Zon-Kuthon worship |
| `Lore - Geb and Nex.md` | Necromancy and arcane war |
| `Lore - Nirmathas and Molthune.md` | Border conflict |
| `Lore - Kyonin.md` | Elven realm |
| `Lore - Druma.md` | Mercantile Prophecies of Kalistrade |
| `Lore - Numeria.md` | Crashed alien tech (Iron Gods) |
| `Lore - Hold of Belkzen.md` | Orc territory |
| `Lore - Land of the Linnorm Kings.md` | Northern jarls |
| `Lore - Irrisen.md` | Witch-queens of Baba Yaga |
| `Lore - Mendev.md` | Worldwound veterans |
| `Lore - Razmiran.md` | Living-god theocracy |
| `Lore - Tian Xia.md` | Asia-coded continent |
| `Lore - Casmaron.md` | Vudra and Kelesh |
| `Lore - Sarusan.md` | Australia-coded continent |
| `Lore - Arcadia.md` | Americas-coded continent |
| `Lore - Crown of the World.md` | Polar circle |
| `Lore - The Darklands.md` | Underdark equivalents |
| `Lore - Deities.md` | Index of all deities (one file per major) |
| `Lore - Deity - Calistria.md` | Per-deity files |
| `Lore - Deity - ...` | (one per major; minor in batches) |
| `Lore - Factions.md` | Cross-region organizations |
| `Lore - Faction - Pathfinder Society.md` | Per-faction files |
| `Lore - Faction - Hellknights.md` | |
| `Lore - Faction - Magaambya.md` | |
| `Lore - Faction - Eagle Knights.md` | |
| `Lore - Faction - Aspis Consortium.md` | |
| `Lore - Faction - ...` | |
| `Lore - History and Ages.md` | Earthfall, Age of Lost Omens, etc. |
| `Lore - Adventure Path - <Name>.md` | Per-AP lore index |
| `Lore - Iconic Heroes.md` | The iconics as canonical NPCs |
| `Lore - Reworks.md` | The single consolidated rework register |

## Lore Reworks Register

`Lore - Reworks.md` is the **canonical register** of every place we
diverge from Paizo upstream. Every other Lore file may link into it.

## Cross-References

- *DESIGN - Lore Reworks* — design discussion / decision rationale.
- *DESIGN - Rules and Edition* — alignment is gone (R-Q3 resolved);
  affects deity, faction, and ancestry lore.
- *DESIGN - Magic* — magic is reworked alchemical/rational; affects
  cosmology, deity, magic-school lore.
- *Rules - Index* — mechanical reference for things lore-named.

## Open Questions (Lore-Index-Local)

- LORE-Q1. Confirm the high-level region file list above is the right
  enumeration and granularity.
- LORE-Q2. One file per major deity vs grouped by pantheon vs single
  big `Lore - Deities.md` file?
- LORE-Q3. Per-AP lore — one file per AP, or grouped by region?
- LORE-Q4. Reworks register format — single chronological log, or
  domain-grouped, or table-driven?
- LORE-Q5. Versioning — when canon changes between Paizo books we
  pulled from, do we record source-version?
- LORE-Q6. Linking convention to `Rules/` and `DESIGN/` files (Markdown
  links, plain mentions, both?).
