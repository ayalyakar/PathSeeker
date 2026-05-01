# DESIGN — Open Questions

> Consolidated registry of every open question across domains.
> Source of truth: each per-domain doc's "Open Questions" section.
> When a question is **resolved**, the resolution is folded into the
> domain doc and the entry here is marked **RESOLVED** with a short
> summary, then archived to the bottom of the file.

---

## Foundational Domains

### Vision (V-Q)

- **V-Q11 (re-posed)** What scene/clip/storyboard export tooling does
  the project commit to (now that anime focus is **main**)? See
  per-doc options.
- **V-Q14 (new)** Anime / manga / light-novel reference inspiration
  list — please enumerate ("tons of inspirations").
- **V-Q15 (new)** Cinematic density budget shape (per CC-Q1 +
  Vision §7.2).
- **V-Q16 (new)** "Wrongness" mechanism — pre-author what NPCs
  pick up, or leave it loose?

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

- ~~IDX-Q1.~~ **Resolved.** DESIGN/ split into 6 sub-folders
  (Foundation, Systems, World, People, Tech, Art) per Option A. See
  `DESIGN/Foundation/DESIGN - Index.md`.

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

### This turn

**Vision:**
- **V-Q15** → **BG3-frequent and more** — anime-grade cinematic
  density. Cross-doc commitment: *Camera and Cinematography*,
  *Animation Pipeline*, *Audio*, *Performance Budget* all sized
  for upper-bound cinematic budget. Numeric anchor pending
  V-Q15-followup.
- **V-Q16** → **Two-channel "wrongness"** — `Magnetism` (variable
  pull, especially women, single or partnered) + ambiguous `Aura`
  (good/bad polarity unreadable to most). See *Vision* §4.4.1.
  Engine for emergent NSFW (per *NSFW* §5.2), romance baseline
  (per *Romance and Relationships* §3.1), NPC reaction model
  (per *NPCs and Companions* §4.1).

### Previous turn

**Vision:**
- **V-Q11-followup** → **All parallel.**
- **V-Q14** → **Resolved (initial batch).** Inspirations list.
- **V-Q17** → **Openly atheist** (Rahadoumi-style). See
  *Religion and Devotion* §3.1.

### Previous turn

**Vision:**
- **V-Q11** → **Yes** (committed). Scene-export tooling in scope —
  screenshot mode, clip recorder, panel/storyboard export, episode
  export — sequencing pending V-Q11-followup. Anchored by §7
  "main focus" elevation.

**Tech / Pipeline:**
- **CP-Q1 / T-Q15** → re-confirmed: hybrid Markdown-w/-YAML-frontmatter
  for prose, pure YAML for stats.
- **T-Q5** → confirmed: folder layout per *Content Pipeline* §4;
  manifest format = TOML.
- **CP-Q3** → inline YAML `decisions:` block in source-tier file.
- **CP-Q5** → paste-in-chat for small extracts; file drop in
  `Content/Source/_raw/` for large; URL fetch when explicitly
  provided.

**People:**
- **BI-Q1** → composed independent subsystems (skin, hair, wounds,
  intimate, fitness, weight, adornments) aggregated onto a
  `BodyState`. See *Body and Identity* §6.
- **RD-Q1** → mixed patron model (single / multi / none all
  supported). Gherman starts with **no patron**. V-Q17 left open
  for his specific stance.

### Foundational + cross-domain decisions (previous turn)

**Vision V-Q follow-ups & new Q's:**
- **V-Q2-followup** → Effectively unclassed (Option C hidden +
  Option A emergent). See *Vision* §4.3.1.
- **V-Q2-quirks** → Deferred ("mixed and unknown yet").
- **V-Q3-followup** → Deferred ("unspecified").
- **V-Q3-mechanism** → Deferred ("unknown").
- **V-Q6-followup** → "Common is common" — accepted by setting
  convention.
- **V-Q7-followup** → Deferred to play-discovery.
- **V-Q8-followup** → Synthetic-from-prompts (no actor reference).
- **V-Q9-followup** → After BL-0001 cel-shader spike.
- **V-Q10-followup** → Sarenrae's chapel.
- **V-Q12** → No archetype, surface-level only.
- **V-Q13** → Looks human, modern outfit, pervasive "wrongness."
  See *Vision* §4.4.
