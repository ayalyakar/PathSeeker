# DESIGN — NSFW

> Living document. The project is NSFW-unlocked. This doc captures scope,
> integration, hard limits, and the working principles for content design.
> Treat as load-bearing reference for any system that touches sexuality,
> intimacy, the body, or related dark themes.

---

## 1. Scope

**Everything is in scope** for NSFW content, with one explicit hard
exception (Section 6).

This includes, non-exhaustively:

- Explicit sexual scenes (solo, partnered, group, monstrous).
- Explicit sexual *gameplay* — not just cutscenes, but mechanically
  integrated activity (see Section 3).
- Kink-specific systems (BDSM, bondage, ownership, transformation,
  pregnancy, lactation, futanari, intersex, body modification, scent,
  voyeurism/exhibitionism, public play, prostitution, etc.).
- Extreme / dark content: non-consensual scenes, dubious consent,
  coercion, slavery, drug-induced states, breaking, corruption arcs,
  loss-scenes, torture, deviances, taboos.
- Relationship configurations: monogamous, polyamorous, harem, casual,
  transactional, traumatic, abusive (in either direction).
- Body-state systems: fertility, conception, pregnancy, parenting,
  menstrual cycles, lactation, scent, arousal, exhaustion, injury,
  marks/bruises, scarring, branding, piercing, tattooing, hair growth,
  weight change.

This is not a list of *what should appear constantly* — it is a list
of *what must be possible* when context calls for it.

## 2. Format

- **Full 3D scenes**, using the same character models and rigs as
  gameplay. No 2D CG fallback layer; no asset-isolated "scene mode."
- This implies the **base character pipeline must be NSFW-ready from
  day one** — anatomy modeled, rigged, and animated; clothing as a
  detachable layer; lighting that holds up in close-up.
- All ancestries the player encounters must have the same fidelity
  (lizardfolk, kobolds, tengu, leshy, fetchlings, dhampir, monsters
  from bestiaries, etc.). Cross-ancestry intimacy is in scope.

## 3. Integration

**Completely integrated across all scopes.** NSFW is not a sidebar; it
is woven into:

- **Quest design** — quests can be NSFW-driven, NSFW-resolved, or have
  NSFW branches; not all are, but any can be.
- **Faction reputation** — factions have attitudes toward sexuality
  (Calistria, Shelyn, Pharasma, Iomedae, Norgorber cults, etc.).
- **Romance and relationship** — the romance system *is* the NSFW
  system at its emotional layer; sex is one expression among many.
- **Combat** — capture/loss states can transition into NSFW outcomes
  (cf. Monster Girl Quest); this is opt-in via context, not a
  global game-over flow.
- **Crafting** — clothing, intimate items, sex toys, contraceptives,
  potions, restraints, costumes are first-class craftable categories.
- **Economy** — sex work, courtesan careers, brothel ownership,
  performance arts.
- **Body progression** — body changes (scars, tattoos, fitness,
  pregnancy, lactation, transformations) are persistent and visible.
- **Religion** — divine relationships have intimate dimensions
  (Calistria, Shelyn, Lamashtu, Urgathoa, Norgorber).
- **Side activities** — full-depth: bathhouses, brothels, cuddle
  inns, festivals (Shelyn / Calistria holidays), private clubs,
  cult rites.
- **Lore** — the "heavy rework on lore" license is partly used to
  align canon with mature treatment of sexuality.
- **Status / conditions** — arousal, exhaustion, residue, marks act
  as PF2e-shaped conditions when relevant.

## 4. Player-Facing Toggles and Warnings

- **No content-warning gates.**
- **No filter toggles.**
- **No age-gate flow.** (The project itself is the gate.)
- **No squeamishness UI.** Content surfaces when context invites it.

## 5. Player Character (NSFW-Specific Anchors)

- Pre-defined **human** protagonist (per *Vision*).
- **Gherman, male, age 21** (resolved V-Q1; see *Vision* §4.1).
  - Rationale: anchors anatomy, rigging, animation, and partner-pair
    design so the engine has a stable "main rig" while supporting any
    partner ancestry against it.

### 5.1 Body Model (resolved N-Q1)

> **Fixed canonical body + story-state body.** Both, layered.

- **Fixed canonical body**: Gherman's base appearance, proportions,
  and intimate anatomy are **authored by us, not slider-driven**.
  No character-creation body editor.
- **Story-state body**: the body **changes through play** in
  response to in-fiction events:
  - Training and athletics → muscle definition.
  - Hunger / asceticism / illness → leanness.
  - Wealth and idleness → softness.
  - Combat injuries → scars (per-location, persistent).
  - Magical transformations → reversible or permanent shape changes.
  - Curses, blessings, alchemy → ancestry-bordering changes.
  - Tattoos, brands, piercings → cosmetic-but-persistent.
  - NSFW-specific changes (per N-Q-followups below): pregnancy
    state if shape-changed female, lactation, etc.
- **No "build" customization slider for the player.** Visible body
  state is always the *consequence of in-game events*.
- **Cosmetic adornments** (clothing, hairstyle, jewelry, makeup,
  scarification, body paint) are player-controllable as activities,
  not as a character-creation menu.

This pairs cleanly with *Vision* §4.1 (canonical identity) and the
*Body and Identity* doc (TBD) which will codify the state-tracking
specifics.

### 5.2 Magnetism as Scene-Emergence Engine (per V-Q16)

