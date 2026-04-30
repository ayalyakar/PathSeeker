# DESIGN — Naming Conventions

> Living document. Naming rules for code, content, assets, files,
> folders, NPCs, items, and in-game entities.

---

## 1. Stance

OCD-grade organization (per the user's stated preference). Names
should be predictable, consistent, and capable of scaling to thousands
of entities without collision.

## 2. Folder and File Naming

- **Folders**: capitalized, multi-word with spaces (`Lore/`,
  `Adventure Path/`).
- **Design files**: `DESIGN - <Domain>.md`.
- **Lore files**: `Lore - <Sub>.md`.
- **Rules files**: `Rules - <Sub> (<Layer>).md`.
- **Backlog files**: `Backlog - <Sub>.md`.
- **Code-folder folders**: capitalized, multi-word with spaces
  (e.g., `Engine/Rules Engine/`, `Engine/World Simulation/`)
  pending NC-Q5 (some teams prefer code folders without spaces).

## 3. Code Naming (proposed; pending NC-Q1)

| Element | Convention |
|---|---|
| C# class | `PascalCase` |
| C# method | `PascalCase` |
| C# field | `_camelCase` (private), `PascalCase` (public) |
| C# const | `PascalCase` |
| GDScript class | `PascalCase` |
| GDScript func | `snake_case` |
| GDScript var | `snake_case` |
| File (C#) | `PascalCase.cs` |
| File (GDScript) | `snake_case.gd` |
| Namespace | `PathSeeker.<Area>.<Sub>` |

## 4. Content ID Naming (proposed; pending NC-Q3)

- **Slug**: kebab-case ASCII (`fireball`, `armor-of-magnetism`).
- **Plugin-scoped**: `<plugin>:<slug>` (`core:fireball`,
  `rotrl:thistletop`).
- **Category-prefix**: `spell.fireball`, `item.armor-of-magnetism`,
  `npc.gherman`, `region.absalom`.

## 5. Cross-References

- *Workflow* §5 — design-doc convention origin.
- *Content Pipeline* — content ID stability (CP-Q13).
- *Tech and Engine* — code conventions.

## 6. Open Questions (Naming Conventions-Local)

- ~~**NC-Q1**~~ **Resolved.** Code naming table in §3 confirmed.
- **NC-Q2** Specific C# code style (StyleCop, EditorConfig, .editorconfig
  bundle)?
- **NC-Q3** Confirm content ID convention in §4.
- **NC-Q4** Asset file naming (`SM_<...>` static mesh, `T_<...>`
  texture — Unreal-style, or other)?
- **NC-Q5** Code folder names — with spaces (per project convention)
  or `PascalCase` (typical Godot/C# convention)?
- **NC-Q6** Localization key naming (mirror plugin-scoped IDs)?
- **NC-Q7** Save-data field naming (snake_case, camelCase)?
- **NC-Q8** Database table/column naming (snake_case standard)?
- **NC-Q9** Branch / commit message conventions?
- **NC-Q10** Test naming (Given_When_Then, MethodName_Scenario_Result,
  free-form)?
- **NC-Q11** NPC display vs ID naming — separate fields?
- **NC-Q12** Translit policy for non-English names (Tian, Vudran,
  Mwangi)?
- **NC-Q13** Numbering for ordered content (`Chapter 01 - X.md` vs
  `Chapter 1 - X.md`)?
