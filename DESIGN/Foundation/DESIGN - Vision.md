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

### 4.2 Origin Framing (resolved V-Q3)

> **Isekai (transported from elsewhere) + In medias res.**

- Gherman is **not native to Golarion**. He was transported from
  another world (specifics canonically unknown to him; player
  discovers progressively).
- The game opens **in medias res** — the player joins Gherman *after*
  the inciting event, not before. No setup cinematic depicting the
  "before"; the mystery starts already in motion.
- Specifically: Gherman is found **seemingly dead on the shore of the
  Foam River near Falcon's Hollow** (frontier town in Andoran's
  Darkmoon Vale) and is brought into town to recover.
- The player takes control when Gherman **wakes up in Falcon's
  Hollow** — exact location pending V-Q10-followup (inn / tavern /
  temple).

### 4.3 Other Canonical Traits (resolved V-Q2, V-Q4–V-Q10)

| V-Q | Trait | Value |
|---|---|---|
| **V-Q2** | Class / archetype | **Flexible class with unique quirks**, exposed later through play |
| **V-Q4** | Orientation | **Straight** |
| **V-Q5** | Aging | **1:1 with the world** — Gherman starts 21, ages on the same calendar tick as everyone else |
| **V-Q6** | Starting languages | **Common** (only) |
| **V-Q7** | Distinctive marks | **Tattoo `08` on the inside of his right wrist** — origin unknown to him |
| **V-Q8** | Voice profile | **No accent**; **low register**; **apathetic baseline** with hints of **sarcasm** and **cynicism**; **world-worn 21** |
| **V-Q9** | Face | **Single canonical face**, designed by us; no face customization |
| **V-Q10** | Starting location | **Falcon's Hollow** (Andoran, Darkmoon Vale) — found seemingly dead on the Foam River shore, brought into town. Specific room (inn / tavern / temple) pending V-Q10-followup |

### 4.4 Implications

- **Isekai framing** explains the canonically-unknown ancestry and
  backstory in a way that respects in-fiction logic: he's an outsider
  who didn't grow up in Golarion at all.
- **Common-only languages** are weird for a man with no Golarion
  origin — implying either (a) he had a magical translation effect
  applied during transport, (b) he learned Common before transport
  via an unknown means, or (c) the isekai mechanism conferred Common.
  Pending V-Q6-followup.
- **Tattoo `08`** is an obvious plot hook — institutional numbering
  from his origin world? Cult marking? Identification number? We
  control its meaning; design pending.
- **Apathetic + sarcastic + world-worn 21** is a tonal anchor for
  every line of VO and every scene-camera framing involving Gherman.
  Drives V-Q8 follow-up: voice-actor reference (existing voice we
  clone from? synthetic from scratch? composite?).
- **Aging 1:1 with world** + persistent world (per *Core Loop and
  Structure*) means decades-long playthroughs are coherent. Gherman
  at 60 is a different person than Gherman at 21 — body, social,
  combat, romantic, magical implications all cascade. See L-Q5/L-Q6,
  N-Q4, BI-Q31.
