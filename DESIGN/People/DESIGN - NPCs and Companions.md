# DESIGN — NPCs and Companions

> Living document. The largest behavioral system in the project: NPC
> brains, schedules, memory, relationships, autonomy, and how
> companions (those NPCs the player adventures with) differ from the
> rest.
>
> Closely coupled to *World Simulation* (the tick), *Dialogue and
> Conversation* (the interface), *Romance and Relationships* (one
> emotional layer), and *Factions and Reputation* (the social graph).

---

## 1. Stance

NPCs are the world. Per *Vision*, the goal is **lifelike, autonomous,
believable** characters — closer to RDR2/Westworld in ambition than
to Skyrim/RDR1.

Operating principles:

- **NPCs run the same simulation regardless of audience.** They
  schedule, eat, sleep, work, court, fight, die whether or not the
  player is in the room.
- **NPC behavior is goal-driven**, not pattern-stamped.
- **NPCs remember.** An NPC the player insults at a tavern remembers
  it next month.
- **NPCs have relationships with each other**, not only with the
  player.
- **Companions are NPCs first.** They follow the player conditionally.

## 2. NPC Types (rough taxonomy, pending NPC-Q2)

| Type | Fidelity | Examples |
|---|---|---|
| **Hero NPC** | Highest — full memory, deep personality, voiced, recurring | Romanceable companions, AP main characters, named iconics |
| **Named NPC** | High — personality, schedule, voice, memory | Quest givers, faction officers, important shopkeeps |
| **Background Named** | Medium — identity, schedule, light memory | Common townsfolk known by name |
| **Anonymous Crowd** | Low — schedule + role, ephemeral memory | Patrons, travelers, generic guards |
| **Critter** | Minimal | Wildlife, pests |

Higher tiers cost more memory, more authoring, more compute. Lower
tiers can promote up to higher tiers when they become relevant
(player names them, becomes friends, etc.).

## 3. NPC Brain (proposed)

A layered architecture (pending NPC-Q3 confirmation):

```
┌──────────────────────────────────────────────────┐
│  Personality (static)                            │  ← traits, kinks,
│  values, edicts, quirks                          │     edicts/anathema
├──────────────────────────────────────────────────┤
│  Mood (dynamic)                                  │  ← arousal, fatigue,
│  emotional state, drives                         │     hunger, fear
├──────────────────────────────────────────────────┤
│  Memory (persistent + decaying)                  │  ← per-NPC episodic
├──────────────────────────────────────────────────┤
│  Goals (active)                                  │  ← short, mid, long
├──────────────────────────────────────────────────┤
│  Schedule (24h)                                  │  ← default routine
├──────────────────────────────────────────────────┤
│  Action selection                                │  ← what to do now
├──────────────────────────────────────────────────┤
│  Behavior tree / utility AI                      │  ← how to do it
└──────────────────────────────────────────────────┘
```

## 4. Memory Model

Memory is the hardest design problem in this domain.

Constraints:
- The world has thousands of NPCs (NPC-Q2 to confirm).
- Memory storage must scale.
- Memory should feel **personal** to the NPC, not LLM-generic.
- Memory must be **queryable** by dialogue, behavior, faction systems.

See NPC-Q1 for memory model options.

## 5. Companions

Companions are NPCs the player travels with. Differences from
non-companion NPCs:

- They follow the player by **negotiated agreement**, not by being
  scripted into the party.
- They have **opinions about the player's actions** (approval-axis or
  opinion-graph; pending NPC-Q12).
- They have **personal arcs** — their goals interact with the
  player's adventures.
- They can **leave**, **die**, **betray**, **be saved**, **be
  romanced**, **breed**, **be enslaved/enslave**, etc., per *NSFW*
  and *Romance*.

The player can travel **alone** (per Vision: solo PC fantasy).
Companions are optional.

## 6. Cross-References

- *World Simulation* — tick that drives NPCs.
- *Dialogue and Conversation* — interface for talking to NPCs.
- *Romance and Relationships* — emotional layer.
- *NSFW* — sexual autonomy of NPCs (N-Q7).
- *Factions and Reputation* — NPC affiliation graph.
- *Body and Identity* — NPC body state (scars, pregnancy, etc.).
- *Crime and Justice* — NPC reactions to crime they witness.
- *Audio* — NPC voice profiles.
- *Performance Budget* — NPC-count budget.

## 7. Open Questions (NPCs and Companions-Local)

### Memory

- **NPC-Q1** Memory model. Options:
  - **(a) Perfect recall + per-NPC log** — small N, scales poorly.
  - **(b) Decaying episodic memory** — recent + important survives;
    old fades.
  - **(c) Summary memory** — stored as periodically-compressed
    summary blocks (LLM-friendly).
  - **(d) Hybrid: recent buffer + summarized history + tagged
    "important" memories never decay.**
  - **(e) Salience-weighted graph memory** — events stored as nodes
    with edges to entities; graph-traversal recall.

### Population

