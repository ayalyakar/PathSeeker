# DESIGN — Save and Persistence

> Living document. The auto-save model, the immutable-history rule,
> save migration, crash tolerance, and what exactly gets serialized.
>
> Constrained by *Core Loop and Structure* §6 (auto-saves only, no
> rewriting history, fresh world per save).

---

## 1. Stance

- **Auto-saves only.** No manual save-scumming.
- **History is preserved.** The player cannot rewrite what they did.
- **Fresh world per save** (resolved L-Q4): each new game spawns a
  fresh Golarion; no cross-save persistence.
- **Crash-tolerant.** The save system must survive process death at
  any moment without corrupting state.
- **Forward-compatible.** Schema migrations must work; saves from
  early dev should remain loadable.

## 2. What Gets Saved

Everything that matters in the simulation:

- Protagonist state (Gherman's stats, body state, inventory,
  conditions, learned spells, prepared spells, focus, currency,
  marks, scars, tattoos, intimate state).
- Every NPC's state (location, schedule offset, mood, memory,
  relationships, body state, alive/dead, inventory).
- World state (calendar, weather, faction goals, AP progression,
  market prices, ecology populations).
- Active combat / scene state (mid-combat saves must be possible).
- Quest state (started, branched, completed, failed).
- Reputation, factions, crime, justice.
- Save metadata (playtime, location, screenshot, signature).

## 3. What Does NOT Get Saved

- Loaded asset data (regenerated on load).
- LLM prompt caches (regenerated).
- Procedural seeds for **already-rendered** chunks (rendering is
  deterministic from the seed).

## 4. Save Layout (proposed)

```
%APPDATA%/PathSeeker/Saves/
└── slot_<NNN>/
    ├── meta.json                  (slot metadata, screenshot path)
    ├── world.sqlite               (canonical world state)
    ├── npcs.sqlite                (NPC state, can be sharded)
    ├── memory.sqlite              (per-NPC memory log)
    ├── history.log                (immutable append-only event log)
    └── snapshots/
        ├── chapter_001.snap       (chapter-end hard snapshots)
        └── ...
```

(Per Windows-only target.)

## 5. Save Cadence (proposed; pending L-Q3)

Layered:

1. **Continuous in-memory journal.** Every state change is logged
   in-memory; a background task flushes to disk every ~30 seconds and
   on key events (zone entry/exit, scene completion, level-up, death,
   intimate scene boundaries, AP chapter transitions).
2. **Rolling auto-snapshot.** A full-state SQLite checkpoint every
   ~5 in-game minutes (~37.5 real seconds at 1:7.5 ratio) — pending
   tuning.
3. **Hard snapshots** at chapter boundaries (project-management /
   recovery).

## 6. Immutable History

- The `history.log` is append-only.
- When the player makes a decision, the decision is logged with a
  monotonic event ID, an in-game timestamp, and the consequences.
- Loading an autosave **rewinds the world state** to that point but
  does **not erase the log** of what happened beyond it (the log
  retains the "alternative history that did happen" for diegetic
  use — e.g., divinations may reveal prior timeline branches if the
  game ever surfaces this).

This is a strong stance — it means save-load isn't a conventional
"undo." The player is repositioned in time, not in memory.

(Pending SP-Q3 confirmation; the user may want classical save/load
semantics where loading wipes log forward of save.)

## 7. Crash Tolerance

- Mid-combat: combat-step transactions must commit per micro-action.
- Mid-scene (especially intimate scenes): scene state must be
  recoverable.
- Mid-pipeline (background world tick): world tick must be
  transactional.
- A save that's been written halfway must be rejected at load time
  with a fall-back to the previous good snapshot.

## 8. Save Migration

When the schema evolves (new fields, renamed fields, refactored
subsystems), the loader must transform old saves to the new shape.

- Schema versioning per table.
- Migration scripts in `Engine/Save/Migrations/`.
- Tests run all known historic save formats through the loader on CI.

## 9. Cross-References

- *Core Loop and Structure* §6 — high-level save policy.
- *Tech and Engine* §3 — runtime data architecture.
- *World Simulation* — what tick state needs serializing.
- *NPCs and Companions* — NPC memory storage.
- *Performance Budget* — save/load latency budget.

## 10. Open Questions (Save and Persistence-Local)

### Format

- ~~**SP-Q1**~~ **Resolved (assistant pick: "best option").** Option
  (d) **mixed: SQLite for the big save tables (world, NPCs, memory,
  history) + sidecar JSON for slot metadata** (screenshot path,
  display name, playtime). Rationale: SQLite for ACID/queryable
  bulk; JSON metadata so the slot list can render without opening
  the SQLite file.

### Cadence

- **SP-Q2** Auto-save cadence and triggers — confirm §5 or revise.
- **SP-Q3** History semantics — confirm §6 (log preserved across
  loads) or use classical "load wipes future" semantics.

### Slots

- **SP-Q4** Slot count — single slot per playthrough, multiple slots,
  unlimited?
- **SP-Q5** Save naming — by chapter, timestamp, location, player-named?
- **SP-Q6** Cloud sync (Steam Cloud, manual)? (Probably moot per Q34
  Windows-only personal project, but worth confirming.)

### Crash recovery

- **SP-Q7** Recovery flow when last autosave is corrupted — fall back
  to previous snapshot, prompt the user, attempt repair?
- **SP-Q8** "Crash report" capture for dev-time diagnosis.

### Migration

- **SP-Q9** Migration policy — auto-migrate silently, prompt user,
  refuse old saves?
- **SP-Q10** Test corpus — how do we maintain a library of historic
  saves to migration-test against?

### Performance

- **SP-Q11** Save/load latency budget — what's the max acceptable
  freeze frame on save trigger?
- **SP-Q12** Asynchronous save — is in-game time paused during save,
  or does play continue?
- **SP-Q13** Save file size budget — at what point do we worry about
  multi-GB saves?

### Scene-specific

- **SP-Q14** Intimate-scene state — saved with full scene continuation
  capability, or scene-end-only commits?
- **SP-Q15** Combat state — full mid-swing recovery, or
  end-of-encounter-only commits?
- **SP-Q16** Long-running activities (multi-day crafting, gestation,
  prison sentences, voyages) — saved as deferred events vs ticked
  forward?

### Diegetic interactions

- **SP-Q17** Does the game ever **mention** to the player that they
  reloaded? (Per "no rewriting history," divinations or NPCs might
  reference past timelines if the player loads — or not.)
- **SP-Q18** "Death" recovery — when Gherman dies and resumes via
  capture/revival/comatose-recovery, what state is rolled back?

### Edge cases

- **SP-Q19** New Game over an existing slot — explicit confirmation,
  delete old, archive?
- **SP-Q20** Crashing during save itself — atomic write protocol
  (write to .tmp, rename)?
- **SP-Q21** Anti-tamper / save signing — irrelevant for personal
  use, or worth doing for our own sanity?
- **SP-Q22** Mod-affected saves — when a content plugin is loaded,
  unloaded, or changed, what happens to dependent state?
