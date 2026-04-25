# DESIGN — Combat

> Living document. Captures the combat-system stance. Magic is its own doc
> (*Magic*) — this doc covers the action layer, not spell internals.

---

## 1. Stance

**Souls-like combat, re-adapted from PF2e Remaster.**

The fantasy: every fight feels weighty, readable, and survivable-with-skill;
positioning, stamina, timing, and build all matter; PF2e's three-action
economy is reshaped, not preserved; the PF2e *math* is preserved.

Reference ceiling: *Elden Ring* / *Sekiro* for moment-to-moment combat
feel. Reference floor: *Dragon's Dogma* for action-RPG class breadth.

## 2. Translation Principles (PF2e → Real-Time Souls-like)

These are working hypotheses, refined per the **resolved C-Q1**:

> **Action-economy translation = stamina meter + per-ability cooldowns +
> Multi-Attack-Penalty as continuous swing-rate.** All three layers
> together, not one-or-the-other.

Detailed mapping:

1. **Three-action economy → stamina + per-ability cooldown +
   continuous swing-rate.**
   - **Stamina** is the global resource for *physical* actions
     (attacks, dodges, sprints, blocks, special weapon arts).
     Regenerates over time; modified by Constitution, encumbrance,
     conditions.
   - **Per-ability cooldowns** apply to discrete special abilities,
     class feats, signature techniques. Some abilities are "always
     available, costs stamina"; others are "cooldown-gated, may also
     cost stamina."
   - **Multi-Attack-Penalty as swing-rate dynamic**: the more rapidly
     the player swings within a short window, the higher the
     under-the-hood penalty to attack rolls — directly mirroring
     PF2e's MAP. The player *feels* this as accuracy degradation
     when mashing rather than as an explicit -5/-10 number.
   - Magical / cast-time abilities (see *Magic*) use a parallel
     *cast-time + interruptibility* model rather than stamina.
2. **Reactions → real-time interrupts.** Attack of Opportunity, Shield
   Block, etc. become *parry/riposte/block* timing windows.
3. **Attack rolls happen under the hood.** Player input (light attack,
   heavy, charged, perfect-timed) modifies the underlying d20 roll —
   skill-shot timing becomes an attack/save bonus.
4. **AC and saves preserved.** Real-time avoidance (dodge, sidestep,
   block, parry, evasion) modifies the rolled outcome rather than
   replacing it.
5. **Damage dice rolled per swing.** Floating-point damage numbers
   sourced from RAW dice expressions (1d8+Str+rune+...).
6. **Critical hit / fumble preserved.** The 10-over / 10-under rule maps
   onto exceptional-timing inputs and exceptional weapon arts.
7. **Conditions preserved by name.** *Frightened*, *Sickened*, *Off-
   guard*, *Slowed*, *Stunned* — same effect, real-time tick.
8. **Incapacitation trait preserved.** High-level players keep the
   immunity-vs-low-level mechanic for boss design clarity.

## 3. Class Identity (Combat)

Each PF2e class must feel **mechanically distinct in real-time**, not
just stat-different. Examples (illustrative, not final):

- **Fighter** — broad weapon mastery, parry windows, exceptional crit
  threat; the "combat skill expression" class.
- **Barbarian** — instinct-coded rage modes, posture-break bias, less
  defense in exchange for damage.
- **Champion** — reaction-heavy, ally-protection mechanics, divine
  attunement charges.
- **Monk** — flow/combo system, ki-fueled stances, unarmed reach.
- **Ranger** — hunt-target tracking, bow handling, animal-companion
  pair-play.
- **Rogue** — stealth, off-guard exploitation, finisher windows.
- **Investigator** — Devise-a-Stratagem-shaped "read" mechanic.
- **Swashbuckler** — panache build/spend during fights.
- **Magus** — spellstrike-as-skillshot.
- **Inventor** — innovation gadget loadout.
- **Gunslinger** — reload management, slinger's reflex windows.
- **Thaumaturge** — esoterica swap, vulnerability application.
- **Kineticist** — channel/impulse stance switching.
- **Druid / Cleric / Witch / Wizard / Sorcerer / Bard / Oracle / Animist
  / Psychic / Summoner** — covered under *Magic* (caster combat is
  largely magic-system-driven).

The radical difference between **mage** and **fighter** is explicit
intent (per Vision answer 18); see *Magic*.

## 4. Companions in Combat

- Companions fight **as autonomous agents**. The player does not pause-
  and-issue-orders.
- Player can issue **lightweight commands** (whistle, gesture, shout):
  rough behavior modes (aggressive / defensive / ranged / withdraw),
  target priority hints, and a small set of ability triggers.
- Each companion has their own AI personality affecting their
  preferred tactics, willingness to follow orders, and morale.

## 5. Encounter Pacing

- **Wandering threats are real.** No invisible encounter walls.
- **PF2e XP budgets** drive encounter generation but are softened by
  context (terrain, time of day, NPC presence, faction).
- **Boss design** uses Souls-like phase logic — moveset reveal, openings,
  punish windows — while keeping PF2e creature stat blocks as the
  underlying truth.
- **Mass combat** (Kingmaker, War for the Crown) — TBD; likely a
  separate sub-mode with its own rules slice.

## 6. Out of Combat / In Combat Boundary

Open question. Project Zomboid / RDR2 model combat as continuous with
exploration; Pathfinder traditionally has a hard initiative boundary.
We default to **continuous** with an *initiative blend*: when a fight
starts, an "encounter clock" begins, but the world keeps ticking; if
the protagonist disengages and outruns, the encounter dissolves.

## 7. Magic in Combat

Hooks only — full design is in *Magic*. Confirmed:
- Full PF spell list + additions + third-party metamagic.
- Reworked: less esoteric, more alchemical/rational.
- High-quality UX/UI (the magic interface is itself a feature).
- Mage gameplay is **radically different** from fighter gameplay.

## 8. Cross-References

- *Magic* — caster combat, spell interface, metamagic.
- *Core Loop and Structure* — encounter persistence, time during combat.
- *Rules and Edition* — RAW math preservation, conversion stance.

## 9. Open Questions (Combat-Local)

- ~~C-Q1.~~ **Resolved.** Hybrid: stamina + per-ability cooldowns +
  MAP-as-swing-rate. See §2.
- C-Q2. Lock-on camera (Souls) vs full free-aim (Skyrim/RDR2)?
- C-Q3. Hit-stop, posture-break, and stagger mechanics — adopted?
- C-Q4. Weapon arts (Elden Ring) vs feats-as-actions — how feat-granted
  combat options surface in real-time UI.
- C-Q5. Reach, flanking, off-guard — preserved as positional truths?
- C-Q6. Multi-target / area attacks (cleave, sweep) — input model?
- C-Q7. Initiative — does the game expose it at all, or is it purely
  hidden?
- C-Q8. Mass combat sub-system — own doc when ready.
- C-Q9. Difficulty scaling — fixed PF2e math, or a "softer/harder"
  variant slider?
- C-Q10. PvP duels (NPC-vs-PC honor duels, Pathfinder Society arena,
  tournaments) — handled in main system or sub-mode?
- C-Q11. Crit decks / crit-effect tables — surface in the real-time
  system or hide behind animation?
- C-Q12. Death-blow / executions / mercy mechanic for NSFW capture
  scenarios — see *NSFW*.
