# DESIGN — Open Questions

> Consolidated registry of every open question across domains.
> Source of truth: each per-domain doc's "Open Questions" section.
> When a question is **resolved**, the resolution is folded into the
> domain doc and the entry here is marked **RESOLVED** with a short
> summary, then archived to the bottom of the file.

---

## Foundational Domains

### Vision (V-Q)

- **V-Q2** Does Gherman have a fixed class/archetype, or pick at
  character-creation-lite? Heightened by V-Q1 unknown-origin framing.
- **V-Q3** Opening framing: amnesia, exiled, abandoned, cursed
  identity-erasure, ritual-stripped, in medias res, isekai-from-Earth,
  recovered-from-comatose, other?
- **V-Q4** Gherman's canonical orientation: fixed straight, fixed
  bi/pan, fluid, or unspecified-and-emergent.
- **V-Q5** Does Gherman age over the persistent timeline?
- **V-Q6** Starting language set?
- **V-Q7** Distinctive marks at start (scars, tattoos, brands, sigils)?
- **V-Q8** Voice profile (accent, register, age-feel, baseline)?
- **V-Q9** Canonical face vs face customization?
- **V-Q10** Starting location of the game?

### Rules and Edition (R-Q)

- **R-Q1** Variant rules baseline enumeration (Free Archetype, ABP,
  PWL, Stamina, Ancestry Paragon, Dual-Class).
- **R-Q2** Treatment of pre-Remaster spells/feats removed in Remaster.
- **R-Q4** Multiclassing model — archetype-only vs gestalt/dual-class?
- **R-Q5** Level cap.
- **R-Q6** Mythic rules — in scope?
- **R-Q7** Third-party publishers prioritized for conversion.
- **R-Q8** Legacy AP story modernization stance.
- **R-Q9** Society Scenario: in-world membership vs meta layer?

### Core Loop and Structure (L-Q)

- **L-Q1** Time scaling during combat / intimate scenes — 1:1 or 1:7.5?
- **L-Q2** Travel — continuous-only vs fast-travel-with-time-skip?
- **L-Q3** Save model details (cadence, slots, branch saves).
- **L-Q5** Wait/sleep/skip mechanic — what activities qualify?
- **L-Q6** Aging of protagonist and NPCs.
- **L-Q7** NPC death from old age, disease, accident — modeled?
- **L-Q8** Pause for menus, or always diegetic-time?
- **L-Q9** Multi-protagonist save trees? (Mostly moot per L-Q4 resolved
  to fresh-world-per-save, but multi-slot UX still applies.)

### Combat (C-Q)

- **C-Q2** Lock-on (Souls) vs full free-aim (Skyrim).
- **C-Q3** Hit-stop, posture-break, stagger.
- **C-Q4** Weapon arts vs feats-as-real-time-actions surfacing.
- **C-Q5** Reach / flanking / off-guard preserved positionally?
- **C-Q6** Multi-target / area attacks input model.
- **C-Q7** Initiative — exposed or hidden?
- **C-Q8** Mass combat sub-system. (See *Mass Combat*.)
- **C-Q9** Difficulty scaling.
- **C-Q10** PvP duels / arenas.
- **C-Q11** Crit decks / crit tables surfacing.
- **C-Q12** Death-blow / mercy / capture transitions.

### Magic (M-Q)

- **M-Q1** Spell preparation preserved vs research/study loop?
- **M-Q3** Reagents — universal vs ritual-only. (Partly answered by
  M-Q2 resolution: universal at minor level for cantrips.)
- **M-Q4** Spontaneous vs prepared distinction post-rework.
- **M-Q5** Divine magic — transactional in rational frame?
- **M-Q6** Occult flavor under "less esoteric."
- **M-Q7** Innate / ancestry magic — biological?
- **M-Q8** Rituals as full diegetic events?
- **M-Q9** Counterspell / dispel real-time.
- **M-Q10** Player-authored spells.
- **M-Q11** Magic items reworked.
- **M-Q12** *Identify magic* as player skill activity.

### NSFW (N-Q)

- **N-Q2** Protagonist canonical orientation. (Mirrors V-Q4.)
- **N-Q3** Pregnancy modeling — gestate / sire / both / shape-changed.
- **N-Q4** Children, families, dynasty, parenting (depends on aging
  L-Q5/L-Q6).
- **N-Q5** STDs / magical equivalents.
- **N-Q6** Internal preference tagging for the scene composer.
- **N-Q7** Companion sexual autonomy — yes/no.
- **N-Q8** Brothel / sex-work career arc fidelity.
- **N-Q9** Slave / captive system arc structure (both directions).
- **N-Q10** Transformation scope and reversibility.
- **N-Q11** Intimate-component rituals (Calistria, Lamashtu, etc.).
- **N-Q12** Public/private behavior model — social rules sim.
- **N-Q13** Asset-generation pipeline age-verification policy
  confirmation.