- ~~**NPC-Q2**~~ **Resolved.** **More than 1,000 easily** —
  effectively combining (b) full city populations named with (d)
  procedural-but-stable for everyone else. Major cities get
  hand-authored NPCs across all roles; smaller settlements use
  procedurally-stamped-and-then-frozen NPCs that the player can
  promote to named through interaction (per the §2 fidelity-tier
  promotion model).

### Brain

- **NPC-Q3** Architecture: layered (proposed §3), GOAP, utility AI,
  HTN, behavior tree, LLM-driven, hybrid.
- **NPC-Q4** Personality model — Big Five, custom Pathfinder-flavored
  trait grid, edict/anathema lists, free-form?
- **NPC-Q5** Mood/drive model — Maslow stack, Sims-style needs,
  arousal-fatigue-hunger-fear-hope grid, custom?
- **NPC-Q6** Goal representation — explicit GOAP-style preconditions/
  effects, narrative goal slots, both?

### Speech

- **NPC-Q7** Speech generation — fully hand-authored, hand-authored
  templates with variables, dev-time LLM-generated bank, mix?
- **NPC-Q8** Voice line baking — every line pre-baked vs per-NPC
  voice cloning at runtime cache (per *Audio*).
- **NPC-Q9** Dialect/accent variation by region.
- **NPC-Q10** "Barks" (idle ambient lines) handled differently from
  conversation?

### Companions

- **NPC-Q11** Total companion roster size — handful (BG3-style ~10),
  large (~30+), open-ended-recruit (anyone you persuade)?
- **NPC-Q12** Approval model — single approval axis per companion
  (BG3) vs opinion-multidimensional (likes-this/dislikes-that), vs
  emergent-from-personality?
- **NPC-Q13** Companion-companion relationships — they like, dislike,
  romance each other, even when the player isn't watching?
- **NPC-Q14** Companion permadeath — fully permanent, or
  recoverable via PF2e revival rules?
- **NPC-Q15** "Leave the party" mechanics — companions decide based
  on personality + situation, not narrative trigger.
- **NPC-Q16** Companion sex / romance autonomy with non-player NPCs
  (mirrors N-Q7) — happens off-screen?

### Iconic Heroes

- **NPC-Q17** How are the iconics deployed? (As recruitable
  companions, AP characters, faction heads, encounter NPCs, all
  of the above by iconic?)
- **NPC-Q18** Are iconics canonically pre-leveled, or do they
  scale with the player?

### Lifelikeness

- **NPC-Q19** NPCs change clothes, get dirty, age, gain weight, get
  injured visibly?
- **NPC-Q20** NPCs marry, have children, raise families on their own
  timeline?
- **NPC-Q21** NPC death from accident/disease/war (mirrors L-Q7)?
- **NPC-Q22** NPC religious observance — do they attend services,
  fast on holy days, etc.?
- **NPC-Q23** NPCs have political opinions and might argue about them
  in tavern earshot?
- **NPC-Q24** NPC sexual orientation, paraphilia, taboos — modeled
  per-NPC?
- **NPC-Q25** NPC "secrets" — things they hide, that the player can
  discover via skill checks / spying?

### Reactivity to player

- **NPC-Q26** Reputation model — local, regional, global, faction-
  scoped, all?
- **NPC-Q27** NPCs recognize the player's appearance changes (scars,
  clothing, transformations).
- **NPC-Q28** NPCs react to the player's smell, blood-stains,
  intimate state (NSFW reactivity).
- **NPC-Q29** NPCs react to the player's company (who you walk in
  with).
- **NPC-Q30** NPCs spread rumors about the player (mirrors WS-Q15).

### Performance

- **NPC-Q31** Off-screen NPCs — how much memory per NPC is
  reasonable?
- **NPC-Q32** Pop-in / pop-out — crowd NPCs spawn on player approach;
  how do we make this not feel cheap?
- **NPC-Q33** NPC-density vs frame-rate tradeoff (PB-Q).
- **NPC-Q34** When the simulation is overwhelmed, who downgrades
  first — anonymous crowd, then background named, then named?

### LLM integration (dev-time)

- **NPC-Q35** Dev-time LLM use for: backstory generation, dialogue
  drafting, mood-context speech variants, scheduling exception
  reasoning. Where do we draw the line?
- **NPC-Q36** Possible later runtime LLM (per T-Q16) — would it slot
  into the brain at the action-selection layer or the dialogue
  layer?

### Edge cases

- **NPC-Q37** NPCs that are also player companions in someone else's
  AP (e.g., the iconics) — how do we handle them when the player
  is running that AP?
- **NPC-Q38** "Genericized" extras — does every guard have a name and
  a mom, or are some explicitly anonymous?
- **NPC-Q39** Children — are they NPCs with the same brain
  architecture but constrained behaviors? (Critical for the NSFW
  hard-line to never be crossed even with autonomous NPC behavior.)
- **NPC-Q40** Animal NPCs — same architecture, simpler personality?
