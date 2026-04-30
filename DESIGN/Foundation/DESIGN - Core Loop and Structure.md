# DESIGN — Core Loop and Structure

> Living document. Defines the macro-structure, time, party model, save/death
> philosophy, and progression breadth.

---

## 1. Macro Structure

**Open-world life-sim**, advanced and reworked beyond existing references.

The closest reference points are:
- *The Sims* (granular daily-life systems),
- *Project Zomboid* (consequence-density and survival-grade simulation),
- *Red Dead Redemption 2* (NPC schedules and ambient world reactivity),
- *Persona* (calendar and social-link cadence),
- *Daggerfall* (open-world scale)

…all hosted inside **Golarion**, with all the dungeon-crawling, AP-running,
combat, magic, and adventuring of a Pathfinder game layered on top.

The player is **not required to adventure**. They can spend a year as a
blacksmith's apprentice, a courtesan, a scholar at the Magaambya, a
fisherman in Shoanti country, or a thief in Absalom — and the world will
continue to live around them.

## 2. Time

- **Persistent world.**
- **1 in-game day = 3 real-time hours.**
  - 1 in-game hour = 7.5 real-time minutes.
  - 1 in-game minute = 7.5 real-time seconds.
- The world clock advances even when the player is sleeping/resting/idle
  in a safe location; combat and tense scenes use a faster, more granular
  tick (TBD — likely 1:1 real-time during action).
- NPCs run **24 in-game hours of schedule**: sleep, work, meals, travel,
  social, leisure, rituals.
- Calendar follows Golarion's **Absalom Reckoning** (months: Abadius,
  Calistril, Pharast, Gozran, Desnus, Sarenith, Erastus, Arodus, Rova,
  Lamashan, Neth, Kuthona; weekdays: Moonday, Toilday, Wealday, Oathday,
  Fireday, Starday, Sunday).

Implications:
- Travel must be **continuously simulated**, not "fade-to-arrived."
- Long activities (research, crafting, training, pregnancy, sieges) need
  a **time-skip with simulated tick** (process the world forward N hours,
  resolving NPC actions, world events, and player passive activities).
- The player UI needs **clock awareness everywhere** — meeting at dusk
  at the docks must feel like an actual appointment.

## 3. Party

- **Solo PC.** The player controls only the protagonist.
- **Companions are full NPCs** driven by the same simulation/AI layer as
  the rest of the world. They:
  - Refuse, leave, sleep, eat, mourn, train, pursue side-goals.
  - Need to be *convinced* (through play, dialogue, gifts, shared
    experience) to follow the protagonist into specific situations.
  - Can die permanently (see *Death*).
  - Can be encountered as opposition if betrayed/aligned otherwise.
- **No squad-control camera, no companion AI tactics screen.** Companions
  fight as autonomous agents; the player can issue voice/gesture/whistle
  commands (TBD) but cannot pilot them.

## 4. NPC and World Lifelikeness

This is the **highest-investment subsystem** in the project. Reference
ceiling is "Westworld hosts," realistic floor is "Skyrim Radiant + RDR2
ambient drama."

Required pillars (each will get its own design doc):

- **Schedules and routines** — every named NPC has 24h coverage.
- **Memory** — NPCs remember interactions, holdable grudges and affection.
- **Relationships** — NPC↔NPC graph, not just NPC↔player.
- **Goals and desires** — Maslow-ish stack, drives autonomous action.
- **Speech generation** — hand-authored beats + LLM-driven barks/dialogue
  filtered by personality and context (LLM strategy: see *Tech and Engine*).
- **Emotional state** — mood, arousal, fatigue, hunger, intoxication, etc.
- **Reactivity** — to clothing, smell, status, faction, time of day,
  weather, recent events, the player's reputation.

## 5. Death and Failure

- **Death is narrative.** No game-over screen.
  - Protagonist death triggers a *consequence path*: capture, rescue,
    revival (PF2e *raise dead* and similar exist canonically), divine
    intervention with debt, time-skip while comatose, identity loss, etc.
  - Specific consequence depends on context, location, who killed them,
    and faction relationships.
- **Failures have consequences.** A botched heist marks you with the
  guard. A failed romance closes that branch. A botched ritual leaves a
  scar. Nothing is "soft-failed."
- **Companions can die permanently** (subject to PF2e revival options
  available at that level, with cost — body, ritual, gold, time).

## 6. Saves