- **N-Q14** "Romantic but not sexual" arcs — first-class supported.
- **N-Q15** Trauma response modeling.

### Art and Presentation (A-Q)

- **A-Q1** 2.5D mix specifics (billboards / pre-rendered / hand-painted).
- **A-Q2** Outline technique.
- **A-Q4** Facial animation pipeline. (Also AN-Q.)
- **A-Q5** Hair pipeline. (Also AN-Q.)
- **A-Q6** Cloth simulation pipeline. (Also AN-Q.)
- **A-Q7** Skin shader for intimate scenes.
- **A-Q8** Photo mode / mirror exception.
- **A-Q9** Diegetic UI props (journal, grimoire, wrist device).
- **A-Q10** Persona-style menu transitions.
- **A-Q11** Voice cloning consent policy. (Mostly moot per Q33: no
  consent constraints — but technical sourcing still TBD.)
- **A-Q12** Lip-sync — phoneme-from-audio vs animator-authored.
- **A-Q13** Render target framerate / resolution. (Also PB-Q.)
- **A-Q14** Day/night and weather fidelity. (Also WS-Q.)

### Tech and Engine (T-Q)

- **T-Q2** Language polyglot proposal vs single-language stance.
- **T-Q3** Data layer hybrid stack vs another shape.
- **T-Q4** Windows version baseline + minimum hardware target.
- **T-Q5** Plugin system folder layout + manifest format.
- **T-Q6** Local LLM inference backend.
- **T-Q7** Local LLM model lineup.
- **T-Q8** Image-gen stack.
- **T-Q9** TTS toolchain.
- **T-Q10** Voice cloning sources policy. (Mostly moot per Q33.)
- **T-Q11** 3D character pipeline.
- **T-Q12** Repo strategy for generated assets.
- **T-Q13** Spike lifecycle policy.
- **T-Q14** Test strategy for rules engine + content pipeline.
- **T-Q15** Source format choice (YAML / JSON / TOML / Markdown+FM).
- **T-Q16** Future runtime LLM — sketch interface now or defer.
- **T-Q17** Source-control branching policy.

### Workflow (W-Q)

- **W-Q4** Working-session mode declaration ritual (explicit vs
  inferred).
- **W-Q5** End-of-session decision-summary style.
- **W-Q6** Re-import policy for previously-imported extracts.

### Index (IDX-Q)

- **IDX-Q1** Should `DESIGN/` be split into sub-folders given the
  35+ file count?

---

## Second-Wave Domains (high-priority, this turn)

### Content Pipeline (CP-Q)

See `DESIGN - Content Pipeline.md`. Highlights:

- **CP-Q1** Source format for content extracts (mirrors T-Q15 — pick
  one to drive both).
- **CP-Q2** Validation gate model — schema-based, code-based, both?
- **CP-Q3** Per-extract user-decision capture format.

### World Simulation (WS-Q)

See `DESIGN - World Simulation.md`. Highlights:

- **WS-Q1** Tick rate — single global tick vs LOD ticks (foreground
  high-frequency, background low-frequency).
- **WS-Q2** Off-screen NPC simulation depth.

### NPCs and Companions (NPC-Q)

See `DESIGN - NPCs and Companions.md`. Highlights:

- **NPC-Q1** Memory model — perfect recall, decay, summary, hybrid.
- **NPC-Q2** Number of named NPCs target (10s, 100s, 1000s, more).

### Save and Persistence (SP-Q)

See `DESIGN - Save and Persistence.md`. Highlights:

- **SP-Q1** Save file format (binary, SQLite, mixed).
- **SP-Q2** Save migration policy when schema evolves.

### Lore Reworks (LR-Q)

See `DESIGN - Lore Reworks.md`. Highlights:

- **LR-Q1** Initial rework register seed list — what's confirmed
  reworked beyond alignment removal and magic-as-rational?

---

## Third-Wave Domains (mid-priority, this turn)

Per-doc question banks live in their respective `DESIGN - <Domain>.md`
files. Cross-doc highlights only listed above as needed.

- *Quests and Activities* (Q-Q)
- *Romance and Relationships* (RR-Q)
- *Body and Identity* (BI-Q)
- *Religion and Devotion* (RD-Q)
- *Factions and Reputation* (FR-Q)
- *Crafting* (CR-Q)
- *Economy* (EC-Q)
- *Audio* (AU-Q)
- *Modding and Extensibility* (MD-Q)

## Fourth-Wave Domains (proposed, this turn)

