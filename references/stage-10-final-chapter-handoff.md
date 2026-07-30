# Stage 10 Final Chapter Handoff

Use when the final planned chapter of a novel draft is completed under the chapter-by-chapter Stage 10 workflow.

## Required sequence

1. Draft the final chapter from outline/scene-breakdown/rolling-summary carry-forward.
2. Run the normal chapter review/fix cycle and write the final chapter review file.
3. Verify the final chapter with `wc -w` and the usual manuscript safety/prose/meta scan for that chapter.
4. Update tracking files to mark Stage 10 complete and Stage 11 as the next required action:
   - `progress.md`: current stage becomes Stage 11; Stage 10 status COMPLETE; chapter/review counts and total word counts include the final chapter.
   - `AGENTS.md`: current stage becomes Stage 11; Stage 10 status COMPLETE; next required action is Stage 11 continuity / mission-logic pass.
   - `rolling-summary.md`: add final chapter summary, final character states, and Book 2/open-thread notes.
5. Run final filesystem verification: chapter count, review count, final chapter word count, computed manuscript total, and tracking-file markers.
6. Run a whole-manuscript scan for safety/prose/meta watchlist terms. Do not silently edit legacy approved chapters at this point unless the task explicitly asks for Stage 11 fixes. Report any older-chapter hits as Stage 11 inputs.
7. Final status should clearly say: final chapter complete, Stage 10 first draft complete, total word count, files changed, what happens, carry-forward to Stage 11, and next required action.

## Pitfalls

- Do not leave the project in “Draft final chapter next” after the final chapter review passes. Promote state immediately to Stage 11.
- Do not claim the whole manuscript is scan-clean if only the final chapter is clean. Distinguish “current chapter clean” from “legacy hits queued for Stage 11.”
- Do not start Stage 11 fixes in the same final-chapter turn unless the author explicitly requested that pass; first close Stage 10 cleanly.
- Preserve the one-chapter-at-a-time rail even if the user sends repeated `continue`; repeated continues mean momentum, not permission to skip review/tracking/verification.