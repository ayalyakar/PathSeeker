---
id: module:hlh:01-adventure-background
plugin: module:hollow-last-hope
type: adventure-background
source:
  book: Hollow's Last Hope
  publisher: Paizo
  year: 2008
  edition: PF1e
  page: 3
  section: Adventure Background
remaster_converted: true
remaster_changes:
  - "No mechanical content in this extract; conversion is narrative-only."
  - "Iomedae portfolio language ('valor, justice, and honor') is already
    Remaster-compatible; preserved verbatim per D-002."
  - "Disease-cure / failed-prayer framing left flagged; final mechanical
    interpretation deferred until full sourcebook is imported (D-003)."
  - "Original module assumes generic adventurer PCs; in our project the
    'heroes' NPCs (TBD) take that slot. Gherman is a secondary PC; see
    D-009. This extract's framing of 'no townsfolk dare venture' is
    preserved verbatim — the heroes (and possibly Gherman alongside them)
    are the ones who do."
  - "Narrative timing: this extract describes events of HLH chapter 2.
    Per D-001, Gherman's awakening is set BEFORE the outbreak; this
    background applies to the SECOND chapter of his arc, not the first."
references:
  locations:
    - lore:falcons-hollow
    - lore:falcons-hollow:brookmans-well
    - lore:darkmoon-vale
  npcs:
    - lore:laurel
    - lore:falcons-hollow:dead-town-elder      # flavor NPC; deceased
  diseases:
    - lore:blackscour
    - lore:blackscour:wheezing-death           # folk-name alias
  factions:
    - lore:falcons-hollow-constabulary
    - lore:church-of-iomedae-falcons-hollow
  deities:
    - lore:iomedae
imports:
  - lore:falcons-hollow
  - lore:iomedae
  - lore:darkmoon-vale
project_links:
  - vision:protagonist                          # V-Q10 retconned to Iomedae church (D-004)
  - vision:anime-story-basis                    # §7 — Gherman ch.1 slice-of-life, HLH triggers ch.2 (D-001)
  - vision:secondary-pc-framing                 # §4.6 — Gherman secondary, heroes are MCs (D-009)
  - lore-reworks:LR-002                         # rationalist magic — see deferred D-003
  - religion-and-devotion:3.1                   # atheist Gherman vs Iomedaean clergy
