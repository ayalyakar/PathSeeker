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

### 4.3 Other Canonical Traits (resolved V-Q2, V-Q4–V-Q10, V-Q12, V-Q13)

| V-Q | Trait | Value |
|---|---|---|
| **V-Q2** | Class / archetype | **Effectively unclassed** at start (hidden / custom-classed). Build emerges from play; class identity is exposed late and may take a non-RAW shape. See §4.3.1. |
| **V-Q4** | Orientation | **Straight** |
| **V-Q5** | Aging | **1:1 with the world** — Gherman starts 21, ages on the same calendar tick as everyone else |
| **V-Q6** | Starting languages | **Common** (only). "Common is common" — accepted as a setting given; no specific origin-language acquired |
| **V-Q7** | Distinctive marks | **Tattoo `08` on the inside of his right wrist** — meaning unknown to him *and to the design* (deferred to play-discovery per V-Q7-followup) |
| **V-Q8** | Voice profile | **No accent**; **low register**; **apathetic baseline** with hints of **sarcasm** and **cynicism**; **world-worn 21**. Voice produced **synthetic-from-prompts** (no actor reference; per V-Q8-followup) |
| **V-Q9** | Face | **Single canonical face**, designed by us; no face customization. **Designed after BL-0001 cel-shader spike** so face concept matches final renderer (per V-Q9-followup) |
| **V-Q10** | Starting location | **Falcon's Hollow, Sarenrae's chapel** (Andoran, Darkmoon Vale). Found seemingly dead on the Foam River shore, brought to the chapel for vigil/recovery |
| **V-Q12** | Anime archetypes | **No archetype, or surface-level only.** Companions and NPCs do not start as kuudere/tsundere/etc. templates. Anime-archetype flavor may **light-touch** a character's early read but is not a starting structure |
| **V-Q13** | Outsider perceptibility | Looks like any other human, but wears a **modern outfit** at game start. Beyond the outfit, **everyone can tell something is off** with him — see §4.4 |

### 4.3.1 Class Shape (resolved V-Q2-followup)

> **Effectively unclassed / custom-classed.** Mostly Option C (hidden
> class assigned by the engine based on opening-arc choices) **plus
> emergent shaping** (Option A) — Gherman is what he does, with the
> engine quietly tracking and revealing class identity (or a custom-
> shaped non-RAW path) over time.

This means:
- No class-pick screen.
- No class label visible to the player at start.
- Combat actions, magic experimentation, social style, and downtime
  pursuits build hidden affinities.
- At a later narrative beat, the affinities **crystallize** as a
  PF2e RAW class **or** a custom-shaped path that diverges from RAW.
- The unique quirks (V-Q2-quirks) are **mixed flavor and currently
  unknown** to design — to be authored as the class arc emerges.

### 4.4 Visible Anachronism and "Wrongness" (resolved V-Q13, V-Q16)

- Gherman **looks like any other human** at a glance — body, face,
  height, build all read as human-Golarion.
