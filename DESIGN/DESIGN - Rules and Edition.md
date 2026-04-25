# DESIGN — Rules and Edition

> Living document. Defines the host ruleset, the conversion stance toward
> other editions, and the content surface area the game is responsible for.

---

## 1. Primary Ruleset

**PF2e Remaster.** All rules, content, items, ancestries, classes, feats,
spells, and creatures from older editions (PF1e, pre-Remaster PF2e) and
third-party sources are **converted thoroughly to PF2e Remaster** before
they enter the game. There is no parallel rule engine.

Rationale:
- Single source of truth for the rules engine.
- Remaster is the cleanest, most internally consistent, and most legally
  open (ORC) baseline.
- Conversion is a one-time content-pipeline cost; runtime stays simple.

## 2. Variant Rules Baseline

**TBD.** To be disclosed/decided later. Likely candidates that need a
yes/no/default-on/default-off determination:

- Free Archetype
- Automatic Bonus Progression
- Proficiency Without Level
- Stamina
- Gradual Ability Boosts
- Ancestry Paragon
- Dual-Class
- Variant Recall Knowledge / Skill rules

See *Open Questions*.

## 3. Faithfulness Stance

**Mostly RAW, adapted for first-person real-time gameplay.**

The translation rules (in priority order):

1. **Outcome fidelity over mechanic fidelity.** The PF2e turn-based
   3-action economy becomes a real-time Souls-like (see *Combat*); what
   matters is that the *distribution of outcomes* — hits, crits, conditions,
   resource depletion — feels mathematically faithful to PF2e.
2. **Preserve the math.** Proficiency + level + bonuses, AC vs attack,
   crit thresholds, save DCs, spell incapacitation traits — these are
   sacred. UI converts player input to dice rolls under the hood.
3. **Preserve named effects.** A *fireball* is a fireball; a *frightened 2*
   is frightened 2; conditions, traits, and spells keep their names and
   text-described behavior so players who know PF2e are fluent immediately.
4. **Adapt action economy.** The 3-action turn becomes stamina/cooldown/
   queued-action shaped to real-time. Reactions become real-time interrupts.
5. **Cut where required.** Out-of-combat skill rolls, downtime, exploration,
   and crafting use PF2e tables but are surfaced as game-systems
   (cf. *Downtime*, *Crafting*, *Exploration*).
6. **House-rule transparently.** Anywhere we deviate, the deviation is
   logged in a `Houserules` registry the player (and modders) can inspect.

## 4. Content Scope

### 4.1 First-Party (Paizo) — In Scope

- All **Adventure Paths** (every AP, Remastered or Remaster-converted).
- All **Adventure Modules** (one-shots and standalones).
- All **Pathfinder Society Scenarios**.
- **Iconic Heroes** (as canonical NPCs, recruitable, encounterable, etc. —
  full integration; see *NPCs and Companions*).
- **Pathfinder Second Darkness** — fully integrated.
- **Adventure Card Game (ACG)** — fully integrated (likely as a meta-system,
  in-world minigame, or content-data source; mechanism TBD).
- All **Bestiary** content, all rulebooks (Player Core, GM Core, Monster
  Core, all Lost Omens, all Player/GM splatbooks).

### 4.2 Third-Party — In Scope

- Third-party **quests, modules, and content** are integrated where
  legally and thematically feasible.
- Third-party rules supplements are converted to Remaster baseline.
- Conversion priority and source list: TBD.

### 4.3 Out of Scope (For Now)

- **Starfinder** — explicitly deferred. Possible far-future integration.

### 4.4 Original Content

In addition to canonical content, the game includes **thousands** of:

- Original main and side quests,
- Procedurally generated quests / activities,
- Sandbox emergent activities (work, hobbies, crime, romance, study,
  travel, tournaments, festivals, etc.),
- Smaller daily-life "tasks" comparable to *Sims*/RDR2 ambient activities.

This implies a **quest authoring + procgen system** that handles both
hand-authored and runtime-composed content uniformly. See *Quests and
Activities* (TBD).

## 5. Setting

- **Golarion canonical**, with **heavy rework on selected lore and
  meta-world elements**.
- Specific reworks: TBD; will be tracked in `DESIGN - Lore Reworks.md`
  once we begin enumerating them.
- The **Magic system** is one of the called-out reworks: less esoteric,
  more alchemical/rational. See *Magic*.

## 6. Conversion Pipeline (Implied)

Because "all content from all editions converted to Remaster" is a
massive undertaking, a tooled pipeline is non-negotiable:

- **Source tier**: raw rulebook ingest (text/structured).
- **Canonical tier**: Remaster-shaped JSON/SQLite records.
- **Runtime tier**: game-loadable data with effect graphs.
- **Diff tier**: a record of every conversion choice, reviewable.

Tech choices for this pipeline: see *Tech and Engine* (pending Q30–Q44).

## 7. Cross-References

- Combat translation → *Combat*.
- Magic rework → *Magic*.
- NSFW additions to rules (corruption, fertility, etc.) → *NSFW*.
- Quest authoring → *Quests and Activities* (TBD).

## 8. Open Questions (Rules-Local)

- R-Q1. Variant rules baseline (Free Archetype etc.) — full enumeration.
- R-Q2. Treatment of pre-Remaster spells/feats that were *removed* in
  Remaster (e.g., alignment-based spells): convert, drop, or rework?
- R-Q3. Alignment system — Remaster removed alignment as a mechanical
  axis. Confirm we follow Remaster (no alignment) vs reintroduce it as
  flavor or as a *corruption/devotion* axis tied to NSFW/faction systems.
- R-Q4. Multiclassing model: archetype-only (Remaster default) or
  expanded (gestalt/dual-class) variant?
- R-Q5. Level cap: 20 RAW, 25/30 mythic-extended, or uncapped via
  endless-progression systems borrowed from Disgaea-style depth?
- R-Q6. Mythic rules (when published / if used) — in scope?
- R-Q7. Third-party publishers prioritized for conversion (Battlezoo,
  Roll For Combat, Paizo Fans United, etc.).
- R-Q8. Are *legacy* (pre-Remaster) APs converted to Remaster rules and
  also have their *story* modernized (Remastered AP releases) or kept
  in original story shape?
- R-Q9. Is Society Scenario play modeled as in-world Pathfinder Society
  membership/quests, or as a meta layer?