- *Dialogue and Conversation* (DC-Q)
- *Skill Checks and Exploration* (SK-Q)
- *Inventory and Equipment* (IE-Q)
- *Locations and Worldspace* (LW-Q)
- *Travel* (TR-Q)
- *Survival and Body Needs* (SU-Q)
- *Crime and Justice* (CJ-Q)
- *Drugs and Substances* (DR-Q)
- *Camera and Cinematography* (CC-Q)
- *Animation Pipeline* (AN-Q)
- *Performance Budget* (PB-Q)
- *Naming Conventions* (NC-Q)
- *Glossary* (GL-Q)

## Fifth-Wave Domains (speculative, this turn)

- *Mass Combat* (MC-Q)
- *Naval and Aerial* (NA-Q)
- *Planar Travel* (PT-Q)
- *Death and Afterlife* (DA-Q)
- *Politics and Intrigue* (PI-Q)
- *Tournaments and Festivals* (TF-Q)
- *Languages* (LG-Q)
- *Mounts and Animals* (MA-Q)
- *Property and Businesses* (PR-Q)

## Sibling-Folder Indexes

- *Lore - Index* (LORE-Q)
- *Rules - Index* (RULES-Q)
- *Backlog - Index* (BL-Q)

---

## Resolved Questions Archive

### Foundational decisions (most recent turn)

- **V-Q1-followup** → **Resolved.** "Unknown" = diegetic mystery
  (Gherman doesn't know his own origin/backstory — discoverable
  in-game). See *Vision* §4.1.
- **W-Q2** → **Resolved.** Backlog format = `BL-NNNN` global IDs +
  checkbox `[ ]`/`[x]` (no status tags) + autonomous edits per the
  new *Workflow* §1.1 carve-out. See `Backlog/Backlog - Index.md`.
- **(New rule)** *Workflow* §1.1 — assistant autonomously edits
  Backlog files; standing approval granted.

### Foundational decisions (initial turn)

- **V-Q1** → **Resolved.** Protagonist Gherman, Male, age 21, ancestry-
  of-origin canonically unknown, backstory canonically unknown. See
  *Vision* §4.1.
- **R-Q3** → **Resolved.** Wholesale Honor Remaster: no alignment
  system in any form. See *Rules and Edition* §5.1.
- **L-Q4** → **Resolved.** Fresh world per save; protagonist
  quasi-narratively immortal at the macro level; failures resolve
  in-game. See *Core Loop and Structure* §6.1.
- **C-Q1** → **Resolved.** Hybrid action-economy: stamina meter +
  per-ability cooldowns + MAP-as-continuous-swing-rate. See *Combat*
  §2.
- **M-Q2** → **Resolved.** Spell slots RAW + essence-tier reagents,
  both layered. See *Magic* §1.1.
- **N-Q1** → **Resolved.** Fixed canonical body + story-state body
  (no slider, both layered). See *NSFW* §5.1.
- **A-Q3** → **Resolved.** Three-way blend: Genshin ramp+specular,
  HSR warmth, Hades silhouette/illustration. See *Art and
  Presentation* §1.1.
- **T-Q1** → **Resolved.** Godot 4 (latest stable). See *Tech and
  Engine* §1.
- **W-Q1** → **Resolved.** `Lore/`, `Rules/`, `Backlog/` are folders
  with `<Folder> - <Sub>.md` sub-files. See *Workflow* §5.1.
- **W-Q3** → **Resolved.** `Rules/` = PF2e mechanical rules
  reference (untouched + project-reworked layers). Project
  laws/workflow stay in *Workflow*. See *Workflow* §5.1.

### Q30–Q44 (Tech and Engine, Workflow — first wave)

- **Q30** Engine preference → **Godot.** Confirmed via T-Q1.
- **Q31** Language → **Best-for-project**, options pending T-Q2.
- **Q32** Data layer → **Best-of-all-worlds**, hybrid stack proposed
  (T-Q3 pending).
- **Q33** Licensing → **Personal project, no copyright/license/
  censoring concerns. Not for redistribution.**
- **Q34** Platform → **Windows-only.**
- **Q35** Solo dev → **Yes, with assistant. First-class plugin
  system would benefit the project.**
- **Q36** LLM-driven content → **Dev-time only**, with a possible
  future runtime caveat (T-Q16).
- **Q37** *(Not decided / already answered — left as no-op.)*
- **Q38** AI use at dev-time → **Complete use across modalities
  with user supervision; nothing ships without explicit approval.**
- **Q39** TTS modality mix → **Mix of all options at dev-time.**
- **Q40** Working style → **Mandatory Q&A loop.** Captured in
  *Workflow*.
- **Q41** Living docs → **DESIGN organized as established; Lore,
  Rules, Backlog folders.** Captured in *Workflow* §5.1.
- **Q42** Mode → **Alternate between design-doc work and prototyping.**
- **Q43** Speculative throwaway code → **Allowed, must be removed
  once real code shipped.**
- **Q44** Autonomous defaults → **Forbidden.** Captured in *Workflow*
  §1.
