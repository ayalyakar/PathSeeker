# DESIGN — Art and Presentation

> Living document. Captures visual style, perspective, UI direction, and
> voice acting strategy.

---

## 1. Visual Style

**Cel-shaded, anime-inflected**, sourced from a deliberate blend of:

| Reference | What it contributes |
|---|---|
| **Genshin Impact / Honkai Star Rail** | Polished anime cel-shading at scale, hair/skin lighting model, expressive faces |
| **Koikatsu / Illusion** | Intimate-scene character fidelity, softer skin shaders, anime-eroge framing |
| **Ni no Kuni (II)** | Ghibli softness, painterly environments, warmth |
| **Persona (5 specifically)** | UI flair, posing, motion-graphic transitions, color confidence |
| **Hades** | Hand-painted illustration energy, character readability, lighting drama |

The synthesis target: **a Genshin-grade real-time renderer** dressed in
**Hades-grade illustration confidence**, capable of holding up at
**Koikatsu-level intimacy**, with **Ni no Kuni warmth** and **Persona's
UI swagger**.

This is a high bar. It implies a custom or heavily-modified anime PBR
shader stack, ramp lighting, signed-distance-field outlines, real-time
specular hair, and a robust facial-rig system. See *Tech and Engine*
(pending) for stack implications.

## 2. 2D / 2.5D / 3D

- **3D-rendered-to-feel-2D** is the working hypothesis.
- Whether we additionally use **billboard sprites**, **pre-rendered
  backgrounds** (FFVII-OG style), **hand-painted skyboxes/dressing**,
  or **paper-mario-style cutout populations** for crowd density —
  **TBD**.
- Constraint: NSFW scenes use the same 3D characters as gameplay
  (per *NSFW*), so the **main character pipeline is fully 3D, fully
  rigged, fully animated**. 2.5D tricks are reserved for environment,
  background, and possibly distant NPC LODs.

## 3. Perspective and Camera

- **First-person** as the default play perspective.
- **Completely free-look** outside of dialogue and specific scripted
  interactions.
- **Camera-locked / framed** during:
  - Dialogue scenes (cinematic over-the-shoulder, third-person, or
    locked first-person framing as scene calls for).
  - Cinematic sequences.
  - NSFW scenes (multi-angle directed framing).
  - Specific interactions that benefit from authored shots
    (rituals, ceremonies, executions, key story beats).
- **Camera transition** between FP free-look and locked scene framing
  must be smooth and authored — never jarring. This is itself a
  craft area.
- **No third-person free-roam camera** by default. (Possible
  *photo mode* / mirror-and-window check exception — TBD.)

## 4. UI

- **Mostly modern, diegetic in-world** UI.
- "Diegetic" means: when possible, the UI lives in the fiction —
  a journal in your hand, a map you actually unfold, a rune circle
  you drag glyphs into to cast, an inventory shown as your bag
  spilling on a table, a relationship "tracker" that's actually a
  scrapbook, a quest log that's actually letters and notes.
- "Modern" means: when the diegetic version would frustrate
  ergonomics, we layer crisp modern UI elements (clean typography,
  modern animation curves, motion-graphic feedback à la Persona).
- The **magic UX** specifically gets bespoke high-quality interface
  treatment (per *Magic*).
- **HUD minimalism** is the default — no permanent health bars,
  minimaps, or quest markers cluttering the screen. Information
  surfaces on demand or contextually (heartbeat for low HP, audio
  cues, environmental signaling, NPC dialogue).
- **Accessibility**: even with diegetic emphasis, a parallel
  classical-UI overlay must be available for ergonomic plays.

## 5. Voice Acting

- **AI-generated, full English VO**, produced **at dev time** (not
  realtime).
- Implication: every line of dialogue — including procedurally
  generated and LLM-driven content — needs a TTS pipeline. For
  procedural content, this is either:
  - (a) Realtime TTS with high-quality cloned voices (heavier
    runtime), or
  - (b) Bake-on-first-encounter TTS (lighter runtime, larger disk),
  - (c) Hybrid (key story lines pre-baked, ambient barks realtime).
- **Voice casting**: each named NPC gets a voice (cloned from
  voice-actor consent / synthetic / public-domain training).
- **Localization**: English-first; translation/dub strategy TBD.
- See *Tech and Engine* (pending) for TTS stack choices.

## 6. Audio (Adjacent)

Not strictly under "Art and Presentation" but called out for
visibility:

- Music must be **scene-aware** to support tonal whiplash (Vision
  §3): heroic, melancholic, comedic, intimate, dread, ambient.
- **Diegetic audio** for spells, footsteps, fabric, breathing,
  weather, urban density.
- A separate `DESIGN - Audio.md` will be created when work begins.

## 7. Cross-References

- *Vision* — tonal flexibility constraints on lighting/music.
- *Combat* — camera handling during real-time combat.
- *Magic* — bespoke spellcasting interface.
- *NSFW* — full 3D scenes must reuse the gameplay rigs.
- *Tech and Engine* (pending Q30–Q44) — shader stack, TTS, render budget.

## 8. Open Questions (Art-Local)

- A-Q1. 2.5D mix specifics — billboards / pre-rendered / hand-painted
  layers vs all 3D.
- A-Q2. Outline technique — geometry, post-process, SDF, hybrid.
- A-Q3. Cel-shading lighting model — Genshin-style ramp, Guilty-Gear
  per-pixel hand-painted, Persona-style flat, custom blend.
- A-Q4. Facial animation pipeline — blendshape, bone, hybrid, ARKit-
  style capture for cinematics?
- A-Q5. Hair — card hair, strand hair, hybrid?
- A-Q6. Cloth simulation — physics, tag-based posing, baked, hybrid?
- A-Q7. Skin shader for intimate scenes — sub-surface scattering,
  contact-AO, sweat/oil layers?
- A-Q8. Photo mode / mirror / cosmetic-check camera exception?
- A-Q9. UI key locations — does the player have a literal in-world
  *journal/grimoire/wrist-device/spell-tome* the camera sees?
- A-Q10. Persona-style menu transitions — yes/no/style-only-on-key-
  moments?
- A-Q11. Voice cloning consent policy — what voice sources are
  acceptable for the project? (Public-domain only, paid synthetic
  voice services, custom voice-actor licenses, all of the above?)
- A-Q12. Lip-sync — phoneme-driven from audio, or animator-authored?
- A-Q13. Render target framerate / resolution baseline.
- A-Q14. Day/night and weather fidelity — full dynamic, time-of-day
  baked, hybrid?
