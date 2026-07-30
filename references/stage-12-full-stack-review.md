# Stage 12 — Act / Whole-Book Full-Stack Review

Use when Stage 11 is complete and the next action is an act-break or whole-book full-stack review. This is a review-and-handoff stage, not a default manuscript-rewrite stage.

## Trigger

- `progress.md` / `AGENTS.md` says current or next stage is Stage 12.
- The user says `continue`, `implement actions`, or similar while Stage 12 is the next required action.
- Stage 11 carry-forward items include act/full-book review, unresolved-status verification, hidden-institution opacity, pacing, or full-stack checks.

## Required Inputs

Read only the necessary narrow context first:

1. `progress.md` current state and counts.
2. `AGENTS.md` current stage/carry-forward.
3. Stage 11 review file.
4. `rolling-summary.md` current whole-book state.
5. The relevant act scene file, chapter-outline excerpt, and story-structure excerpt for the act being reviewed.
6. Run `wc -w` / file counts and targeted watchlist scans for the act under review.

## Review Scope

Stage 12 assesses:

- pacing
- escalation
- stakes
- protagonist agency
- antagonist pressure
- team dynamics / coalition geometry
- plausibility / authority boundaries
- emotional cost
- safety boundary
- series-launch setup if reviewing the final act

For a final-act / whole-book review, explicitly check:

- whether the ending satisfies the current book without over-resolving the series engine
- whether unresolved statuses are deliberate and visible
- whether the hidden institution remains unnamed, unexplained, and unknown to Stuart if that is a project constraint
- whether any lean bridge chapters need Stage 13 expansion, rather than editing them inside Stage 12 by default

## Required Reviewers

Baseline Stage 12 reviewers:

- Alex — structure, pacing, payoff
- Morgan — reader satisfaction and confusion
- Casey — continuity and open threads
- Hayes — military/authority plausibility
- Vale — intelligence/geopolitical logic
- Jordan — prose/pacing/readability

Add:

- Quinn for safety / fact-boundary review
- Cross for climax/action/consequence readability

## Output File

Write a review file under `reviews/`, e.g.:

- `reviews/stage-12-act-3-whole-book-full-stack-review.md`

Required sections:

- Deliverable Info
- Gate Status
- Verification Snapshot
- criteria table for the full-stack checks
- reviewer sections with issues, hard questions, reservations, approval position
- Fixes Applied
- Author Decisions Needed
- Dissent / Unresolved Concerns
- Next Required Step

## Fix Policy

Do not reflexively rewrite manuscript chapters during Stage 12. Apply manuscript edits only when a Stage 12 finding is a clear blocker and does not require an author-only creative decision.

Most Stage 12 reservations become Stage 13/14 carry-forward items, such as:

- evaluate expansion/texture for lean chapters
- preserve hidden-institution opacity
- preserve unresolved statuses
- ensure partial victory reads as satisfying
- line-edit legacy prose/watchlist terms later

If there are no blockers, mark Stage 12 PASS WITH RESERVATIONS and advance tracking to Stage 13.

## Tracking Updates

After writing the Stage 12 review:

1. Update `progress.md`:
   - current stage becomes Stage 13
   - Stage 12 status COMPLETE — PASS WITH RESERVATIONS
   - review file count increments
   - Stage 12 checklist/output is recorded
   - next required action becomes Stage 13 — Developmental Edit
2. Update `AGENTS.md` with Stage 12 result and carry-forward.
3. Update `rolling-summary.md` with a compact Stage 12 audit state.
4. Verify:
   - chapter count
   - review count
   - review file exists
   - `Missing reviewers, if any: none`
   - `PASS WITH RESERVATIONS`
   - tracking files now point to Stage 13

## Common Pitfall

When the user says `implement actions` after Stage 11, they usually mean implement the next documented workflow action, not immediately edit every reservation. For Stage 12, that means write the full-stack review, convert non-blocking reservations into Stage 13/14 carry-forward, update tracking, and only edit manuscript text if the review finds a true blocker.