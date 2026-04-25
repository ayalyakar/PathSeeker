# DESIGN — Open Questions

> Consolidated registry of every open question across domains.
> Source of truth: each per-domain doc's "Open Questions" section.
> When a question is **resolved**, the resolution is folded into the
> domain doc and the entry here is marked **RESOLVED** with date and
> a short summary, then archived to the bottom of the file.

---

## Vision (V-Q)

- **V-Q1** Protagonist identity baseline (gender, name, age-bracket, origin).
- **V-Q2** Does the protagonist have a fixed class/archetype, or pick at
  character-creation-lite?
- **V-Q3** Opening framing (amnesia / exiled noble / fresh adventurer /
  catastrophe / isekai / in medias res / player-elected).
- **V-Q4** Protagonist orientation — fixed, fluid, contextual, none?
- **V-Q5** Does the protagonist age over the persistent timeline?

## Rules and Edition (R-Q)

- **R-Q1** Variant rules baseline enumeration (Free Archetype, ABP, PWL,
  Stamina, etc.).
- **R-Q2** Treatment of pre-Remaster spells/feats removed in Remaster.
- **R-Q3** Alignment system — keep removed (Remaster) or reintroduce as
  flavor / corruption-devotion axis?
- **R-Q4** Multiclassing model — archetype-only vs gestalt/dual-class?
- **R-Q5** Level cap.
- **R-Q6** Mythic rules — in scope?
- **R-Q7** Third-party publishers prioritized for conversion.
- **R-Q8** Legacy AP story modernization stance.
- **R-Q9** Society Scenario: in-world membership vs meta layer?

## Core Loop and Structure (L-Q)

- **L-Q1** Time scaling during combat / intimate scenes — 1:1 or 1:7.5?
- **L-Q2** Travel — continuous-only vs fast-travel-with-time-skip?
- **L-Q3** Save model details (rolling autosave interval, slots,
  branch/chapter saves, single canonical vs many).
- **L-Q4** New Game semantics — fresh world per save vs single
  persistent Golarion across protagonist generations.
- **L-Q5** Wait/sleep/skip mechanic — what activities qualify?
- **L-Q6** Aging of protagonist and NPCs.
- **L-Q7** NPC death from old age, disease, accident — modeled?
- **L-Q8** Pause for menus, or always diegetic-time?
- **L-Q9** Multi-protagonist save trees?

## Combat (C-Q)

- **C-Q1** Stamina / cooldown / hybrid for action-economy translation.
- **C-Q2** Lock-on (Souls) vs full free-aim (Skyrim).
- **C-Q3** Hit-stop, posture-break, stagger.
- **C-Q4** Weapon arts vs feats-as-real-time-actions surfacing.
- **C-Q5** Reach / flanking / off-guard preserved positionally?
- **C-Q6** Multi-target / area attacks input model.
- **C-Q7** Initiative — exposed or hidden?
- **C-Q8** Mass combat sub-system.
- **C-Q9** Difficulty scaling.
- **C-Q10** PvP duels / arenas.
- **C-Q11** Crit decks / crit tables surfacing.
- **C-Q12** Death-blow / mercy / capture transitions.

## Magic (M-Q)

- **M-Q1** Spell preparation preserved vs research/study loop?
- **M-Q2** Spell slots vs single resource (mana/focus/essence)?
- **M-Q3** Reagents — universal vs ritual-only.
- **M-Q4** Spontaneous vs prepared distinction post-rework.
- **M-Q5** Divine magic — transactional in rational frame?
- **M-Q6** Occult flavor under "less esoteric."
- **M-Q7** Innate / ancestry magic — biological?
- **M-Q8** Rituals as full diegetic events?
- **M-Q9** Counterspell / dispel real-time.
- **M-Q10** Player-authored spells.
- **M-Q11** Magic items reworked.
- **M-Q12** *Identify magic* as player skill activity.

## NSFW (N-Q)

- **N-Q1** Protagonist body customization — slider vs cosmetic-only.
- **N-Q2** Protagonist canonical orientation.
- **N-Q3** Pregnancy modeling — gestate / sire / both / shape-changed.
- **N-Q4** Children, families, dynasty, parenting (depends on aging L-Q6).
- **N-Q5** STDs / magical equivalents.
- **N-Q6** Internal preference tagging for the scene composer (no UI).
- **N-Q7** Companion sexual autonomy — yes/no.
- **N-Q8** Brothel / sex-work career arc fidelity.
- **N-Q9** Slave / captive system arc structure (both directions).
- **N-Q10** Transformation scope and reversibility.
- **N-Q11** Intimate-component rituals (Calistria, Lamashtu, etc.).
- **N-Q12** Public/private behavior model — social rules sim.
- **N-Q13** Asset-generation pipeline age-verification policy
  (defaulted: every generated asset passes through such a filter
  at gen time; awaiting confirmation).
