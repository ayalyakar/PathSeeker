# DESIGN — World Simulation

> Living document. The tick model, time, weather, ecology, faction-event
> propagation, and the LOD strategy that keeps Golarion alive even when
> the player isn't looking.
>
> Load-bearing for the Vision pillar of "fully complex and simulated
> lifelike world."

---

## 1. Stance

The world **runs whether or not the player is in the room**. Every
decision in this doc serves three pillars:

- **Continuity** — the world has memory and momentum. NPCs go to bed
  whether or not we're watching; markets shift; battles end; rumors
  spread.
- **Plausibility** — events emerge from rules and state, not from
  scripted-in-front-of-the-player triggers.
- **Affordability** — we can't run RDR2-density simulation on every
  NPC in every region simultaneously. LOD is mandatory.

The simulation is a **layered tick** with multiple frequencies and
fidelities. Foreground (player-attended) ticks are dense and
high-resolution; background (off-screen) ticks are coarse summaries.

## 2. Time Model (recap from *Core Loop and Structure*)

- **1 in-game day = 3 real-time hours.**
- Time scaling during combat / intimate scenes: pending L-Q1.
- Day/night, calendar (Absalom Reckoning), holidays, seasons all
  modeled.
- Long activities and time-skips evaluate the world forward N hours.

## 3. Tick Layers (proposed; pending WS-Q1)

| Layer | Tick rate | Fidelity | Used for |
|---|---|---|---|
| **L0 Player-attended** | Every game frame | Full physics, full AI | Active scene, current zone |
| **L1 Same-zone off-camera** | ~1 Hz | Behavior trees, no physics | Zone NPCs, ambient events |
| **L2 Same-region** | Every in-game minute | Coarse goals + schedules | Town residents off-zone |
| **L3 Same-continent** | Every in-game hour | Aggregate events | Distant NPC summaries |
| **L4 World** | Every in-game day | Macro events | Faction shifts, war fronts, prices |

When the player travels to a region, the simulation **promotes** its
NPCs from a lower tier to a higher one and reconciles state.

## 4. Subsystems

### 4.1 NPC Schedules

See *NPCs and Companions* for the full design. The simulation
provides the **tick pulse** that drives schedule advancement.

### 4.2 Weather

- Regional climate model.
- Diurnal and seasonal variation.
- Stochastic weather events (storms, droughts, magical anomalies).
- Affects travel, NPC moods, agriculture, festivals.

### 4.3 Ecology and Wildlife

- Animal populations, migration, hunting pressure.
- Predator-prey interactions.
- Plant growth (relevant to alchemical reagent sourcing per *Magic*).

### 4.4 Economy Tick

- Markets shift prices over time and per region.
- Trade routes carry goods.
- Wars and disasters disrupt supply.
- See *Economy*.

### 4.5 Faction Events

- Faction goals advance over time.
- Conflicts escalate or de-escalate.
- Major NPCs make decisions.
- News and rumors propagate (region-by-region speed).
- See *Factions and Reputation*.

### 4.6 Adventure-Path Triggers

- APs fire their canonical events on Golarion calendar dates (or per
  player progression — see Q-Q questions).
- Multiple APs may run concurrently; the simulation tracks them all.

### 4.7 Quasi-Permadeath of NPCs

- NPCs can die from causes the player is unaware of (combat,
  accident, age — pending L-Q7).
- Dead NPCs stay dead; their roles may be filled by successors.

## 5. Cross-References

- *Core Loop and Structure* — time scaling, save model.
- *NPCs and Companions* — the actors the simulation drives.
- *Factions and Reputation* — faction dynamics tick.
- *Economy* — economic tick.
- *Travel* — travel through simulated terrain.
- *Performance Budget* — what the simulation can afford.
- *Save and Persistence* — serializing world state.

## 6. Open Questions (World Simulation-Local)

### Tick architecture

- ~~**WS-Q1**~~ **Resolved.** **Hybrid: single global tick + LOD-tiered.**
  L0 (player-attended) and L1 (same-zone-off-camera) drive off the
  global tick; L2/L3/L4 (region/continent/world) run on coarser
  derived sub-ticks. The §3 layered model is preserved; the global
  tick is the master clock.
- **WS-Q2** Off-screen NPC simulation depth — full schedule + memory
  vs summarized + reconstructed when the player approaches?
- **WS-Q3** Determinism — is the simulation deterministic given the
  same seed (helpful for debugging) or stochastic-in-RNG?
- **WS-Q4** Multi-thread the simulation tick? (Important for
  performance; complicates state.)

### Time

- **WS-Q5** When does the simulation pause? Menus? Inventory? Map?
  (Mirrors L-Q8.)
- **WS-Q6** Time-skip evaluation — for a 1-week skip, do we tick
  forward 1 week of L4 events, or compute summary?
- **WS-Q7** Player asleep / unconscious — does simulation continue
  in real-time or jump?

### Weather and ecology

- **WS-Q8** Climate model fidelity — per-tile, per-region, per-zone?
- **WS-Q9** Magical weather (Worldwound, Numerian alien storms,
  planar incursions) modeled as climate events?
- **WS-Q10** Wildlife respawn — Bethesda-style respawn timer, or
  fully simulated populations that can be hunted out?
- **WS-Q11** Plant/reagent regrowth modeled (since reagents matter
  per *Magic* §1.1)?

### Economy / faction

- **WS-Q12** Market price model — supply/demand simulation, or
  scripted regional prices with shocks?
- **WS-Q13** War simulation — abstract attrition, or full Mass-Combat
  battles auto-resolved when the player isn't there?
- **WS-Q14** Faction goal model — explicit `goal:` lists with progress
  meters, or emergent from NPC desires?

### News and rumor

- **WS-Q15** Rumor propagation model — graph-based, distance-based,
  faction-network-based?
- **WS-Q16** "News value" — does the simulation classify events as
  important enough to spread, and how?
- **WS-Q17** Player-affecting rumor floor — does the player ever
  meet an NPC who says "I heard you slew the dragon at X"?

### Adventure paths

- **WS-Q18** AP triggers — fire on calendar date, on player level, on
  player location, on player declared interest, or hybrid?
- **WS-Q19** AP NPCs that should be alive at chapter 5 — does the
  simulation protect them from tier-1 death-by-accident?
- **WS-Q20** Concurrent AP handling — what if two APs need the same
  NPC alive on the same date?

### Hooks

- **WS-Q21** Player-perceptible signals — do players see weather
  forecasts, faction news boards, market reports? Diegetic UI surfaces?
- **WS-Q22** Debug overlay for simulation state (dev-time only).

### Edge cases

- **WS-Q23** Magical effects that warp time (haste, slow, time stop,
  time travel) — simulation handling?
- **WS-Q24** Planar travel — does each plane have its own
  simulation, or is the player "frozen" in Golarion time?
- **WS-Q25** Player-induced apocalypse — what if the player wipes
  out a town or causes a war? Simulation must handle drastic state
  shifts cleanly.
