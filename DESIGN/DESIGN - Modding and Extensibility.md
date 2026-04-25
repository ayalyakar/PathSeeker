# DESIGN — Modding and Extensibility

> Living document. The plugin architecture (per Q35 / *Tech and Engine*
> §6) — even though only the user plays the game, treating our own
> content as plugins keeps the codebase modular at scale.

---

## 1. Stance

- All large content is **plugins** under `Content/`.
- The engine **discovers plugins at boot** via manifest.
- Plugins can supply **data, scripts, assets, manifest**.
- Plugin order matters; declared dependencies enforced.

## 2. What's a Plugin?

| Plugin | Examples |
|---|---|
| Core ruleset | Player Core / GM Core / Monster Core |
| Adventure Path | Rise of the Runelords, Kingmaker, etc. |
| Module | One-shot modules |
| Region/Lore pack | Tian Xia expansion, Casmaron pack |
| Faction expansion | Hellknight orders, Pathfinder Society |
| Character pack | Custom companions, iconic-additions |
| Mood pack | Music/lighting/dialogue tone variants |
| NSFW expansion | Specific kink systems, scene packs |
| Mechanic mod | Variant rule sets, alternative magic |
| Original content | All non-canonical content created by us |

## 3. Plugin Layout (proposed; pending T-Q5)

```
Content/<Category>/<Plugin Name>/
├── plugin.toml             (manifest: id, version, deps, load order)
├── data/                   (canonical-tier data)
├── scripts/                (gameplay scripts)
├── assets/                 (textures, models, audio)
├── localization/
└── docs/
```

## 4. Cross-References

- *Tech and Engine* §6 (plugin system).
- *Content Pipeline* — plugins are consumed by the canonical-tier
  builder.
- *Save and Persistence* — mod-affected saves (SP-Q22).

## 5. Open Questions (Modding-Local)

- **MD-Q1** Manifest format — TOML, JSON, YAML, custom (mirrors T-Q5).
- **MD-Q2** Versioning model — semver, date-based, monotonic?
- **MD-Q3** Dependency resolution — strict, loose, ranged?
- **MD-Q4** Load order conflict resolution — last-wins, declared-priority,
  conflict-detection-fail-boot?
- **MD-Q5** Hot-reload during dev (mirrors CP-Q21).
- **MD-Q6** Save migration when plugins change/are removed (SP-Q22).
- **MD-Q7** Script sandboxing — even for trusted (single-user)
  plugins, do we sandbox to prevent self-foot-shooting?
- **MD-Q8** Plugin authoring tool — generate skeleton on command?
- **MD-Q9** Per-plugin test harness?
- **MD-Q10** Asset overrides — plugins can replace core assets?
- **MD-Q11** Per-plugin data schema extension — plugins can add new
  field types to canonical schema?
- **MD-Q12** Plugin discovery — file-system scan, manifest-list,
  both?
- **MD-Q13** "Active plugins" UI — toggle from main menu?
- **MD-Q14** Per-save plugin set — saves remember which plugins
  were active?
- **MD-Q15** Future-runtime-LLM (T-Q16) — does the plugin manifest
  declare runtime-LLM requirements?