- He wakes up wearing a **modern outfit** (clothing alien to
  Golarion's medieval-fantasy aesthetic) — the most immediate
  visible cue to NPCs that something is wrong.
- The modern outfit will be **replaced** as Gherman acquires
  Golarion-appropriate clothing. *Body and Identity* tracks any
  pieces he keeps as persistent mementos.
- Even after dressing down, **everyone can tell something is off
  about him** — pervasive non-verbal signal that NPCs sense
  without being able to name it.

#### 4.4.1 The two mechanisms (resolved V-Q16)

The "wrongness" decomposes into **two distinct, simultaneously-
active effects** that NPCs feel at the same time:

##### A) Magnetism

> An **unmistakable pull** toward Gherman, variable in intensity
> from **lightly noticed** to **obsession**, with everything in
> between. **Especially affects women** (single or partnered alike).
> Women in committed relationships are *not* immune — the magnetism
> is strong enough to fray vows, justify infidelity to one's own
> conscience, or draw uninvited attention even on first sight.

Mechanically (proposed; see *NPCs and Companions*, *Romance and
Relationships*, *NSFW*):

- A `Magnetism` modifier applies on every NPC interaction with
  Gherman, scaled by **NPC personality** (resistance, openness,
  attraction profile), **proximity**, **prior exposure** (it grows
  with familiarity), and **NPC current mood / vulnerability**.
- Outcome bands: **subliminal** (NPC notices nothing consciously
  but their behavior shifts), **noticed** (NPC is aware of being
  drawn), **infatuation** (NPC's autonomous goals start including
  Gherman), **obsession** (NPC's autonomous goals are dominated by
  Gherman; jealousy, possessiveness, breakdown if denied).
- "Especially women" is the default attraction profile, but is
  modulated by individual NPC orientation and personality —
  straight men, asexual/aromantic NPCs, and women with strong
  resistance can land in lower bands; even hostile resistance
  doesn't *eliminate* the pull, only suppresses it.
- The magnetism is **not consent-conferring** for *NSFW*
  purposes. NPCs in obsession-band states may pursue intimacy
  Gherman doesn't reciprocate; the system models that asymmetry
  honestly. Likewise, Gherman's reciprocation under magnetism is
  not pre-determined — the player picks his behavior.

##### B) Ambiguous aura

> A **strange aura** that NPCs perceive as **"something wrong"** —
> but **most cannot tell whether it's wrong in the *good* sense or
> the *bad* sense**. Reactions split unpredictably between
> protective drawing-toward and instinctive recoil, and many NPCs
> oscillate between the two.

Mechanically (proposed):

- An `Aura` modifier separate from magnetism — a perceptibility
  signal coloring NPC instinct.
- Per-NPC roll on first contact assigns a **read polarity**
  (positive / negative / unreadable), modulated by NPC training
  in occult / religious detection (priests, witches, oracles, and
  certain trained NPCs read more accurately, sometimes uncovering
  the underlying isekai-outsider truth).
- The polarity is **not the truth** — it is the NPC's gut. Two
  NPCs may meet Gherman together and form opposite reads.
- Cumulative interaction can shift the read; betrayal or kindness
  consolidates it.
- Religious factions, divinatory NPCs, and entities with
  alignment-replacement-trait sensitivity (`sanctified`/`unholy`/
  spirit-detection) get **distinctive but ambiguous** results
  rather than the empty *void* read that V-Q17 atheism produces.
  The two signals (atheism-void + ambiguous-aura) compound to
  make Gherman an **interesting puzzle** to any NPC paying
  attention.

##### How the two interact

- A given NPC can be **drawn-by-magnetism + recoiling-by-aura**
  simultaneously, producing the classic anime-protagonist effect
  of "I can't stop watching him and I don't know why I'm afraid."
- Or **drawn-by-magnetism + drawn-by-aura** — instant, unsettling
  attachment.
- Or **resistant-magnetism + recoiling-aura** — outright hostile.
- Or **resistant-magnetism + drawn-aura** — a curious wary
  protector.
- The four-quadrant model is a useful first approximation; the
  actual mechanic resolves with continuous values (see open
  follow-ups in §9).

The two mechanisms are the engine that makes Gherman behave like
an **anime protagonist** in the world: improbable harem dynamics
become diegetic; emergent NSFW scenes have a believable in-fiction
trigger; faction tensions form around him organically; Sarenrae's
chapel staff find themselves both pulled to and disturbed by him
on day one.

#### 4.4.2 Surfaces affected

The "wrongness" mechanism is a **load-bearing scene-design lever**.
A thousand small moments throughout the game come back to it:

- **First impressions** (NPC reactions in *Dialogue*, *NPCs and
  Companions*, *Crime and Justice*).
- **Magical detection** (divinations, *detect outsider*-like
  effects, certain rituals).
- **Faction reactivity** (religious orders read his aura;
  scholarly factions notice his outfit; paranoid factions notice
  both).
- **Romance / intimacy beats** — partners sense it on physical
  contact; cumulative exposure consolidates polarity.
- **NSFW emergence** — the magnetism is the engine that turns
  ambient interaction into intimate possibility.
- **Witnessing crimes** — witness reliability is colored by their
  read of Gherman; some refuse to testify against him, others
  fixate on him as the obvious suspect regardless of evidence.

### 4.5 Implications

- **Isekai framing** explains the canonically-unknown ancestry and
  backstory in a way that respects in-fiction logic.
- **Source world and transport mechanism** are **deferred**
  (V-Q3-followup, V-Q3-mechanism). The game can be played in full
  without resolving them; if/when resolution happens, it is a
  late-game beat.
- **Common-only languages** explained by setting convention:
  Common is common. No magical machinery required.
- **Tattoo `08`** is a permanent mystery prop. Meaning is not
  pre-authored; we'll define it when the relevant arc surfaces.
- **Apathetic + sarcastic + world-worn 21** is the tonal anchor.
  Voice is synthetic-from-prompts.
- **Aging 1:1 with world** + persistent world means decades-long
  playthroughs are coherent.
- **Falcon's Hollow / Sarenrae's chapel opening** anchors the
  early game in **Andoran's Darkmoon Vale** with a Sarenrae-
  aligned cleric/healer as the first NPC. Intersects:
  - *Religion and Devotion* (first divine NPC, regardless of
    Gherman's eventual stance).
  - *Lore* (Darkmoon Vale, Lumber Consortium, *Hollow's Last Hope*
    AP material in scope per BL-0026).
  - *Crime and Justice* (Lumber Consortium oppression as early
    political lever).
  - *Body and Identity* (the chapel discovers and documents
    Gherman's body state on intake — tattoo, outfit, "wrongness").
- **Gherman has no patron deity** at game start (resolved RD-Q1
  this turn). Sarenrae's chapel is his *first NPC contact*, not his
  faith. Specific stance toward the divine pending V-Q17.

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

## 7. Project Intent: Anime Story Basis (Main Focus)

> *"Game is designed to create a living world as basis for an anime
> story of what happens, somewhat."*
>
> **Reaffirmed:** *"Main focus is to create an anime out of it.
> With tons of inspirations."*

This is the **primary project intent**. It supersedes
"forever project" framing where the two conflict: every long-horizon
choice should serve the goal of producing a **living world whose
emergent play reads as anime**.

The project is therefore **two layered ambitions stacked**:

1. A faithful, simulation-rich, NSFW-unlocked Pathfinder RPG (per
   §1, §3, §4).
2. **An anime-story generator** built on top of that simulation —
   the simulation produces moments; those moments are the anime.

The directive ripples through every craft decision:

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
- **Story export potential** — given the elevated focus, this is
  promoted from "deferred" to **likely-needed**: screenshot / clip /
  scene / storyboard export tooling is on the planning horizon so
  emergent moments can be captured as anime-formatted artifacts.
  Format and fidelity still pending V-Q11-restated below.
- **Gherman's voice profile** (V-Q8) — apathetic / sarcastic /
  cynical / world-worn — fits a recognizable anime-protagonist
  archetype (jaded male MC drawn back into engagement). Note that
  V-Q12 explicitly **rejects** archetype-as-starting-template at
  the writing level — anime archetype flavor is *surface*, never
  scaffolding.
- **"Tons of inspirations"** — the user has explicitly committed to
  drawing on a large reference library of anime / manga / light
  novels. This list is **pending V-Q14** below — each named
  reference becomes a tonal-vocabulary entry the design can draw
  from.

### 7.2 What the elevation changes

Concretely, the promotion from "soft directive" to "main focus"
changes:

- **Camera and Cinematography** is no longer a support craft — it
  becomes a primary domain (because *the camera is the anime*).
  Cinematic density goes up (per CC-Q1 resolution: "lots of
  cinematics"). See *Camera and Cinematography*.
- **Animation** must hit anime-quality keyframes for emotional and
  combat beats — not just functional motion. See *Animation
  Pipeline*.
- **Dialogue cadence** must read on the page like anime/manga
  dialogue does — short beats, subtext, body-language gaps,
  punchline timing.
- **Music** prioritizes JRPG / anime score conventions.
- **Performance Budget** allocates more frame budget to
  cinematic-quality moments (per *Performance Budget*).
- **Story-export tooling** is committed and built **all parallel**
  (resolved V-Q11-followup): screenshot mode, clip recorder,
  storyboard/panel export, and full episode export are all in
  scope concurrently, none deferred behind the others.

### 7.3 Tonal Vocabulary — Anime Inspirations (resolved V-Q14)

The following is the **anchor reference list** for the project's
anime tonal vocabulary. Each entry is a citation any design doc can
draw from when justifying or describing a tonal/visual/narrative
choice. List is **non-closed** — the user has signalled "and
probably more" for future additions (BL-0027 stays open as
an inspirations-list backlog).

| Inspiration | What it contributes to PathSeeker |
|---|---|
| **Hell's Paradise (Jigokuraku)** | Visceral horror-with-beauty aesthetic; survival in an exotic doomed environment; criminals seeking redemption framing; lush body-horror combat |
| **Fate/Zero**, **Fate/Stay Night**, **Heaven's Feel** | Layered moralities in a high-stakes magical war; summoned legends meeting modern flesh; tragic romance under doom; Heaven's Feel specifically — explicit darkness, body horror, sacrificial sexuality, "the route where everything breaks" |
| **Bleach** | Stylish combat-as-identity; expansive cosmology of soul / hierarchy / opposition (Soul Society / Hollow / Espada); climactic showdown structure; cool-as-craft aesthetic; ban-kai-style "true form revealed" beats |
| **Redo of Healer (Kaifuku Jutsushi Yarinaoshi)** | Openly transgressive sexual content; vengeance arc as central drama; transformation and captivity as gameplay-narrative loop; healing-as-control-reversal; permission to render the dark thoroughly |
| **Demon Slayer (Kimetsu no Yaiba)** | Combat-as-art (breathing-style visuals, motion as living calligraphy); generational trauma and family bonds; suffering-rendered-beautiful; period-piece weight applied to fantasy |
| **My Dress-Up Darling (Sono Bisque Doll)** | Slice-of-life romance counterbalance; hobby-as-bonding; gentle sensuality and body acceptance; soft pacing between dark arcs; craft-as-intimacy |
| **Berserk** | Dark fantasy gravity at the upper limit; epic suffering and defiant agency; betrayal as cosmic horror; demonic warfare; permission to render rape, gore, and divine evil unflinchingly |
| **Goblin Slayer** | Monomaniacal purpose carried by an "ordinary" adventurer; party dynamics in low-fantasy adventure; brutal-realism in a heroic setting; tabletop-RPG flavored party play |

**How this list is used:**

- When a design choice is contested, point at the inspiration(s) it
  serves (e.g., "this combat camera draws from *Demon Slayer*'s
  breathing-style coverage; this tone draws from *Berserk*").
- Cross-doc citations: any doc may cite an inspiration with the
  shorthand `[insp: <Title>]` to anchor a design choice.
- The **NSFW + dark-themes commitment** (per *NSFW* §1) is
  doubly-anchored by *Redo of Healer* + *Berserk* — the
  inspirations explicitly cover the explicit + transgressive +
  brutal range the project commits to render.
- The **slice-of-life balance** (per *Vision* §3 tonal flexibility)
  is anchored by *My Dress-Up Darling* — it reminds us that the
  project is not all darkness; gentle scenes are first-class.
- The **cool-stylized combat** (per *Combat*, *Animation Pipeline*)
  is anchored by *Bleach* + *Demon Slayer*.
- The **summoning / cosmology** flavor (per *Magic*, *Religion and
  Devotion*, *Death and Afterlife*) draws from *Fate* + *Bleach*.

### 7.4 Cross-References (anime layer)

This pillar ripples through *Art and Presentation*, *Animation
Pipeline*, *Camera and Cinematography*, *Dialogue and Conversation*,
*Audio*, *NPCs and Companions*, *Tech and Engine* (export tooling),
*Combat* (combat-as-art), *NSFW* (transgressive anime grounding),
and *Magic* / *Religion and Devotion* / *Death and Afterlife*
(cosmology). As we deepen each of those domains, anime-conventions
guidance is folded in (per Backlog BL-0022).

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

### Resolved (this turn)

- ~~V-Q2-followup.~~ **Resolved.** Effectively unclassed (Option C
  hidden + Option A emergent shaping). See §4.3.1.
- ~~V-Q2-quirks.~~ **Deferred.** "Mixed and unknown yet" — to be
  authored as the class arc emerges.
- ~~V-Q3-followup.~~ **Deferred.** "Unspecified" — source world is
  not pre-authored; discovered (or not) in late-game beats.
- ~~V-Q3-mechanism.~~ **Deferred.** "Unknown" — transport mechanism
  not pre-authored.
- ~~V-Q6-followup.~~ **Resolved.** "Common is common" — accept by
  setting convention; no special mechanism needed.
- ~~V-Q7-followup.~~ **Deferred.** Tattoo `08` meaning unknown to
  design; authored when its arc surfaces.
- ~~V-Q8-followup.~~ **Resolved.** Synthetic-from-prompts (no
  actor reference). Pipeline pending T-Q9.
- ~~V-Q9-followup.~~ **Resolved.** Canonical face designed **after**
  BL-0001 cel-shader spike completes.
- ~~V-Q10-followup.~~ **Resolved.** Sarenrae's chapel.
- ~~V-Q12.~~ **Resolved.** No archetype, surface-level only. See
  §4.3.
- ~~V-Q13.~~ **Resolved.** Looks human; modern outfit anachronism;
  pervasive "wrongness" everyone senses. See §4.4.

### Re-posed / Open

- ~~V-Q11.~~ **Resolved.** **Yes** — full export-menu committed.
- ~~V-Q11-followup.~~ **Resolved.** **All parallel.**
- ~~V-Q14.~~ **Resolved (initial batch).** Inspirations list. See §7.3.
- ~~V-Q15.~~ **Resolved.** Cinematic density = **BG3-frequent and
  more** — micro-moments throughout play **plus** episode-style
  set-pieces, anime-density. Cross-doc commitment: *Camera and
  Cinematography*, *Animation Pipeline*, *Audio*, *Performance
  Budget* now all sized for an upper-bound cinematic budget.
- ~~V-Q16.~~ **Resolved.** Two-channel "wrongness" — Magnetism
  (variable, especially women, single or not) + ambiguous Aura
  (good/bad polarity unreadable to most). See §4.4.1.
- ~~V-Q17.~~ **Resolved.** Openly atheist (Rahadoumi-style). See
  *Religion and Devotion* §3.1.

### New (this turn)

- **V-Q16-followup-A** **Magnetism scale** — confirm the four-band
  model (subliminal / noticed / infatuation / obsession) or pick a
  different shape; per-NPC growth curves; reset/decay rules; cap
  on simultaneous obsession-band NPCs (or no cap)?
- **V-Q16-followup-B** **Magnetism orientation override** — when a
  straight male NPC encounters Gherman, does the magnetism still
  apply (in a "I admire him / want to be like him" non-sexual way)
  or is the effect strictly attraction-tracked, applying only to
  NPCs whose orientation includes male partners?
- **V-Q16-followup-C** **Aura on first-meet randomness** — pure RNG
  per NPC, deterministic-from-NPC-personality, hybrid?
- **V-Q16-followup-D** **Aura visibility to player** — does the
  player ever see what an NPC's read polarity is, or stays
  diegetic-only (player must infer from NPC behavior)?
- **V-Q15-followup** **Cinematic density numeric anchor** — rough
  count per hour of play (3+ micro-moments, 1 episode-set-piece
  per hour, etc.) so *Performance Budget* can size the cinematic
  shader/anim budget concretely.
