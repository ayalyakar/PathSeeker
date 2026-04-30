# DESIGN — Survival and Body Needs

> Living document. Hunger, thirst, fatigue, sleep, hygiene, temperature,
> disease, and the survival-sim layer drawn from Project Zomboid + RDR2.

---

## 1. Stance

The body has needs. Ignored long enough, they degrade performance
and ultimately health. Survival systems are **simulated, not gimmicky**
— modeled at granularity that rewards attention without becoming a
constant chore.

## 2. Tracked Needs (proposed)

| Need | Effect when low | Recovery |
|---|---|---|
| Hunger | Fatigue, attribute penalty | Eat |
| Thirst | Fatigue, faster than hunger | Drink |
| Sleep | Cognitive penalty, mood drop | Rest in bed |
| Hygiene | Social penalty, smell-NPC reaction | Bathe |
| Temperature | Damage at extremes | Clothing, fire, shelter |
| Bowel/Bladder | Discomfort, social penalty | Toilet |
| Sexual release | Mood drift, NSFW arousal accumulation | Per *NSFW* |
| Disease | PF2e disease tracks | Medicine, magic |
| Injury | Per *Body and Identity* | Treatment |

## 3. Granularity

- Foreground (player) — full tracking with periodic reminders.
- Background (NPCs at NPC-Q tier) — simplified or summarized.

## 4. Cross-References

- *Body and Identity* — body state.
- *NPCs and Companions* — NPC need behavior.
- *Crafting* — cooking, brewing.
- *World Simulation* — weather/temperature.
- *Magic* — magical sustenance (*create food and water*, *prestidigitation*).
- *NSFW* — sexual release as need.

## 5. Open Questions (Survival and Body Needs-Local)

- ~~**SU-Q1**~~ **Resolved.** **Project-Zomboid harsh** —
  unforgiving need pace; ignored needs cause real degradation;
  survival management is a real layer of play, not a chore-token.
  Magical bypass (*create food and water* etc.) remains available
  but expensive — see SU-Q11.
- **SU-Q2** Surfacing — explicit bars, audio cues, NPC complaints,
  body animation only?
- **SU-Q3** Nutrition variety — different foods give different
  buffs?
- **SU-Q4** Spoilage — food rots over time?
- **SU-Q5** Hygiene NPC reactivity intensity?
- **SU-Q6** Bathing as activity — first-class scene with NSFW
  potential?
- **SU-Q7** Toilet need — modeled, abstracted, ignored?
- **SU-Q8** Sleep mechanics — partial sleep penalty, dream sequences
  (per a future *Dreams* doc)?
- **SU-Q9** Climate damage — Cold, Heat ranges, gear interaction?
- **SU-Q10** Disease tracking — PF2e RAW disease + new ones?
- **SU-Q11** Magical bypass — *create food and water* trivializes;
  policy?
- **SU-Q12** Camping — full system per TR-Q18?
- **SU-Q13** Pregnancy nutritional / sleep effects (BI-Q13)?
- **SU-Q14** Drug withdrawal (per *Drugs and Substances*)?
- **SU-Q15** Withdrawal from other addictions (sexual, magical)?
- **SU-Q16** NPC needs — same architecture, simpler tracking?
- **SU-Q17** Companion need management — NPCs eat from shared
  ration, complain when out?
- **SU-Q18** Disability and impairment — long-term injury effects
  modeled?
- **SU-Q19** Aging effects on need pace (BI-Q31)?