decisions:
  - id: D-001
    question: "Narrative timing of Hollow's Last Hope vs Gherman's awakening (turn Q: Narrative Timing)"
    answer: "Option B — Gherman wakes BEFORE outbreak; slice-of-life onboarding chapter, then HLH triggers as chapter 2"
    rationale: "Lets the player meet Falcon's Hollow at peace before the crisis; provides the slice-of-life balance per V-Q14 inspirations (My Dress-Up Darling); preserves canonical HLH events without skipping them."
  - id: D-002
    question: "Iomedae portfolio phrasing (turn Q1)"
    answer: "Preserve verbatim — 'goddess of valor, justice, and honor'."
    rationale: "Already Remaster-compatible; no alignment language; no rework needed."
  - id: D-003
    question: "Failed-prayer framing — how Iomedae's prayers fail to cure blackscour under rationalist magic (turn Q2)"
    answer: "DEFERRED. Leaning Option C (both local-capacity AND disease-specific framing). Final decision waits for complete HLH sourcebook injection."
    rationale: "Need to see how the rest of HLH frames blackscour mechanics before committing. Captured here so the deferral is traceable."
  - id: D-004
    question: "Sarenrae chapel vs Iomedae church coexistence in Falcon's Hollow (turn Q3)"
    answer: "Option C — Iomedae church only. Gherman's waking RELOCATED from Sarenrae's chapel to Iomedae's church."
    rationale: "Heightens immediate tension: atheist Gherman (V-Q17) wakes at the austere goddess-of-valor-justice-honor's church, opening confrontation with Iomedaean clergy on day one. Stronger anime-story hook than the gentler Sarenrae version. Matches canonical Falcon's Hollow."
    consequence: "Vision §4.2/§4.3 V-Q10 retconned. Religion and Devotion §3.1 updated. BL-0016 closed (re-resolved)."
  - id: D-005
    question: "Laurel handling (turn Q4)"
    answer: "Capture as Named-NPC stub now (Option A)."
    rationale: "First named NPC encountered in any extract; load-bearing for HLH chapter 2."
    consequence: "Lore - NPC - Laurel.md created."
  - id: D-006
    question: "Capture-now or defer for surface entities (turn Q5)"
    answer: "Capture all now: Brookman's Well, Blackscour, Wheezing Death (alias), dead town elder (flavor), Falcon's Hollow Constabulary, Church of Iomedae (Falcon's Hollow chapter)."
    rationale: "User explicitly directed."
    consequence: |
      Created stubs:
        - Lore - Falcon's Hollow.md  (with Brookman's Well + dead elder sub-sections)
        - Lore - Disease - Blackscour.md  (with Wheezing Death alias)
        - Lore - Faction - Falcon's Hollow Constabulary.md
        - Lore - Faction - Church of Iomedae (Falcon's Hollow).md
  - id: D-007
    question: "Frontmatter shape and dual-section preservation (turn Q6, Q7)"
    answer: "Frontmatter shape OK. Dual-section preserved: Source text (verbatim) + Project-canon converted text. Decisions log in frontmatter (Q8)."
    rationale: "Lossless source preservation per Content Pipeline goal; re-derivation is possible if conversion rules evolve."
  - id: D-008
    question: "Apostrophe handling in slugs (turn Q9)"
    answer: "Strip apostrophe, no separator: falcons-hollow, brookmans-well, laurels-shop. Filenames retain apostrophe (Falcon's Hollow); slugs do not."
    rationale: "User Q9 → second option."
  - id: D-009
    question: "MC framing — Gherman as PC vs Gherman as story protagonist (turn directive)"
    answer: "Gherman is the playable PC but is treated as a SECONDARY narrative character. The 'heroes' NPCs (yet to be defined) are the anime story's MCs."
    rationale: "User directive this turn. Reframes anime-story output (cinematics spotlight heroes), reframes V-Q12 anime archetypes (attach to heroes not Gherman), reframes V-Q11 export tooling (heroes as featured subjects), reframes how AP/Module 'PC slots' are filled (heroes go in by default)."
    consequence: "Vision §4.6 added. NPCs and Companions §2 'MC NPC' tier added above Hero NPC. New V-Q18+ tracks heroes definition."
  - id: D-010
    question: "Schema strictness for first extracts"
    answer: "Provisional/loose schema: frontmatter + body, no hard validation. Schemas tighten as more extracts of each type arrive (per CP-Q2)."
    rationale: "Avoids premature lock-in; lossless source preservation gives re-derivation options if we tighten the schema later."
---

# Hollow's Last Hope — Adventure Background

## Source text (verbatim, lossless)

> Adventure Background
>
> In the past week, numerous residents of
> Falcon's Hollow have fallen ill, each suf-
> fering from the same hacking affliction.
> Local remedies prove as useless as prayers
> at the Church of Iomedae, goddess of valor,
> justice, and honor, and already at least
> one town elder has been claimed by the
> wheezing death.
>
>  Fortunately for Falcon's Hollow, a canny
> local herbalist named Laurel has traced the
> source of the malady to Brookman's well,
> a small spring on the edge of town, and a
> rare fungus called blackscour. By banning
> the use of the spring, the town constabu-
> lary hopes to prevent further infection, but
> such measures offer little respite to those
> already afflicted.
>
>  While Laurel has attempted numerous
> treatments, she has been unable to cure
> the disease. She lacks the reagents to brew
> one last unusual medicine, though all the
> necessary elements can be found within
> nearby Darkmoon Vale. Thus far, though,
> no townsfolk have dared to venture into the
> wooded reaches and secure the ingredients
> for this potential cure.

(Source: *Hollow's Last Hope*, Paizo, 2008, p. 3, "Adventure
Background." Line breaks reflect the original PDF's two-column
layout; word splits like *suf-/fering* and *constabu-/lary* are
PDF artifacts preserved here for lossless re-derivation.)

## Project-canon converted text

In the past week, numerous residents of Falcon's Hollow have
fallen ill, each suffering from the same hacking affliction.
Local remedies prove as useless as prayers at the Church of
Iomedae, goddess of valor, justice, and honor, and already at
least one town elder has been claimed by the *wheezing death*.

Fortunately for Falcon's Hollow, a canny local herbalist named
Laurel has traced the source of the malady to Brookman's Well, a
small spring on the edge of town, and a rare fungus called
*blackscour*. By banning the use of the spring, the town
constabulary hopes to prevent further infection, but such
measures offer little respite to those already afflicted.

While Laurel has attempted numerous treatments, she has been
unable to cure the disease. She lacks the reagents to brew one
last unusual medicine, though all the necessary elements can be
found within nearby Darkmoon Vale. Thus far, though, no
townsfolk have dared to venture into the wooded reaches and
secure the ingredients for this potential cure.

(Conversion notes: text is structurally identical to source —
PF1e to Remaster requires no narrative rework here. Word
de-hyphenation only.)

## Notes

### Narrative placement (per D-001)

This Adventure Background describes the events of **chapter 2 of
Gherman's arc**, not chapter 1. The slice-of-life chapter 1
(Gherman waking up, recovering, meeting Falcon's Hollow at peace)
runs *before* the outbreak begins. The disease arrives as the
first major narrative jolt of Gherman's residence in town.

### Secondary-PC framing (per D-009)

The original module assumes the player party are the adventurers
who venture into Darkmoon Vale to retrieve blackscour reagents.
In our project:
- The **heroes NPCs** (TBD — see V-Q18+) are the canonical
  adventurers slotting into that role.
- **Gherman** participates as a secondary character — supporter,
  observer, complicating presence, possibly a love-interest or
  rival to one of the heroes, depending on emergent play.
- The anime-story output frames the heroes as the MCs of the
  HLH arc; Gherman appears as a side character with his own
  parallel beats (his atheism vs the Iomedaean clergy, his V-Q16
  magnetism affecting Laurel and townsfolk, his isekai mystery
  sometimes intersecting the disease arc — pending design).

### Iomedae church opening (per D-004)

Gherman wakes up not at Sarenrae's chapel (previous V-Q10
resolution) but at **the Church of Iomedae in Falcon's Hollow**.
Implications:
- The Iomedaean clergy who saved his life are stern, valor-coded,
  honor-bound — the antithesis of Gherman's apathetic-cynical
  baseline (V-Q8) and atheist stance (V-Q17).
- The clergy will press him on his lack of faith, his lack of
  origin, his strange "wrongness" (V-Q16 aura).
- His tattoo `08` (V-Q7) will be noticed and possibly read by
  Iomedaean detection — distinctively but ambiguously.
- The first NPC interactions are loaded with three-way tension:
  duty (clergy), atheism (Gherman), and Magnetism (V-Q16) pulling
  individual clerics toward him despite their disapproval.

### Failed-prayer framing — DEFERRED (per D-003)

The original text says Iomedaean prayers are "useless" against
blackscour. In our rationalist-magic Golarion (LR-002), divine
*heal* spells are empirically real — so the failure must have a
cause. Leaning explanation:
- **Local capacity** — the Falcon's Hollow chapter has only
  low-rank clerics; rank-1/2 *heal* doesn't suppress blackscour.
- **Disease resistance** — blackscour is a magically-resistant
  fungal pathogen; resists divine cures below some threshold.

Final decision waits for the full HLH sourcebook injection so we
can see how the cure mechanic is structured.

### Cross-references

- *Vision* §4.2 (origin framing), §4.3 (V-Q10 starting location),
  §4.6 (secondary-PC directive), §7 (anime story basis).
- *Religion and Devotion* §3.1 (Gherman's atheist stance, now at
  Iomedae church).
- *Lore Reworks* LR-002 (rationalist magic — affects D-003).
- *Lore - Falcon's Hollow* (canonical town).
- *Lore - Disease - Blackscour* (the disease).
- *Lore - NPC - Laurel*.
- *Lore - Faction - Falcon's Hollow Constabulary*.
- *Lore - Faction - Church of Iomedae (Falcon's Hollow)*.
- Backlog BL-0026 (Falcon's Hollow lore — partially done by this
  extract).
