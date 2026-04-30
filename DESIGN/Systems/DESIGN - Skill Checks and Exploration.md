# DESIGN — Skill Checks and Exploration

> Living document. Out-of-combat PF2e skills (Acrobatics, Athletics,
> Stealth, Perception, Diplomacy, Crafting, Survival, etc.) translated
> to first-person real-time, plus the exploration / activity layer
> derived from PF2e exploration mode.

---

## 1. Stance

Skills run constantly in the background. The player **acts** in
first-person; the engine **rolls** under the hood and surfaces
outcomes. Dramatic checks may be exposed (per RAW visible DC).

Modes (per PF2e):
- **Encounter mode** → real-time combat (per *Combat*).
- **Exploration mode** → real-time travel through danger.
- **Downtime** → time-skipped activities.

## 2. Skill Translation Examples

| Skill | Real-time mapping |
|---|---|
| **Acrobatics** | Player-input movement (jump, balance, tumble) modified by skill |
| **Athletics** | Climb, swim, force-open inputs gated by skill |
| **Stealth** | Detection model (per WS / NPC) checks Stealth vs Perception |
| **Perception** | Continuous Perception DC against hidden things in environment |
| **Diplomacy / Intimidation / Deception** | Conversation rolls (per *Dialogue*) |
| **Crafting** | Per *Crafting* |
| **Society** | Recall Knowledge for cultural/political topics |
| **Lore (X)** | Per-topic Recall Knowledge |
| **Religion** | Recall Knowledge + ritual + faith interactions |
| **Arcana / Nature / Occultism** | Recall + identification + interaction |
| **Medicine** | Treat Wounds; First Aid; long-term care |
| **Survival** | Tracking, sustenance, navigation |
| **Thievery** | Pick locks, disable devices, sleight-of-hand |

## 3. Cross-References

- *Combat* — encounter-mode handoff.
- *World Simulation* — exploration-mode terrain / NPC perception.
- *Dialogue and Conversation* — social skills.
- *Crafting* — Crafting skill.
- *Travel* — Survival, navigation.
- *Crime and Justice* — Stealth, Thievery, Deception used criminally.

## 4. Open Questions (Skill Checks and Exploration-Local)

- ~~**SK-Q1**~~ **Resolved (mirrors DC-Q2).** **Show numeric DC**
  for major/consequential rolls; **show pass/fail tier** for minor
  rolls. Threshold for "major" is context-driven (named-NPC
  interaction, story-gate skill check, or DC ≥ a tier-defined
  threshold). Hidden rolls are reserved for stealth-specific
  cases where the player not knowing they were rolled-against is
  itself the point.
- **SK-Q2** Recall Knowledge UX — diegetic mental note, journal
  entry, screen prompt?
- **SK-Q3** Continuous Perception model — pulse-checks, persistent
  sense, mixed?
- **SK-Q4** Stealth — line-of-sight + sound + smell + light? How
  many sensory layers do NPCs use?
- **SK-Q5** Skill use timing — instant, action-cost (per *Combat*),
  multi-second? PF2e exploration-activity timings preserved?
- **SK-Q6** Player-input vs skill-roll weight — how much does
  player skill (timing, accuracy) modify the underlying roll?
- **SK-Q7** Trained-only actions (PF2e gating) — UI handling for
  inability to attempt?
- **SK-Q8** Aid action — how does an ally aid in real-time?
- **SK-Q9** Lore proficiencies (sub-skills) — full enumeration as
  separate skills?
- **SK-Q10** Skill challenges (multi-roll set-piece) — modeled as
  scenes (BG3 / Pillars-style)?
- **SK-Q11** Failure consequences — graceful or harsh by default?
- **SK-Q12** Skill use during conversation — can the player
  Athletic-jump out of a window mid-dialogue?
- **SK-Q13** Magical skill enhancement — *guidance*, items,
  potions, mutagens — applied via UI or auto?
- **SK-Q14** Skill increases over time — RAW level-based vs use-
  based mastery (Daggerfall/Morrowind influence)?
- **SK-Q15** Survival — hunting, foraging, weather-reading — full
  systems?
- **SK-Q16** Tracking — visible footprints, scent trails, magical
  detection?
- **SK-Q17** Navigation — compass, stars, landmarks, magical
  divination — surface how?
- **SK-Q18** Treat Wounds in real-time — as an activity with
  visible bandaging animation?
- **SK-Q19** Long-term care — multi-day skill use; downtime?
- **SK-Q20** Society etiquette — checks for "knowing what fork to
  use" at noble dinners?
