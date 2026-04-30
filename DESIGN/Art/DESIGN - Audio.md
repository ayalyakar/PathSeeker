# DESIGN — Audio

> Living document. Music, sound effects, voice (per *Art and Presentation*
> §5), ambient soundscape, scene-aware mood, and the audio dev-time
> production pipeline.

---

## 1. Stance

Audio carries half the immersion. Per the Vision pillar of tonal
flexibility, audio must be **scene-aware** — same scene, different
context, different mood.

Layers:
- **Music** — adaptive scoring per scene mode (heroic, melancholic,
  comedic, intimate, dread, ambient, festival, …).
- **SFX** — combat, environment, footsteps, magic, fabric, breath.
- **Ambient** — biomes, urban density, weather, crowd murmur.
- **Voice** — full English, AI-generated dev-time (per Q29 / *Art*
  §5).
- **NSFW audio** — breath, voice, body, environment; treated with
  the same fidelity as combat audio.

## 2. Music Direction

- Anime/JRPG sensibility consistent with Genshin/HSR/Persona/Hades
  references, but blendable.
- Per-region motifs (Cheliax: orchestral grandeur; Shoanti drum;
  Tian zither; Mwangi percussion; Osirion strings).
- Per-faction motifs (Pathfinder Society fanfare, Hellknight
  funereal, Calistria sensual, etc.).
- Per-NPC motifs for hero NPCs.

## 3. Voice Production

- **Dev-time AI generation** with user supervision and approval per
  line (per *Workflow* §9).
- Voice profiles per NPC (per A-Q11 — moot consent constraints per
  Q33; technical sourcing still TBD via T-Q9 / T-Q10).
- Lip-sync per A-Q12.

## 4. Cross-References

- *Art and Presentation* §5 — voice acting source.
- *NPCs and Companions* — per-NPC voice profiles.
- *World Simulation* — weather/time-of-day audio shifts.
- *NSFW* — intimate audio.
- *Performance Budget* — audio memory/streaming budget.
- *Tech and Engine* T-Q9 — TTS toolchain.

## 5. Open Questions (Audio-Local)

- **AU-Q1** Music engine — adaptive vertical-remix (FMOD/Wwise-style),
  horizontal scene-driven, hybrid?
- **AU-Q2** Music sourcing — fully composed (human / AI dev-time),
  procedural-generated, mix?
- **AU-Q3** Per-region motif inventory — list and own?
- **AU-Q4** Per-faction motif — list and own?
- **AU-Q5** Per-NPC motif fidelity — only hero NPCs, or extend to
  named?
- **AU-Q6** Combat music handling — Souls-style "boss-only," Persona-
  style "every encounter," Skyrim-style "always music," none?
- **AU-Q7** Intimate-scene music — distinct genre slot, character-
  motif variation, ambient-only?
- **AU-Q8** Scene transitions — hard cuts vs cross-fade vs musical
  rests?
- **AU-Q9** Foley density — every footstep / cloth-rustle / object
  pickup / ?
- **AU-Q10** Material-based footstep system — surface × footwear?
- **AU-Q11** Ambient soundscape system — pre-baked per zone, layered
  procedural?
- **AU-Q12** Spell SFX consistency — per-school/tradition signatures?
- **AU-Q13** NSFW audio sourcing — recorded from open-source samples,
  AI-generated, hand-recorded?
- **AU-Q14** Voice line bank size per NPC (combat barks, ambient
  barks, conversation)?
- **AU-Q15** Voice line generation cadence — bake-on-demand vs all-
  pre-baked?
- **AU-Q16** Voice cloning model choice (T-Q9 mirrors).
- **AU-Q17** Lip-sync method (A-Q12 mirrors).
- **AU-Q18** Multi-character dialogue audio mixing (positional, head-
  related transfer)?
- **AU-Q19** Crowd murmur engine — pre-recorded loops vs procedural
  layered?
- **AU-Q20** UI sound design — Persona-loud vs minimalist diegetic?
- **AU-Q21** Audio accessibility — subtitles, audio descriptions,
  visual sound indicators (even though personal project)?
