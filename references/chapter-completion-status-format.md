# Chapter Completion Status Format

Use this after each Stage 10 chapter that is drafted, reviewed, fixed, and approved under the chapter workflow.

## Terminal-Friendly Order

1. Files created/changed:
   - chapter draft path
   - review path
2. Tracking files updated:
   - `progress.md`
   - `AGENTS.md`
   - `rolling-summary.md`
3. Verification bullets:
   - chapter/review file counts
   - exact `wc -w` chapter word count
   - required reviewers and missing-reviewers status
   - gate status
   - safety/continuity checks such as no premature reveals
4. Running status table:
   - chapter number
   - title
   - word count
   - status
5. `What happens`:
   - concrete plot beats only
   - no praise, no review language, no vague “tension escalates” unless tied to an event
6. `Carry-forward to Chapter N+1`:
   - actionable continuity state: locations, resource state, knowledge state, named-character status, unresolved promises, required tone/safety constraints
7. `Next required chapter`:
   - title and number only unless a gate blocks progress

## Persistence Mapping

- `rolling-summary.md` receives the prose story-state version.
- `AGENTS.md` receives operational carry-forward and next required chapter.
- `progress.md` receives checklist state, file counts, exact word counts, and next action.
- `reviews/chapter-NN-review.md` receives review issues, hard questions, reservations, fixes applied, and gate status.

## Pitfalls

- Do not replace the carry-forward section with generic advice. It must be specific enough for the next session to draft from.
- Do not estimate word counts; always use `wc -w`.
- Do not present review praise as “what happens.” Use plot facts.
- Do not let a lean action chapter trigger padding automatically. Expand only if story function feels thin.
