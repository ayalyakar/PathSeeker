# DESIGN — Vision

> Living document. Captures the project's north-star fantasy, tonal palette,
> protagonist framing, and the inspirational works that anchor the feel.
> Decisions here should be the slowest to change.

---

## 1. Core Player Fantasy

> *"I am a character living inside Golarion, in a fully complex and simulated
> lifelike world. I can do anything."*

This is the foundational sentence the rest of the design must serve. Every
subsystem (combat, NSFW, dialogue, economy, magic, weather, AI scheduling) is
in service of the player feeling **embodied** inside a world that **continues
without them** and **reacts plausibly** when they touch it.

Three sub-pillars implied by the sentence:

- **Embodiment** — first-person, persistent, no fourth-wall menus that break
  presence (UI is diegetic where feasible — see *Art and Presentation*).
- **Simulation depth** — NPCs, factions, economies, weather, time, and
  ecosystems run independently of the player.
- **Agency without rails** — the world supports the player attempting any
  reasonable (and many unreasonable) actions, including those most RPGs
  refuse to model.

## 2. Inspirational Palette

The game should feel like a careful synthesis of:

| Source | What it contributes |
|---|---|
| **Wizardry** | First-person dungeoneering rigor, deep character systems |
| **Pillars of Eternity** | Reactive prose, faithful TTRPG-derived rules |
| **Monster Girl Quest** | Mechanically integrated NSFW, encounter writing |
| **Baldur's Gate (franchise)** | Companion depth, faithful adaptation craft |
| **Etrian Odyssey** | Mapping/exploration as gameplay, dungeon identity |
| **Koikatsu / Illusion** | Character creation depth, full-3D intimate scenes |
| **Daggerfall** | Scale, procedural breadth, "do anything" energy |
| **Disgaea** | Number-go-up depth, systemic absurdity at the edges |
| **Persona** | Calendar/life-sim fusion, social link cadence, UI flair |
| **FromSoftware** | Combat feel, environmental storytelling, opacity-as-design |
| **Project Zomboid** | Sim-density, brutal consequence, no hand-holding |
| **The Sims** | Daily-life granularity, autonomous NPC behavior |
| **Red Dead Redemption 2** | World reactivity, NPC schedules, ambient drama |

Not a checklist — a tonal North Star. When a design choice is contested, ask:
*does this sit comfortably inside the polygon those games define?*

## 3. Tone

**Highly context-dependent.** No single register dominates. The game must be
able to:

- Run a heroic AP arc with mythic weight,
- Pivot to comedic banter at the inn the next hour,
- Stage a quiet melancholic romance scene,
- Host extreme/dark NSFW content in private,
- Satirize Golarion's own tropes when appropriate.

This means writing systems, music systems, lighting, and NPC dialogue
selection must all be **scene-aware** rather than globally tuned. See
*Core Loop and Structure* for the scene/mode-switching mechanism (TBD).

## 4. Protagonist

- **Pre-defined protagonist.** Not a self-insert; not a created PC.
- Pre-defined as **human** (per NSFW design — keeps the body-systems anchor
  ancestry-stable while interacting with non-human partners).
- Identity, name, backstory, gender, and starting circumstance: **TBD** —
  blocks several downstream decisions (voice casting, opening cinematic,
  starting region, default class, canonical relationships).

## 5. Solo PC, Lifelike Party

- The player controls **only** the protagonist.
- All other party members and the entire world are NPCs driven by the
  simulation + AI behavior layer.
- This is a deliberate inversion of BG3/Pathfinder-Kingmaker control. The
  fantasy is "I am one person in a world of people," not "I am a god of
  five bodies." Companions must therefore be *believable as autonomous agents*
  — they refuse, leave, sleep, pursue their own goals.

## 6. Forever Project

- No MVP. No ship date.
- Foundations bias toward **modularity, data-driven content, and
  long-horizon refactor tolerance** over flashy verticals.
- Throwaway prototypes are fine for de-risking but should be marked as such.

## 7. Cross-References

- Tonal flexibility → see *Art and Presentation* (lighting/music modes).
- Protagonist details → see *Open Questions*.
- Simulation density → see *Core Loop and Structure*.
- "Anything" includes NSFW — see *NSFW*.

## 8. Open Questions (Vision-Local)

- V-Q1. Protagonist identity baseline (gender, name, age-bracket, origin).
- V-Q2. Does the protagonist have a fixed **class/archetype**, or do they
  pick at character-creation-lite?
- V-Q3. Opening framing: amnesia, exiled noble, fresh adventurer, surviving
  catastrophe, isekai-from-Earth, in medias res, or player-elected?
- V-Q4. Is the protagonist canonically *bisexual / pansexual / orientation-
  fluid* (pragmatic for romance breadth) or fixed?
- V-Q5. Does the protagonist age over the course of the game's persistent
  timeline? (Affects long-term saves, NPC relationships, mortality stakes.)
