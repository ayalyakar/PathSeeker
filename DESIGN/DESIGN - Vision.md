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

### 4.1 Canonical Identity (resolved V-Q1)

| Trait | Value |
|---|---|
| **Name** | **Gherman** |
| **Gender** | Male |
| **Age at game start** | 21 |
| **Ancestry of origin** | **Canonically unknown** — to be discovered in-game |
| **Backstory** | **Canonically unknown** — to be discovered in-game |

The "Unknown" entries are **diegetic mystery** (resolved
V-Q1-followup): the protagonist himself does not know his origin
or past at the start of the game. The discovery of identity is one
of the long-arc plot threads — *not* an authorial deferral.

### 4.2 Implications

- The opening framing must explain **why** Gherman's origin and history
  are unknown to him: amnesia, exile, abandonment-as-infant, magical
  curse, identity-erasure ritual, etc. (See V-Q3.)
- The **discovery of identity** is itself a long-arc plot thread.
- All canonical-Golarion content that assumes a known origin (ancestry
  feats triggered at level 1, ancestral languages known, family-region
  reputation) needs a "blank-slate-protagonist" treatment.
- Gender-fixed protagonist + pre-defined identity simplifies cinematic
  authoring, voice casting, animation pipeline, and tailored romance
  arcs — at the cost of the player not "being themselves."

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

- ~~V-Q1.~~ **Resolved.** Gherman, Male, 21, ancestry/backstory canonically
  unknown. See §4.
- ~~V-Q1-followup.~~ **Resolved.** Diegetic mystery — Gherman does
  not know his own origin or past; discoverable in-game.
- V-Q2. Does Gherman have a fixed **class/archetype**, or pick at character-
  creation-lite? (Heightened by the "unknown origin" framing — does he
  even know his class at start?)
- V-Q3. **Opening framing**, now load-bearing: amnesia, exiled, abandoned,
  cursed identity-erasure, ritual-stripped, in medias res, isekai-from-
  Earth, recovered-from-comatose-ten-years-after-event, or other?
- V-Q4. Gherman's canonical orientation: fixed straight, fixed bi/pan,
  fluid, or unspecified-and-emergent-from-play?
- V-Q5. Does Gherman age over the persistent timeline? (At 21 starting
  age, an aging protagonist has interesting story arc potential.)
- V-Q6. **(New)** Does Gherman have a known starting **language set**? If
  origin is unknown, what languages does he speak at start?
- V-Q7. **(New)** Does Gherman have any **distinctive marks** at start —
  scars, tattoos, brands, magical sigils — that hint at origin?
- V-Q8. **(New)** Voice profile for Gherman — accent, register, age-feel
  of voice, emotional baseline. Drives all VO casting/cloning.
- V-Q9. **(New)** Does Gherman have a **canonical face** (designed by us)
  or do we offer face customization while keeping the rest fixed?
- V-Q10. **(New)** Starting location of the game — where is Gherman when
  the player takes control? (Inn, ship, prison cell, alley, woods,
  battlefield, ritual chamber, …)
