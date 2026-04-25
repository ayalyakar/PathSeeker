# DESIGN — Dialogue and Conversation

> Living document. The interface for talking to NPCs: scene framing,
> branching, persuasion, NPC personality filtering, voice playback,
> camera handling, and pacing.
>
> Distinct from *NPCs and Companions* (the brain) and *Romance and
> Relationships* (the emotional layer).

---

## 1. Stance

A conversation is a **scene** — camera, framing, voice, NPC
expression, response choice. Real-time-but-paused (or with limited
real-time pressure for high-stakes scenes).

The player's input modes:
- **Dialogue choices** (classic branch tree),
- **Persuasion** (PF2e Diplomacy / Intimidation / Deception with
  visible DC framing),
- **Topic injection** (recall topics — quests, rumors, gossip,
  knowledge),
- **Item/show** (present an object, show a wound),
- **Body language** (posture, eye contact, distance — first-person
  affords this).

NPC responses are **personality-filtered** (per *NPCs and
Companions*) and **voiced**.

## 2. Scene Camera

Per *Camera and Cinematography* — locked or framed during dialogue
(per Q27). Default framing: BG3-style over-the-shoulder, with
occasional close-ups for emphasis. First-person retained for casual
exchanges.

## 3. Cross-References

- *NPCs and Companions* — who's talking and why.
- *Camera and Cinematography* — scene framing.
- *Audio* — voice playback.
- *Skill Checks and Exploration* — Diplomacy/Intimidation rolls.
- *Romance and Relationships* — relationship-aware dialogue.
- *Dialogue Pipeline* (a possible CP sub-doc) — authoring shape.

## 4. Open Questions (Dialogue and Conversation-Local)

- **DC-Q1** Authoring format — branching tree (BG3), Yarn/Ink/Twine,
  custom DSL?
- **DC-Q2** Persuasion DC visibility — show numeric DC, show
  pass/fail tier, hide entirely?
- **DC-Q3** Failure consequences — visible feedback, hidden
  reputation hit, narrative-only?
- **DC-Q4** Real-time pressure — does an NPC react to silence,
  hesitation, walking away mid-conversation?
- **DC-Q5** Repeated dialogue — how do we prevent "talked-out"
  feeling (rotating barks, conversation cooldowns)?
- **DC-Q6** Topic UX — Morrowind-style topic list, Mass-Effect-style
  hub, organic-only?
- **DC-Q7** Voice playback — full VO required for every line, or
  some lines text-only?
- **DC-Q8** Lip-sync precision (A-Q12 mirrors).
- **DC-Q9** First-person free-look during dialogue — allowed (player
  can look at the room while NPC talks)?
- **DC-Q10** Multi-NPC conversation — handled (BG3-style), only one
  active speaker, both?
- **DC-Q11** Eavesdropping — first-class system (overhear NPCs
  talking)?
- **DC-Q12** Telepathy / *message* / etc. — surfaced as alternate
  conversation channel?
- **DC-Q13** Lying / deception — does the player see "LIE" tags,
  or is detection emergent from NPC Sense Motive?
- **DC-Q14** Truth-detection (zone of truth, etc.) — modeled as
  conversation modifier?
- **DC-Q15** NPC Sense Motive vs player deception — visible roll?
- **DC-Q16** Conversation history — does the journal record
  conversations? Player can re-read?
- **DC-Q17** Conversation-aware NPC (recalls earlier statements
  by player) — depth?
- **DC-Q18** AI-drafted conversation generation dev-time (NPC-Q35
  mirrors) — when, supervised how?
- **DC-Q19** Translation handling — when player speaks one language
  and NPC another, what does the player see/hear?
- **DC-Q20** Companion interjections — companions chime in during
  player conversations?
