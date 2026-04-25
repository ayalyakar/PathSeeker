# DESIGN — Factions and Reputation

> Living document. The faction graph: organizations the player can
> join, support, oppose, infiltrate, lead, or destroy; and the
> reputation system that tracks the player's standing with each.
>
> Coupled to *NPCs and Companions* (faction NPCs), *World Simulation*
> (faction goal advancement), *Religion and Devotion* (religious
> orders as factions), *Crime and Justice* (criminal gangs as
> factions), *Quests and Activities* (faction quests).

---

## 1. Stance

Factions are **first-class actors in the simulation**. They have
goals, resources, NPCs, territory, and inter-faction relationships.
Reputation is **per-faction, per-region, and per-NPC** — stratified.

No alignment-coded faction logic (per R-Q3); factions cohere around
**values**, **edicts**, **interests**, and **history**.

## 2. Faction Anatomy

```
Faction
├── identity (name, sigil, creed, region(s))
├── values (what we stand for)
├── edicts (what we require of members)
├── anathema (what we forbid)
├── goals (current objectives)
├── resources (money, influence, NPCs, holdings)
├── NPCs (members, ranked)
├── territory (regional presence)
├── relationships (alliances, rivalries, enmities with other factions)
└── history (past events affecting the present)
```

## 3. Player Reputation

Reputation has multiple axes per faction:
- **Standing** (hostile … unknown … aware … trusted … favored … leader).
- **Notoriety** (how visible the player is to this faction).
- **Trust per officer** (some NPCs in the faction trust the player
  more than the faction at large).
- **Public vs hidden** (a player might be a secret Aspis agent and
  a public Pathfinder).

## 4. Cross-References

- *NPCs and Companions* — faction members.
- *World Simulation* — faction goal tick.
- *Religion and Devotion* — religious factions.
- *Crime and Justice* — criminal factions, guard factions.
- *Quests and Activities* — faction quests.
- *Lore Reworks* §3 / LR-Q17–LR-Q19.

## 5. Open Questions (Factions and Reputation-Local)

- **FR-Q1** Faction count target — major canonical (~30), expanded
  (~100s), per-region exhaustive (~1000s)?
- **FR-Q2** Per-faction depth — full anatomy (§2) for all, or tiered?
- **FR-Q3** Standing model — numeric, discrete, both?
- **FR-Q4** Notoriety vs standing — separate axes?
- **FR-Q5** Faction membership exclusivity — can the player be a
  Pathfinder and a Hellknight at once? An Aspis agent and a
  Society member (only with deception)?
- **FR-Q6** Faction rank progression — internal advancement quests?
- **FR-Q7** Faction leadership — can the player become leader?
  Reform a faction? Start a new one?
- **FR-Q8** Faction destruction — can the player destroy a faction?
- **FR-Q9** Inter-faction tick — alliances and wars develop in the
  simulation (per WS-Q14)?
- **FR-Q10** Faction NPCs — same brain as other NPCs (per *NPCs*)
  with extra role state?
- **FR-Q11** Faction-affiliated insignia, uniforms, codewords —
  diegetic clothing/identity (per *Body and Identity* BI-Q26)?
- **FR-Q12** Reputation discovery — does the player see a "standing
  meter" or only emergent NPC reactions?
- **FR-Q13** Reputation events — what specifically affects
  standing? (Quest completion, killing, gifts, betrayal, recruitment,
  attendance at faction event, …)
- **FR-Q14** Per-region reputation — is "Pathfinder Society" a
  single faction, or one per lodge?
- **FR-Q15** Guilds (smiths, alchemists, scholars, courtesans,
  thieves) — modeled as factions?
- **FR-Q16** Noble houses — factions?
- **FR-Q17** Secret societies — modeled with hidden membership?
- **FR-Q18** Pathfinder Society Scenarios (R-Q9) — handled here?
- **FR-Q19** Iconic Heroes' faction affiliations (NPC-Q17) — tracked?
- **FR-Q20** Cross-AP faction continuity — when an AP advances a
  faction's state (e.g., the Eagle Knights post-Hell's Rebels), does
  the simulation honor that?
