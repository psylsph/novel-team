# Stage 10 Sustained Auto-Approval Run

Use this when the author repeatedly says `continue` during Stage 10 and standing auto-approval is active.

## Purpose

Keep chapter momentum high while preserving continuity, review gates, and safety boundaries across many chapters in one session.

## Per-Chapter Micro-Cycle

1. **Verify current state before drafting**
   - Read `progress.md`, `AGENTS.md`, `rolling-summary.md`.
   - Read the relevant `chapter-outline.md` and `scene-breakdown.md` excerpt.
   - Read the prior chapter ending/carry-forward lines.
   - Run file/word-count verification (`wc -w chapters/chapter-*.md`; count chapter/review files).

2. **Draft directly from approved scene objectives**
   - Use the Stage 8 scene objective/obstacle/turn/hook as guardrails.
   - Preserve exact carry-forward state: location, group count, batteries/resources, missing-person names, known/unknown threat facts, and hidden-information rules.
   - Keep geography broad and non-operational; use consequence and crowd pressure instead of route/tactical detail.

3. **Self-check before review**
   - Verify word count with `wc -w`.
   - Search for prohibited/early-reveal terms (`Bikini Black`, `Unit 985`) when the outline says they must remain hidden.
   - Search for safety-sensitive terms around cyber, weapons, breaching, evasion, route mapping, checkpoints, and tactical procedure.
   - Search prose-tic patterns from `references/prose-tic-watchlist.md` (`particular`, `kind of`, denial-fragment clusters, repeated `did not`).
   - Patch small issues before writing the review.

4. **Write the review as a real gate**
   - Include required reviewers; add Hayes/Cross for action and Vale for geopolitical/intel/hostage material.
   - Every reviewer must have concrete issues, hard questions with why-it-matters + proposed solution, and reservations with mitigation.
   - `Gate status: PASS WITH RESERVATIONS` only after actionable fixes are applied.
   - Include `Missing reviewers, if any: none` and a `Fixes Applied` section.

5. **Update tracking immediately after approval**
   - `progress.md`: stage status, file counts, word counts, checklist, next chapter.
   - `AGENTS.md`: current state, chapter file/review/word count/gate, carry-forward to next chapter, output list.
   - `rolling-summary.md`: concise chapter summary and current character/list/resource states.

6. **Final verification**
   - Re-run file counts and `wc -w` for all chapter files plus the current review.
   - Verify review header markers and absence of `Pending`/`TBD` placeholders.
   - Re-run safety/hidden-term searches on the chapter.

7. **Report in terminal-friendly format**
   - Files changed.
   - Tracking files updated.
   - Verification bullets.
   - Running status table.
   - `What happens` summary.
   - `Carry-forward to Chapter N+1` with exact continuity/resource/knowledge constraints.
   - `Next required chapter`.

## Pitfalls

- Do not let repeated `continue` skip review or tracking updates.
- Do not trust tracking files without filesystem verification; correct drift before adding new state.
- Do not let action/escape chapters drift into route maps, checkpoint procedure, evasion advice, or hostile tactics.
- Do not over-explain the strategic campaign before the outline permits it; preserve hidden-information timing.
- When group counts change, immediately update `AGENTS.md`, `rolling-summary.md`, and the next chapter carry-forward.
- When a missing-person list begins, preserve source quality: what was seen, what was heard, what is feared, and what remains unproved.