- **Falcon's Hollow opening** anchors the early game in **Andoran's
  Darkmoon Vale**. This is canonical (and a published Pathfinder
  starter region — *Hollow's Last Hope* etc.), giving us proven AP
  material for the first arc. See LR-Q for any reworks needed.

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

## 7. Project Intent: Anime Story Basis

> *"Game is designed to create a living world as basis for an anime
> story of what happens, somewhat."*

A **soft directive**, qualified ("somewhat"), but load-bearing for
production craft. The project produces a living, simulated Golarion;
**emergent play is shaped to read like an anime narrative** when
viewed as story.

This is **not** a constraint on what stories happen — the simulation
generates events organically. The directive shapes **how** those
events look, sound, and feel:

- **Tone and pacing.** Even the context-dependent tone palette
  (per §3) is **weighted toward anime conventions**: dramatic beats,
  introspective interludes, slice-of-life rests between arcs, comic
  release after tension, quiet emotional moments held longer than
  Western pacing would.
- **Visual language** (per *Art and Presentation* §1.1) — anime
  cel-shading, anime expression range, anime poses. Already locked.
- **Animation language** (per *Animation Pipeline*) — anime-style
  poses, exaggerated key moments, anticipation-and-snap timing,
  expression sheets per character.
- **Camera language** (per *Camera and Cinematography*) — close-ups
  on emotional moments, dramatic angles, speed lines and
  motion-streak effects on key beats, time-suspension for impact
  hits.
- **Dialogue cadence** (per *Dialogue and Conversation*) — beats
  drawn from anime/manga rhythm; introspection allowed; trope-aware
  writing; subtext and body-language carried by performance, not
  exposition.
- **Music and audio** (per *Audio*) — JRPG / anime VO conventions,
  motif-per-character, leitmotifs for arcs.
- **Companion and NPC archetypes** (per *NPCs and Companions*) —
  anime archetypes (kuudere, tsundere, deuteragonist, mentor, fated
  rival, etc.) as **starting templates**, deepened beyond stereotype
  through relational play.
- **Story export potential** — eventually, screenshot / clip /
  storyboard / scene-export tooling may be relevant so the player
  (or developer) can clip story moments into anime-formatted
  artifacts. **Deferred** — see V-Q11 below.
- **Gherman's voice profile** (V-Q8) — apathetic / sarcastic /
  cynical / world-worn — fits a recognizable anime-protagonist
  archetype (jaded male MC, drawn back into engagement by the world
  and characters around him).

Cross-references: this pillar ripples through *Art and Presentation*,
*Animation Pipeline*, *Camera and Cinematography*, *Dialogue and
Conversation*, *Audio*, *NPCs and Companions*. As we deepen each of
those domains, anime-conventions guidance is folded in.

## 8. Cross-References

- Tonal flexibility → see *Art and Presentation* (lighting/music modes).
- Anime story basis → see §7 + *Art and Presentation*, *Animation
  Pipeline*, *Camera and Cinematography*, *Dialogue and Conversation*,
  *Audio*, *NPCs and Companions*.
- Protagonist details → §4.
- Simulation density → see *Core Loop and Structure*.
- "Anything" includes NSFW — see *NSFW*.

## 9. Open Questions (Vision-Local)

- ~~V-Q1, V-Q1-followup.~~ **Resolved.** Identity + diegetic mystery.
  See §4.1.
- ~~V-Q2.~~ **Resolved.** Flexible class with unique quirks
  (exposed later). See §4.3.
- ~~V-Q3.~~ **Resolved.** Isekai + in medias res; opening at
  Falcon's Hollow on Foam River shore. See §4.2.
- ~~V-Q4.~~ **Resolved.** Straight. See §4.3.
- ~~V-Q5.~~ **Resolved.** Ages 1:1 with world from age 21. See §4.3.
- ~~V-Q6.~~ **Resolved.** Common only. See §4.3.
- ~~V-Q7.~~ **Resolved.** Tattoo `08` on inside right wrist. See §4.3.
- ~~V-Q8.~~ **Resolved.** No accent, low register, apathetic baseline
  with sarcasm/cynicism, world-worn 21. See §4.3.
- ~~V-Q9.~~ **Resolved.** Single canonical face. See §4.3.
- ~~V-Q10.~~ **Partially resolved.** Falcon's Hollow / Foam River
  shore / wakes up in town. See §4.3 and V-Q10-followup.

### New / Expanded

- **V-Q2-followup.** "Flexible class with unique quirks (exposed
  later)" — what does *flexible class* mean concretely? Options:
  - (a) **Daggerfall-style emergent** — Gherman has no class; what
    he does shapes what he becomes (combat-driven → fighter feats
    unlock; magic-driven → caster path opens).
  - (b) **PF2e-RAW class with player-pick at level 1** but
    in-fiction "I don't yet know what I am."
  - (c) **Hidden class** — the engine assigns a class behind the
    scenes based on opening-arc choices; reveals over time.
  - (d) **Multi-class via Free Archetype** (R-Q1 implication) —
    Gherman gets several archetype slots over time, growing into
    his identity.
  - (e) **Custom mechanic** that's neither RAW class nor pure
    emergent — describe.
- **V-Q2-quirks.** "Unique quirks" — when revealed, what flavor?
  Magical (innate ability from his origin world), supernatural
  (tied to the tattoo), mundane-skill (anachronistic knowledge
  from his other world), all of the above?
- **V-Q3-followup.** Isekai source world — fully canonical-Golarion-
  invented (a forgotten plane of the Great Beyond, a dead world,
  a parallel Material Plane), or **Earth** (modern / historical /
  futuristic), or *unspecified — discovered late game*?
- **V-Q3-mechanism.** What transported him? Magical ritual,
  cosmic accident, deity action, technological mishap, war
  casualty, voluntary, summoned, betrayed, curse?
- **V-Q6-followup.** How does Gherman speak Common at start with no
  Golarion origin? (a) Translation magic at transport. (b) The
  tattoo `08` confers it. (c) Earth-origin where some equivalent of
  Common exists. (d) Pre-transport he was already a planar
  traveler. (e) Other.
- **V-Q7-followup.** Tattoo `08` meaning — pick now, defer to play?
  Candidates: institutional numbering (orphanage, prison, military),
  cult member, identification chip in tattoo form, divine mark,
  test-subject number from a magical/scientific facility, custom.
- **V-Q8-followup.** Voice acquisition — pick a reference voice
  actor we'd like to clone-from-style (per T-Q9/T-Q10 dev-time TTS),
  or define purely synthetic from voice-profile prompts? (Free use
  per Q33.)
- **V-Q9-followup.** Canonical face — when do we design it? Now
  (concept art spike) or after the cel-shader spike (BL-0001)?
- **V-Q10-followup.** Where exactly in Falcon's Hollow does Gherman
  wake up? (a) The Sitting Duck inn. (b) An alternate inn / tavern.
  (c) The Sarenrae chapel. (d) The home of a private healer. (e)
  The town's communal house / local lord's hall. Each carries
  different first-NPC implications.
- **V-Q11.** **(New, from §7 anime-story-basis pillar.)** Does the
  project commit to **scene/clip/storyboard export tooling** as a
  deferred deliverable? If yes, what fidelity: still-frame
  screenshots, video clips, panel layouts, full storyboard with
  dialogue?
- **V-Q12.** **(New.)** Anime-archetype starter templates for
  companions and NPCs — adopt as a writing convention (with deeper
  later development), or treat anime-archetype-flavor as a *light
  garnish* rather than a starting structure?
- **V-Q13.** **(New.)** Gherman's "isekai outsider" status —
  perceptible by NPCs (smell wrong, look wrong, magical detection
  flags), or invisible (he passes for human-Golarion at a glance)?
