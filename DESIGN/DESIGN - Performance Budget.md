# DESIGN — Performance Budget

> Living document. Frame-rate targets, GPU/CPU/RAM budgets, NPC count
> ceilings, simulation tick budget, asset memory caps, save load times.
> Centralizes the constraints that everything else must respect.

---

## 1. Stance

Personal Windows-only target (Q34) gives us a single hardware
profile to optimize for, but the game is ambitious enough that
budgets must be explicit, not implicit.

## 2. Targets (proposed; pending PB-Q1+)

| Target | Value (proposed) |
|---|---|
| Resolution | 1440p (2560×1440) baseline; 4K aspirational |
| Framerate | 60 fps stable; 30 fps minimum |
| Active NPCs on screen | 30 (full-fidelity) + 100 (background LOD) |
| Region NPC pool simulated | 1,000+ |
| World NPC pool tracked | 10,000+ |
| RAM working set | 16 GB |
| VRAM working set | 12 GB |
| Disk save size | < 200 MB |
| Save commit latency | < 200 ms (background); < 1 s (foreground) |

## 3. Cross-References

- *Tech and Engine* T-Q4 (hardware floor).
- *World Simulation* — tick budget.
- *NPCs and Companions* — count budget.
- *Animation Pipeline* — per-character cost.
- *Audio* — voice line memory.
- *Save and Persistence* — save IO budget.

## 4. Open Questions (Performance Budget-Local)

- **PB-Q1** Hardware floor (mirrors T-Q4) — what's the minimum
  spec we target?
- **PB-Q2** Framerate target — 60 fps strict or 30 fps acceptable?
- **PB-Q3** Resolution target — 1440p, 4K, both?
- **PB-Q4** GPU budget split — character vs environment vs UI vs
  post?
- **PB-Q5** CPU thread plan — main, render, audio, sim, IO,
  remainder?
- **PB-Q6** RAM/VRAM ceilings.
- **PB-Q7** Simulation tick frame budget — % of frame for L0,
  per-frame budget for L1/L2/L3/L4 (per WS-Q1)?
- **PB-Q8** Asset streaming bandwidth — disk read/sec targets?
- **PB-Q9** Save IO budget (mirrors SP-Q11).
- **PB-Q10** Voice cache size budget (mirrors AU-Q14/15).
- **PB-Q11** When over budget, what degrades first? (NPC fidelity,
  shadow quality, distance tier, animation rate, …)
- **PB-Q12** Profiling tooling — Godot built-ins, RenderDoc, custom
  in-engine HUD?
- **PB-Q13** Performance regression tracking — automated test scene?
