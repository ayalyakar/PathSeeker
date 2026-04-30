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

### 1.1 Carve-out: Backlog autonomy

The **only standing exception** to §1: the assistant **autonomously
adds, edits, completes, archives, and removes** tasks in `Backlog/`
files as work proceeds. The user reviews via diffs at commit time
rather than approving each Backlog edit per task.

This carve-out applies **only to** files inside the `Backlog/` folder.
Every other folder (DESIGN/, Lore/, Rules/, Content/, Engine/, etc.)
remains under §1 strict approval discipline.

The carve-out exists because the Backlog is by design a high-velocity,
low-stakes operational artifact — task lists need to track work in
real-time without becoming a bottleneck. Standing approval is granted
once here, captured in this section.

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
- Folders are capitalized; multi-word folder names use spaces.
- Cross-references use *italic Domain Name*.
- Each design doc ends with an **Open Questions** section using a
  per-doc prefix (V-Q, R-Q, L-Q, C-Q, M-Q, N-Q, A-Q, T-Q, W-Q, etc.).
- The cross-doc registry of unresolved questions lives in
  `DESIGN - Open Questions.md`.
- When a question is resolved, it folds into the parent doc and is
  archived in `DESIGN - Open Questions.md`.

### 5.1 Sibling Project Folders (resolved W-Q1, W-Q3)

> **`Lore/`, `Rules/`, `Backlog/` are folders, each containing
> `<Folder> - <Sub>.md` files.** Same convention as `DESIGN/`.

Disambiguated meanings:

- **`Lore/`** — the in-fiction Golarion content corpus (canon as we
  use it, plus our reworks in-place). Files like `Lore - Cosmology.md`,
  `Lore - Inner Sea Region.md`, `Lore - Reworks.md`, etc. The
  *design discussion* about lore reworks lives in
  `DESIGN/DESIGN - Lore Reworks.md`; the *content* lives in `Lore/`.
- **`Rules/`** — the **PF2e mechanical rules reference** for our
  project. Two layers:
  - **Untouched PF2e Remaster rules** as the canonical reference
    (e.g., `Rules - Conditions (Untouched).md`, `Rules - Combat
    Actions (Untouched).md`).
  - **Project-reworked rules** documenting our adaptations to
    real-time, alchemical magic, etc. (e.g., `Rules - Combat
    (Project).md`, `Rules - Magic Resource (Project).md`).
  - The *design discussion* about rules lives in `DESIGN/`; the
    *consolidated reference* lives in `Rules/`.
- **`Backlog/`** — actionable tasks only. No design discussion.
  Files like `Backlog - Engine.md`, `Backlog - Content Pipeline.md`,
  `Backlog - Spikes.md`. Format pending W-Q2.

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

## 11. Session-Start Ritual (resolved W-Q4, W-Q5, W-Q6)

At the start of every working session, the assistant proactively
asks the user three questions before any other work:

1. **Mode declaration (W-Q4).** *"Are we in **design-doc mode**,
   **prototyping mode**, **content-import mode**, or **mixed**
   today — and what's the focus?"*
2. **Last-session summary check (W-Q5).** *"Brief recap of what
   was decided last session — anything you want to revisit before
   we move forward?"*
3. **Re-import cadence (W-Q6).** *Only if prior content extracts
   exist:* *"Are there extracts you want re-imported with updated
   decisions, or are we forward-only this session?"*

These three questions take seconds; they reset shared state, surface
buried disagreements, and prevent drift between sessions. The user's
answers define the implicit "scope of this session," which the
assistant respects until explicit re-scoping.

The session-start ritual applies to **every** working session,
regardless of how short. Even a five-minute session starts with
the ritual.

## 12. Cross-References

- *Index* — corpus map.
- *Open Questions* — current open registry.
- *Tech and Engine* — branching strategy and tooling implications.

## 13. Open Questions (Workflow-Local)

- ~~W-Q1.~~ **Resolved.** `Lore/`, `Rules/`, `Backlog/` are folders
  with `<Folder> - <Sub>.md` sub-files. See §5.1.
- ~~W-Q2.~~ **Resolved.** Backlog format = `BL-NNNN` global IDs,
  checkbox `[ ]`/`[x]` (no status tags), autonomous edits per §1.1.
  See `Backlog/Backlog - Index.md`.
- ~~W-Q3.~~ **Resolved.** `Rules/` = PF2e mechanical rules (untouched
  reference + project-reworked layer). Project laws/workflow live in
  *Workflow*, not in `Rules/`. See §5.1.
- ~~W-Q4.~~ **Resolved.** Explicit mode declaration at session start
  via the §11 ritual.
- ~~W-Q5.~~ **Resolved.** Last-session summary check at session
  start (rather than end-of-session summary) per §11.
- ~~W-Q6.~~ **Resolved.** Re-import cadence asked at session start
  per §11; re-imports are diff-and-migrate (handled per-extract).