The **Magnetism** channel from *Vision* §4.4.1 is the diegetic
engine that drives intimate-scene emergence. Where most games
require explicit player initiation (dialogue choice, romance gate,
quest trigger), PathSeeker's NSFW scenes can emerge organically
because the world has a real reason for them to:

- NPCs in **infatuation** band may proposition Gherman during
  ordinary interaction; he can accept or refuse.
- NPCs in **obsession** band actively pursue intimacy with him —
  some respect a refusal, some don't (depending on personality).
  This produces both **welcome romantic intensity** and **stalking
  / coercion / dub-con** scenarios with full mechanical fidelity.
- The magnetism is **not consent-conferring.** A Magnetism-driven
  NPC pursuing Gherman is **not implicitly authorized** by the
  pull. The system models *Magnetism causes pursuit* but
  *consent is a separate axis* — both Gherman's consent and the
  NPC's awareness-of-being-magneted are tracked and surfaced as
  appropriate to the scene.
- The transgressive-content commitments (per §1, §6, V-Q14
  inspirations) become **systemically grounded** — emergent dub-
  con / non-con scenarios are not contrived; the magnetism makes
  them plausible.

## 6. Hard Limits

**The single absolute hard refusal:**

- **No explicit depiction of sexual content involving minors.**

This applies to:
- Generated text describing sexual acts involving minors.
- Generated images, models, or scenes depicting same.
- Mechanics that frame minors as romance/sexual targets.
- "Aged-up" workarounds that rely on visually child-coded characters.

This is a strict line and will be enforced at every layer (data,
generation, runtime). Everything else is allowed.

**Outside that line, no further refusals.** Dark themes, non-con,
coercion, taboo, monstrous, extreme — all allowed when narratively
or systemically called for.

## 7. Working Principles for Content Design

(How this collaboration produces NSFW content responsibly while
respecting your "no toggles, no warnings" stance.)

- **Diegetic gating, not UI gating.** Dark content arrives through
  context (location, NPC personality, faction, choices, time of day),
  not through menu sliders. The world's *fiction* is the filter.
- **Consent within the fiction is a design variable, not a refusal
  mechanism.** Some scenes are consensual, some aren't; the system
  models both with the same fidelity.
- **Mechanical consequences are real.** A coerced encounter leaves
  marks (mood, reputation, body, faction). A loving one does too.
- **Authorship pipeline is tooled.** Hand-authored scenes for major
  arcs; procedurally composed for ambient/background content; LLM/
  diffusion-generated for tail-of-distribution, with quality review.
- **No "punishment" framing of NSFW.** Sex isn't a fail-state; it's
  one possible outcome among many.

## 8. Cross-References

- *Vision* — protagonist is human; tone is context-dependent.
- *Core Loop and Structure* — body progression as one progression
  surface among many; relationship/romance as AP-grade depth.
- *Rules and Edition* — body/intimate conditions modeled as PF2e-
  shaped conditions/effects; ancestry-faithful anatomy.
- *Tech and Engine* (TBD) — pipeline for body, animation, content
  generation, age-verification of all generated assets at gen time.
- *Lore Reworks* (TBD) — Golarion lore reshaped where canon under-
  serves a mature treatment.

## 9. Open Questions (NSFW-Local)

- ~~N-Q1.~~ **Resolved.** Fixed canonical body + story-state body
  (no slider, both layered). See §5.1.
- N-Q2. Protagonist canonical orientation — fixed, fluid, player-
  declared during opening, or no-orientation-axis-at-all (always
  contextual)?
- N-Q3. Pregnancy — does the protagonist gestate (if female-bodied),
  sire (if male-bodied), or both (if shape-changed)? Persistent
  character impact (months of in-game time)?
- N-Q4. Children / families — long-timeline systems for offspring,
  parenting, dynasty? (Connects to L-Q6 aging.)
- N-Q5. STDs / magical equivalents — modeled as PF2e diseases with
  intimate vectors?
- N-Q6. Fetish opt-in/out — even with no UI toggles, do you want
  *internal* tagging so a "scene composer" can prefer/avoid certain
  themes per-protagonist (e.g., this character canonically isn't
  into X), or does everything roll without preference?
- N-Q7. Companion sexual autonomy — companions pursue NSFW
  relationships with each other and with NPCs independent of the
  player. In scope?
- N-Q8. Brothel/sex-work career arc — fully supported career path
  with mechanics (clientele, skills, reputation, ownership)?
- N-Q9. Slave/captive systems — both directions (the protagonist
  can own and can be owned). In scope confirmed; arc structure TBD.
- N-Q10. Transformation — magical, alchemical, curse-driven body
  changes (gender, ancestry, partial). Scope and reversibility?
- N-Q11. Rituals with intimate components — Calistria/Lamashtu/etc.
  rites modeled at full fidelity?
- N-Q12. Public/private behavior model — NPCs react to public
  intimacy by faction/region; this implies a "social rules" sim.
- N-Q13. Asset-generation pipeline policy — confirm every generated
  asset (image, model, animation, voice, text) flows through an
  age-verification filter at generation time.
- N-Q14. "Romantic but not sexual" arcs — first-class supported
  alongside explicit ones?
- N-Q15. Trauma response modeling — mechanical and narrative aftermath
  of dark scenes (PTSD-like conditions, recovery arcs, support NPCs)?
