# Sequel Project Kickoff From Approved Follow-On Concept

Use this when the author approves a proposed follow-on-book concept and asks to create a new project directory / start the process.

## Trigger

Signals include:

- “ok sounds good, create a new directory and start the process”
- “let’s do that as book 2”
- “use this sequel idea and start the project”

If the conversation immediately above contains a substantive sequel pitch that the author approves, treat that pitch as the Stage 0 seed. Do not ask the author to restate the seed.

## Workflow

1. Confirm the target path and create the new project directory under the requested series root.
2. Initialize standard directories:
   - `concepts/`
   - `characters/`
   - `settings/`
   - `research/`
   - `mission/`
   - `chapter-briefs/`
   - `chapters/`
   - `reviews/`
   - `exports/`
3. Create `concepts/seed.md` from the approved sequel pitch and carry forward explicit continuity anchors from the prior book.
4. Because the author has approved the concept and asked to start, proceed directly through Stage 1 in the same turn when feasible:
   - `concepts/stage-1-premise-options.md`
   - `reviews/stage-1-premise-review.md`
   - `concepts/stage-1-final-premise.md`
5. Update project tracking:
   - `AGENTS.md`
   - `progress.md`
   - `rolling-summary.md`
   - initialize `IDEAS.md` if no reference file exists.
6. Stop at the next author gate: approval to enter Stage 2.

## Review Requirements

Stage 1 still requires Alex, Morgan, and Vale. The review must state:

- required reviewers;
- missing reviewers: none;
- gate status;
- fixes applied;
- author decisions needed.

Do not skip the review because the author already liked the pitch. Their approval lets you use the pitch as seed and start the process; it does not remove the Stage 1 review gate.

## Continuity Requirements for Sequels

Capture prior-book carry-forward anchors in `concepts/seed.md`, `AGENTS.md`, and `rolling-summary.md`:

- unresolved character fates;
- relationship state;
- hidden-information state;
- antagonist status;
- title/series promise;
- safety and plausibility boundaries;
- any “do not reveal yet” constraints.

For a direct sequel, avoid treating the new project as blank-slate Stage 0. The prior book’s final `rolling-summary.md`, concerns log, and retrospective are valid seed context if available in the current conversation or accessible under the project root.

## Final Status Pattern

Report compactly:

- project directory;
- files created;
- directories created;
- current stage statuses;
- review verification;
- final premise hook;
- next required gate.

End with the next approval phrase/action, e.g. “Say `continue` to enter Stage 2 — Character and Cast Development.”
