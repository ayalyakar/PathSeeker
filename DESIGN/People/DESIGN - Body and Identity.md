# DESIGN — Body and Identity

> Living document. The "story-state body" system from *NSFW* §5.1, made
> general: how every body in the game (the protagonist's, every NPC's)
> tracks its current state and how that state changes through play.
>
> Coupled to *NSFW*, *Survival and Body Needs*, *Romance and
> Relationships*, *Crafting* (clothing, body mods), *Magic*
> (transformations), and *Animation Pipeline* (visible state).

---

## 1. Stance

A body in this game is not a static avatar. It accumulates marks from
play:

- **Fitness state** (athletic ↔ soft ↔ frail).
- **Weight** (lean ↔ average ↔ heavy).
- **Skin condition** (pale, tanned, freckled, scarred, sunburned,
  bruised, dirty, oiled, sweaty).
- **Hair** (length, color, style, growth, removal).
- **Wounds and scars** (per-location, persistent).
- **Tattoos / brands / piercings / scarification** (player-chosen
  or inflicted).
- **Intimate state** (arousal, post-coital marks, residue, soreness,
  contraceptive status, fertility cycle position, pregnancy state,
  lactation state, sexual disease state).
- **Ancestry-modified state** (curses, blessings, transformations,
  partial-form changes).
- **Conditions** (PF2e conditions: sickened, fatigued, drained, etc.,
  but rendered visible where relevant).
- **Adornments** (clothing layered separately, but tracked here for
  state — "wearing the soiled noble's gown for the third day").

This applies to **Gherman** (per V-Q1 / N-Q1) and to **every NPC**
(at fidelity tier per NPC-Q2).

## 2. Visibility and Persistence

- All state is **persistently saved** (per *Save and Persistence*).
- State is **rendered when relevant** — clothing covers most bodies,
  but exposed states (sweaty face, bandaged arm) show through clothing
  at appropriate detail.
- State is **legible to NPCs** — they react to scars, smell, dress,
  visible pregnancy, etc. (NPC-Q27, NPC-Q28).
- State is **legible to the player** via diegetic UI (mirror,
  character sheet, in-bed inspection).

## 3. Per-Tier Fidelity

- **Hero NPCs / protagonist** — full state.
- **Named NPCs** — most state, lower fidelity for cycle/pregnancy
  tracking unless storied.
- **Background and crowd** — visual state only (visible scars,
  weight, dress); no internal state tracked.

## 4. Identity Change

- **Gradual changes** (training, weight, scars, hair growth) emerge
  from play.
- **Sudden changes** (transformation spells, curses, alchemical
  body-mods, surgery, pregnancy → birth) trigger explicit narrative
  beats.
- **Reversible vs permanent** — depends on cause; tracked per
  change.

## 5. Cross-References

- *NSFW* §5.1 — story-state body principle.
- *Survival and Body Needs* — hunger/sleep/temperature inputs.
- *Romance and Relationships* — body-as-relationship-marker.
- *Crafting* — body modification crafting (tattoos, piercings,
  alchemical body changes).
- *Magic* — transformation spells, contraceptive magic.
- *Animation Pipeline* — visible expression of state.
- *NPCs and Companions* — NPC body tracking.

## 6. Open Questions (Body and Identity-Local)

### Schema

- **BI-Q1** State schema — single flat record per body, or composed
  from independent subsystems (skin, hair, wounds, intimate, …)?
- **BI-Q2** Persistence granularity — per-pixel scarring locations,
  per-location-region (left forearm, right thigh), per-zone (torso,
  legs, head), simpler?
- **BI-Q3** State graph for "transformations" — reversible tagging,
  layer stack, replacement?

### Visible rendering

- **BI-Q4** How does the renderer surface state? Texture-blend layer,
  decal system, per-region mesh swap, hybrid?
- **BI-Q5** Clothing-vs-body interaction — what bleed-through?
- **BI-Q6** Wet/dry/sweaty/bloody/dirty as a global "surface state"
  pass?
- **BI-Q7** Real-time pregnancy belly progression (per RR-Q5 / N-Q3)
  — pregnancy as a 9-month timeline, modeled how?

### Wounds / scars

- **BI-Q8** Wound model — per-location HP, location-specific
  effects?
- **BI-Q9** Scar formation — every wound that heals leaves a mark,
  or only those above a severity threshold?
- **BI-Q10** Healing rate by treatment — magical, mundane, herbal?
- **BI-Q11** Amputation — possible? Prosthesis system?

### Intimate state

- **BI-Q12** Fertility cycle for female-bodied — modeled in detail
  (ovulation window, contraceptive interaction)?
- **BI-Q13** Pregnancy stages — visible, mechanical, gameplay-affecting
  per-trimester?
- **BI-Q14** Lactation — induction, maintenance, drying-up?
- **BI-Q15** STDs / curses (per N-Q5) — symptomatic stages?
- **BI-Q16** Arousal as a tracked state — affects dialogue,
  decisions, NPC reactivity?
- **BI-Q17** Post-coital marks (per BI-Q4) — visible, time-decaying?

### Adornment

- **BI-Q18** Tattoo system — design tool? Catalog of designs?
  Inflicted via NPC slavery (per N-Q9)?
- **BI-Q19** Piercings — multiple slots, swappable jewelry, magical
  socket items?
- **BI-Q20** Hair — length grows over in-game time; haircuts as
  activities?
- **BI-Q21** Beard / body hair (Gherman is male, age 21 — body hair
  grows; shaving routine as activity?)?

### Identity beyond body

- **BI-Q22** Names — known-by-others, aliases, false identities,
  legal name vs in-use name?
- **BI-Q23** Reputation as identity — does Gherman accumulate
  monikers ("the One Who Bleeds Slowly", "Liar of Korvosa")?
- **BI-Q24** Disguise — as a system (changing how NPCs identify
  Gherman)?
- **BI-Q25** Class identity — does the player declare "I am a
  fighter" in-fiction, or is class implicit-from-actions?
- **BI-Q26** Faction identity — wearing the Hellknight insignia
  is a different identity than not wearing it?

### Transformation

- **BI-Q27** Magical transformations (polymorph, baleful,
  *true reincarnation*, druidic wild shape) — temporary, persistent,
  permanent buckets?
- **BI-Q28** Alchemical body modifications — elixirs, mutagens,
  permanent procedures?
- **BI-Q29** Curses that reshape the body — first-class system
  (Lamashtu, Urgathoa contexts)?
- **BI-Q30** Reversal — universal "remove curse" / "restoration" /
  "regenerate" RAW interactions?

### Ageing

- **BI-Q31** Ageing per ancestry — humans age vs elves don't (in
  meaningful timeframes)?
- **BI-Q32** Visible ageing — wrinkles, gray hair, posture?
- **BI-Q33** Death-from-age (mirrors L-Q7).
