# DESIGN — Workflow

> Living document. **Mandatory project-wide rules** for how the assistant
> and the user work together. These rules override any default behavior
> of the assistant. Reread before every working session.

---

## 1. The Core Rule

**The user decides everything. The assistant proposes, never disposes.**

This is not a polite preference. It is a **mandatory project-wide
workflow**, applied to:

- Vision and design decisions.
- Architecture and tech choices.
- Naming, file/folder layout, formatting.
- Content scope, lore reworks, mechanic interpretations.
- All Pathfinder / third-party content imports (extract by extract).
- Even *low-stakes* questions and decisions.

There are **no autonomous defaults**. There is **no "I'll just pick X
unless you object"** behavior.

## 2. The Q&A Loop

The standard rhythm of a working turn:

1. **Assistant asks** every question that needs answering for the
   current scope of work.
2. **User decides** — answers directly, or directs the assistant to
   suggest options.
3. **For uncertain questions, assistant suggests options** (with
   tradeoffs, not a recommendation-as-default), and the user picks.
4. **Assistant implements** only what was approved, only as approved.
5. **Assistant asks again** for the next decision.

This applies in:
- Pure design-doc work (everything goes in `DESIGN/`).
- Prototyping / vertical slice work.
- Content import extracts.
- Tech and tooling.
- Refactors.
- Naming.

## 3. Extract-by-Extract Content Import

When importing Pathfinder / third-party content, the protocol is:

1. The user provides an **extract** (a chunk of source content — a
   spell list, a class, a feat, a stat block, an NPC, a region, an AP
   chapter, etc.).
2. The assistant **reads it** and **asks every conversion question**
   raised by the extract:
   - Remaster shape vs source shape decisions.
   - Lore-rework alignment.
   - Naming, identity, tagging.
   - Where it slots into the data layer / plugin folder.
   - Edge cases.
3. The user answers / decides per extract.
4. The assistant **commits the converted record** with the user's
   decisions captured in the diff and (where relevant) in
   `DESIGN - Lore Reworks.md` or similar.
5. Move to the next extract.

Bulk autonomous conversion is **forbidden** unless the user has, for
that specific session, explicitly authorized batch behavior with
explicit rules. Defaults do not survive across extracts.

## 4. Ask Style Expectations

When the assistant asks questions, the assistant:

- **Asks tons of questions.** Surface as many as are genuinely needed;
  do not pre-trim for "user friendliness." The user prefers to see the
  full set and skip what they don't have opinions on.
- **Groups by cluster** so the user can answer one cluster at a time.
- **Numbers questions** so answers can be referenced by ID later
  (V-Q1, R-Q2, T-Q5, etc.).
- **Suggests options when the user is unsure** — multiple options
  with tradeoffs, *not* one recommendation framed as "default."
- **Records every decision** in the appropriate `DESIGN - <Domain>.md`
  doc. Decisions that don't make it into a design doc are forgotten.

## 5. Living Documentation

- All design decisions live in `DESIGN/` as `DESIGN - <Domain>.md`
  files, capitalized with spaces around the dash.
- Folders are capitalized.
- Cross-references use *italic Domain Name*.
- Each design doc ends with an **Open Questions** section using a
  per-doc prefix (V-Q, R-Q, L-Q, C-Q, M-Q, N-Q, A-Q, T-Q, etc.).
- The cross-doc registry of unresolved questions lives in
  `DESIGN - Open Questions.md`.
- When a question is resolved, it folds into the parent doc and is
  archived in `DESIGN - Open Questions.md`.

## 6. Two-Track Working Mode

Per the user's direction, work alternates between:

- **Design-doc mode** — pure documentation, no code, no commits to
  source folders. Used to mature a domain before implementation.
- **Prototyping mode** — vertical slices, throwaway code, spikes.
  Used to de-risk specific unknowns.

The mode is **declared at the start of a working session**. Modes can
switch within a session, but only with the user's explicit cue.

## 7. Throwaway / Speculative Code

- Allowed when used to de-risk an unknown.
- Must live in `Tools/Spikes/<topic>/` or branch `spike/<topic>`.
- Must include a `SPIKE.md` describing the question, the answer, and
  the disposition.
- **Must be removed** once real code addressing the same concern has
  been written and shipped to `main`. The user enforces this; the
  assistant proposes removal proactively when a spike's purpose is
  fulfilled.

## 8. Approval Discipline

- **Nothing ships without the user's explicit approval.** "Ships" =
  any commit to a stable branch, any inclusion of an asset in the
  game build, any conversion record entering the canonical data
  layer.
- The assistant may freely make commits **on the working branch**
  (currently `claude/pathfinder-game-design-hhWTr`) for design docs
  and spikes, since pushing to a feature branch is part of the
  working rhythm. But conceptual approval still precedes the doc
  capture.

## 9. AI Generation Discipline

For all dev-time AI generation (text, image, audio, voice, 3D, code):

- **Generated content is candidate, not canon**, until the user
  approves it.
- **Approval is per-asset / per-passage**, not blanket.
- **Iteration is the default**: first generation is rarely the final;
  the assistant should plan for revision rounds.
- **Hard line enforcement** (per *NSFW* §6): every NSFW generation
  pipeline includes a minor-content filter at generation time.

## 10. Anti-Patterns to Avoid

The assistant should **never**:

- Pick defaults silently for "low-stakes" choices and announce them.
- Assume a question is rhetorical and proceed.
- Bulk-import content without per-extract Q&A.
- Mark things "decided unless you object."
- Name folders or files with new conventions without asking.
- Promote a spike into "real" code without an explicit user decision.
- Hide questions to keep the response shorter — always surface them.

## 11. Cross-References

- *Index* — corpus map.
- *Open Questions* — current open registry.
- *Tech and Engine* — branching strategy and tooling implications.

## 12. Open Questions (Workflow-Local)

- **W-Q1.** Should `LORE`, `RULES`, and `BACKLOG` be **single files**
  at the project root (`LORE.md`, `RULES.md`, `BACKLOG.md`), or
  **folders** (`Lore/`, `Rules/`, `Backlog/`) containing
  domain-organized sub-files?
  - The user's stated organizational preference (capitalized folder
    names, neat sub-domains) leans toward folders, but the user said
    "files welcome." **Asking before creating.**
- **W-Q2.** Should `BACKLOG` use a specific format (Markdown checklist,
  task IDs, status tags, links to design docs)?
- **W-Q3.** Should `RULES.md` (project rules) be separate from
  `DESIGN - Workflow.md` (project workflow), or are they the same
  thing? "RULES" might mean "PF2e rules" (mechanics) instead — clarify.
- **W-Q4.** Working-session declaration ritual: do we explicitly type
  "design mode" / "prototyping mode" at session start, or do we
  infer from context?
- **W-Q5.** Approval acknowledgement style: do you want the assistant
  to summarize "here's what was decided this turn" at the end of
  every working session?
- **W-Q6.** Re-import policy: when a previously-imported extract is
  re-imported with different decisions, how do we handle history /
  diff / migration of dependent content?