- **Auto-saves only.** No manual save-scumming.
- **History is preserved.** Players cannot rewrite what they did.
- Save cadence: TBD. Likely a **rolling autosave** (every N minutes or
  on key events) plus **scene-end commits** for important branches.
- A small number of **"hard save" pillars** at chapter/AP boundaries may
  exist for project-management reasons (export, share, recovery).
- Implication: the game must be tolerant to crash and to interruption
  inside long scenes (transactional state).

### 6.1 New Game Semantics (resolved L-Q4)

- **Fresh world per save.** Each new game spawns a fresh Golarion.
- No cross-save persistence; no dynasty-across-runs system; no shared
  world between protagonist generations.
- Gherman is **narratively quasi-immortal** at the macro level —
  failures and severe wounds resolve in-game (capture, scarring,
  comatose recovery, magical revival, divine intervention with cost,
  etc.) but the *world itself* belongs to a single playthrough.
- Implication: no "ancestor mode" or "next generation plays in your
  Golarion" features. The "forever project" is forever in
  *content density*, not in *cross-save persistence*.

See *Open Questions* for crash recovery, multi-character saves, and
save-slot policy. See also *Save and Persistence* for the technical
shape.

## 7. Progression Surfaces

PF2e character level is **one** progression axis among many. Every
listed system is treated with **AP-grade depth** — meaning hand-authored
arcs, faction NPCs, named locations, mechanical rewards, lore.

Non-exhaustive list (each becomes its own design doc when work begins):

- **Downtime crafting** (forge, alchemy, scribing, leatherworking,
  tailoring, cooking, brewing, jewelry, etc.)
- **Romance and relationships** (multi-partner, NPC-driven, sexual and
  non-sexual, time-grown)
- **Faction reputation** (Pathfinder Society, Hellknights, Magaambya,
  Eagle Knights, Aspis Consortium, individual cities, religions, …)
- **Side activities** — full-depth: gambling, hunting, fishing,
  cooking, brewing, dueling clubs, arena, racing, music, painting,
  dance, scholarship, exploration mapping, treasure hunting,
  tournaments, festivals, cults, smuggling, brothel work, court
  intrigue, kingdom-building (Kingmaker), siege warfare (War for the
  Crown), legal cases, journalism, etc.
- **Reputation / infamy** — separate from faction; how the world at
  large speaks of the protagonist.
- **Property and business** — owning, running, expanding.
- **Mounts, animals, familiars** — bonded over time, trainable.
- **Religion / devotion** — divine relationships are persistent.
- **Body** — fitness, scars, tattoos, weight, hair, skin condition,
  piercings, intimate state (see *NSFW*).
- **Knowledge/skill mastery** — beyond proficiency tiers, granular use-
  driven mastery (cf. Daggerfall/Morrowind).
- **Languages** — Pathfinder languages, learnable over time.
- **Legacy** — children, inheritance, dynasties (NSFW-adjacent and
  long-timeline; see *NSFW* and *Open Questions* on aging).

This list is **non-exclusive**: anything that is treated as "mainline"
content in any of our reference games (Sims hobbies, RDR2 chores,
Persona social links, Pillars factions, etc.) is in scope.

## 8. Cross-References

- Combat as one of many activities → *Combat*.
- Magic study, divine devotion → *Magic*, *Religion* (TBD).
- All NSFW progression surfaces are integrated, not siloed → *NSFW*.
- Procedural quest generation → *Quests and Activities* (TBD).

## 9. Open Questions (Loop-Local)

- L-Q1. Time scaling during combat and intimate scenes — 1:1 real-time
  or maintain 1:7.5 ratio?
- L-Q2. Travel: continuous simulation only, or option to "fast-travel
  with time-skip" for known-safe routes?
- L-Q3. Save model details: rolling autosave interval, max slots, named
  branch saves at chapter ends, single canonical save vs many?
- ~~L-Q4.~~ **Resolved.** Fresh world per save; protagonist quasi-
  narratively immortal; failures resolve in-game. See §6.1.
- L-Q5. Speed-up controls — is there a "wait/sleep until" mechanic, and
  what activities qualify as time-skippable?
- L-Q6. Aging: protagonist and NPCs age in real time? On a compressed
  scale? Frozen?
- L-Q7. NPC death from old age, disease, accident — modeled?
- L-Q8. Pause: does the game pause for menus/inventory, or is it always
  diegetic-time?
- L-Q9. Multi-protagonist (current, retired, ancestor) save trees?