- **§7 elevated** to "main project focus" (was "soft directive").

**Workflow:**
- **W-Q4 / W-Q5 / W-Q6** → Session-Start Ritual (3 questions
  asked at every session start). See *Workflow* §11.

**Tech / Foundation:**
- **T-Q2** → Polyglot (C# core + GDScript glue + reserved C/Rust
  + Python tooling).
- **T-Q3** → Hybrid data layer (YAML/JSON source → SQLite runtime
  → in-memory + graph projection).
- **T-Q4** → Windows 11 baseline.
- **T-Q15 / CP-Q1 / Q-Q1** → Hybrid source format
  (Markdown+YAML-frontmatter for prose, pure YAML for stats).
- **NC-Q1** → Code naming table confirmed.
- **IDX-Q2** → Italics + first-mention relative MD links.
- **PB-Q1** → Windows 11 baseline (hardware floor TBD).

**Lore:**
- **LR-Q1** → Initial register: LR-001 alignment, LR-002 magic,
  **LR-003 gods (new)**, **LR-004 meta-lore (new)**.

**Architecture:**
- **WS-Q1** → Hybrid single-global + LOD-tiered.
- **NPC-Q2** → 1,000+ named NPCs (hand-authored majors +
  procedurally-stamped-then-frozen for the rest).
- **SP-Q1** → Mixed: SQLite for bulk + JSON sidecar for slot
  metadata.
- **MD-Q1** → TOML for plugin manifests.

**Systems:**
- **DC-Q1** → Ink (by Inkle) for dialogue authoring.
- **DC-Q2 / SK-Q1** → Numeric DC for major rolls; pass/fail
  tier for minor rolls.
- **IE-Q1 / CR-Q2** → Hybrid (diegetic + menu).
- **EC-Q2** → Agent-based market simulation.
- **SU-Q1** → Project-Zomboid harsh need pace.
- **DR-Q3** → Per-substance tolerance/addiction.

**People:**
- **RR-Q1** → Hybrid affect-map (fixed core dimensions + free-form
  per-NPC tags).

**World:**
- **FR-Q1** → ~500–1,000 factions, tiered depth.
- **LW-Q1** → Compressed-for-travel but true-to-Golarion geography.
- **TR-Q1** → Real-time walked + player-choice abstraction on
  safe routes.
- **CJ-Q1** → Witness model (line-of-sight + memory + report-rate)
  confirmed.

**Art:**
- **CC-Q1** → Authored transitions + lots of cinematics.
- **AN-Q1** → Universal humanoid base rig + per-ancestry overrides.
- **AU-Q1** → Hybrid music engine.
- **GL-Q1** → Flat alphabetical glossary.

### Foundational decisions (previous turn — class arc)

- **V-Q2** → **Resolved.** Flexible class with unique quirks
  (exposed later). See *Vision* §4.3.
- **V-Q3** → **Resolved.** Isekai (transported from another world)
  + In medias res (player joins after the event); opening at
  Falcon's Hollow / Foam River shore. See *Vision* §4.2.
- **V-Q4** → **Resolved.** Straight. See *Vision* §4.3.
- **V-Q5** → **Resolved.** Ages 1:1 with world from age 21.
- **V-Q6** → **Resolved.** Common only at start.
- **V-Q7** → **Resolved.** Tattoo `08` on inside right wrist.
- **V-Q8** → **Resolved.** No accent, low register, apathetic
  baseline with sarcasm/cynicism, world-worn 21.
- **V-Q9** → **Resolved.** Single canonical face designed by us.
- **V-Q10** → **Partially resolved.** Falcon's Hollow / found on
  Foam River shore / wakes up in town; specific room pending
  V-Q10-followup.
- **IDX-Q1** → **Resolved.** DESIGN/ split into 6 sub-folders
  (Foundation, Systems, World, People, Tech, Art). Reorg this turn.
- **(New pillar)** *Vision* §7 — **Anime Story Basis** — game
  is designed to produce a living world that serves as the
  substrate for anime-style emergent stories.

### Foundational decisions (previous turn)

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