- **N-Q14** "Romantic but not sexual" arcs — first-class supported.
- **N-Q15** Trauma response modeling.

## Art and Presentation (A-Q)

- **A-Q1** 2.5D mix specifics (billboards / pre-rendered / hand-painted).
- **A-Q2** Outline technique.
- **A-Q3** Cel-shading lighting model.
- **A-Q4** Facial animation pipeline.
- **A-Q5** Hair pipeline.
- **A-Q6** Cloth simulation pipeline.
- **A-Q7** Skin shader for intimate scenes.
- **A-Q8** Photo mode / mirror exception.
- **A-Q9** Diegetic UI props (journal, grimoire, wrist device).
- **A-Q10** Persona-style menu transitions.
- **A-Q11** Voice cloning consent policy.
- **A-Q12** Lip-sync — phoneme-from-audio vs animator-authored.
- **A-Q13** Render target framerate / resolution.
- **A-Q14** Day/night and weather fidelity.

## Tech and Engine (T-Q)

- **T-Q1** Engine: confirm Godot 4 vs Unity 6 vs other.
- **T-Q2** Language polyglot proposal vs single-language stance.
- **T-Q3** Data layer: hybrid stack (JSON → SQLite → in-memory + graph)
  vs another shape.
- **T-Q4** Windows version baseline + minimum hardware target.
- **T-Q5** Plugin system: confirm folder layout proposal; manifest
  format (TOML / JSON / YAML / custom).
- **T-Q6** Local LLM inference backend (llama.cpp / vLLM / koboldcpp /
  Ollama / ExLlamaV2 / custom).
- **T-Q7** Local LLM model lineup for narrative / rules / NSFW.
- **T-Q8** Image-gen stack (ComfyUI hand-built vs Forge / A1111 /
  InvokeAI; checkpoints PonyXL / Illustrious / NoobAI / merges).
- **T-Q9** TTS toolchain (cloud-only / local-only / hybrid).
- **T-Q10** Voice cloning sources policy.
- **T-Q11** 3D character pipeline: Koikatsu/HoneySelect/Daz exports
  vs custom rig from day one.
- **T-Q12** Repo strategy for generated assets (Git-LFS vs separate
  repo vs external store).
- **T-Q13** Spike lifecycle policy (time-box, removal rules).
- **T-Q14** Test strategy for rules engine + content pipeline.
- **T-Q15** Source format choice (YAML / JSON / TOML / Markdown+FM).
- **T-Q16** Future runtime LLM — sketch interface now or defer.
- **T-Q17** Source-control branching (main directly vs feature branches).

## Workflow (W-Q)

- **W-Q1** `LORE`, `RULES`, `BACKLOG`: single root files vs folders
  with sub-files. **Blocks creation of any of these structures.**
- **W-Q2** `BACKLOG` format (Markdown checklist, task IDs, status,
  links to design docs).
- **W-Q3** `RULES` ambiguity: project rules (overlap with *Workflow*)
  vs PF2e mechanics rules. Disambiguate.
- **W-Q4** Working-session mode declaration ritual (explicit vs
  inferred).
- **W-Q5** End-of-session decision-summary style.
- **W-Q6** Re-import policy for previously-imported extracts.

---

## Resolved Questions Archive

### Q30–Q44 (Tech and Engine, Workflow)

- **Q30** Engine preference → **Godot, Unity fallback** (final
  choice pending T-Q1 confirmation).
- **Q31** Language → **Best-for-project**, options to be presented
  (T-Q2). User wants assistant to suggest options.
- **Q32** Data layer → **Best-of-all-worlds**, hybrid stack proposed
  (T-Q3). User wants assistant to suggest options.
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
- **Q39** TTS modality mix → **Mix of all options at dev-time**
  (specifics in T-Q9).
- **Q40** Working style → **Mandatory Q&A loop: assistant asks
  tons of questions, user decides; assistant suggests options when
  user is unsure. Especially during extract-by-extract Pathfinder
  content imports.** Captured in *Workflow*.
- **Q41** Living docs → **DESIGN organized as established; LORE,
  RULES, BACKLOG (actionable only) files welcome.** Layout pending
  W-Q1.
- **Q42** Mode → **Alternate between design-doc work and
  prototyping/vertical-slice work.** Captured in *Workflow* §6.
- **Q43** Speculative throwaway code → **Allowed, must be removed
  once real code shipped.** Captured in *Workflow* §7 + *Tech and
  Engine* §8.
- **Q44** Autonomous defaults → **Forbidden. User decides every
  question, including low-stakes ones.** Captured in *Workflow* §1.
