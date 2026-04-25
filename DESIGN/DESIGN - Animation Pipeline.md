# DESIGN — Animation Pipeline

> Living document. Body, facial, intimate, combat, cinematic animation.
> Pulled out of *Art and Presentation* §1 because animation is its own
> production craft.

---

## 1. Stance

Cel-shaded anime fidelity at AAA scale (per *Art* §1.1) demands a
**robust animation pipeline** with multiple layers:

- **Body animation** (locomotion, combat, climbing, sitting,
  carrying, sleep).
- **Facial animation** (expressions, lip-sync, micro-tells).
- **Hand / finger animation** (object handling, gesture).
- **Cloth / hair simulation**.
- **Intimate animation** (per *NSFW* §2 — full-3D scenes).
- **Combat animation** (weapon-art moves, hit reactions, dodges).
- **Cinematic animation** (cutscene authoring).

## 2. Pipeline (proposed)

```
[Concept]   →   [Reference]   →   [Block]   →   [Polish]   →   [Review]   →   [Ship]
   │              │                │             │              │              │
 Storyboard,    motion-cap        rough         tuned          user           game-loaded
 references    or AI-mocap-       keyed         & secondary    approval       via animator
                from-video        animation     motion         per scene      controller
```

## 3. Tools (candidates)

- **Blender** for hand-keyed work.
- **Mixamo** for body retargeting baseline.
- **Cascadeur** for combat/physics-aware.
- **AI motion-capture** (RADiCAL, etc.) — drafts.
- **Koikatsu / HoneySelect 2** export pipelines (per T-Q11 — pending).
- **Daz / CharacterCreator** (per T-Q11).
- **Custom rig** as the long-term state.

## 4. Cross-References

- *Art and Presentation* — visual style.
- *Camera and Cinematography* — camera-coupled animations.
- *NSFW* — intimate animation fidelity.
- *Body and Identity* — body-state animation overlays.
- *Combat* — weapon arts, hit reactions.
- *Tech and Engine* T-Q11 — character pipeline base.

## 5. Open Questions (Animation-Local)

- **AN-Q1** Base rig — humanoid universal vs per-ancestry?
- **AN-Q2** Facial system — blendshape, bone, hybrid (mirrors A-Q4)?
- **AN-Q3** Lip-sync (mirrors A-Q12).
- **AN-Q4** Hair (mirrors A-Q5) — card hair, strand hair, hybrid?
- **AN-Q5** Cloth (mirrors A-Q6) — physics, baked, hybrid?
- **AN-Q6** Skin shader for intimate (mirrors A-Q7).
- **AN-Q7** Combat animation count — minimum viable per weapon
  group?
- **AN-Q8** Hit reactions — directional, per-location, generic?
- **AN-Q9** Locomotion — root-motion vs in-place?
- **AN-Q10** Climbing / parkour set — full system vs cinematic
  triggers?
- **AN-Q11** Sitting / lying / in-furniture animations — full set
  per furniture type?
- **AN-Q12** Object interaction — hand IK on every grabbable item?
- **AN-Q13** Intimate animation library size — target scope?
- **AN-Q14** Per-partner-ancestry intimate animations — every
  combination, common-only, abstracted?
- **AN-Q15** Pregnancy belly progression visible (BI-Q7) —
  shape-key driven?
- **AN-Q16** Body-state interaction with combat anim (injured stance,
  fatigued swing)?
- **AN-Q17** Companion animation — same fidelity as PC?
- **AN-Q18** NPC animation tier (per NPC-Q tier) — fidelity scales?
- **AN-Q19** AI-motion-cap usage policy at dev-time?
- **AN-Q20** Animation review and approval flow?
- **AN-Q21** Performance budget for active animated bodies on screen
  (PB-Q)?
