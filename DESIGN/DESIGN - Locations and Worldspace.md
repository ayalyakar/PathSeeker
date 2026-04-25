# DESIGN — Locations and Worldspace

> Living document. How regions, cities, dungeons, wilderness, and
> interiors are authored, streamed, populated, and connected.

---

## 1. Stance

The world is **Golarion canonical at scale** — every named place
from canonical AP coverage at minimum, with thousands of original
locations.

Hierarchy:
- **Continent** → **Region** → **Settlement / Wilderness Zone** →
  **Sub-zone** (district, dungeon, building) → **Room / Outdoor
  Cell**.

## 2. Streaming and LOD

- Player-attended zones load in full.
- Distant regions kept as simulation-only stubs (per *World
  Simulation* L4).
- Travel between zones supports both seamless (where possible) and
  loading-screened (between continents).

## 3. Content Categories

- **Cities** — Absalom, Korvosa, Magnimar, Cassomir, Westcrown, …
- **Towns / Villages**.
- **Dungeons** — every published, plus megadungeons, plus procedural.
- **Wilderness** — biomes, hexes, encounter density.
- **Strongholds / Keeps**.
- **Temples**.
- **Brothels / Bathhouses / Festival Grounds**.
- **Workshops / Guildhalls**.
- **Planes** (per *Planar Travel*).

## 4. Cross-References

- *World Simulation* — population/streaming.
- *Travel* — between locations.
- *Performance Budget* — what fits in memory.
- *Content Pipeline* — location authoring.
- *Lore - <Region>.md* — per-region content.

## 5. Open Questions (Locations and Worldspace-Local)

- **LW-Q1** World scale — true-to-Golarion (~Earth-sized) or
  compressed-for-travel?
- **LW-Q2** Cell vs open-world — Bethesda cells, Daggerfall procedural,
  full open-world (per region), hybrid?
- **LW-Q3** Loading screens — accepted (continent transitions) vs
  zero-tolerance?
- **LW-Q4** Overland map — Pillars-style overland with encounters,
  full-3D walked, both?
- **LW-Q5** Megadungeon support — multi-level streaming?
- **LW-Q6** Procedural dungeon generation — algorithmic, AI-assisted,
  hand-built?
- **LW-Q7** Interior persistence — does dropped trash stay where
  you drop it for months?
- **LW-Q8** NPC home/work persistence — NPCs return home daily; what
  happens if their home burns down?
- **LW-Q9** Building interior fidelity — every door enterable, or
  selective (named-NPC homes only)?
- **LW-Q10** Vertical density — multi-story buildings climbable,
  rooftops accessible (Assassin's Creed)?
- **LW-Q11** Subterranean systems (sewers, Darklands) — full
  navigation?
- **LW-Q12** Map and minimap — diegetic map, modern minimap, none,
  hybrid?
- **LW-Q13** Cartography — does the player draw their own map (Etrian)?
- **LW-Q14** Fast-travel (per L-Q2) — interacts with location system?
- **LW-Q15** Content fill density — every tavern lovingly written,
  or templated taverns with hand-touches?
- **LW-Q16** Iconic location preservation — must Sandpoint always
  match canon imagery, or reworkable?
- **LW-Q17** Original locations — invented by us, integrated into
  canon how?
- **LW-Q18** Region streaming budget (per *Performance Budget*).
- **LW-Q19** Plane streaming (per *Planar Travel*) — completely
  separate worldspace, or shared system?
- **LW-Q20** Destruction — can the player burn down buildings, and
  does the world reflect it permanently?
