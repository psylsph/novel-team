# Stage 10 Scan and Momentum Lessons

Session-derived guidance for sustained auto-approved chapter drafting.

## Repeated `continue` still means one complete chapter cycle

If the author sends repeated momentum cues in the same turn (for example `good continue` twice), treat it as urgency/momentum, not permission to batch chapters. Complete exactly one full chapter cycle:

1. Verify current state and next required chapter.
2. Draft the chapter.
3. Run review/self-check and apply fixes.
4. Update `progress.md`, `AGENTS.md`, and `rolling-summary.md`.
5. Verify chapter/review counts, `wc -w`, review gate, and safety/prose/meta scans.
6. Present the chapter package and name the next required chapter.

## Manuscript scan discipline

Before marking a chapter approved, run a compact scan for:

- workflow/persona/meta leaks: Alex, Jordan, Casey, Hayes, Vale, Morgan, Riley, Quinn, Cross, Sam, Mason, Hermes, Unit 985 where prohibited;
- prose tics that should be rewritten when accidental: `did not`, `kind of`, `particular`;
- safety-sensitive terms that may indicate over-specificity: SCADA, payload, exploit, hack, breach, weapon, tactical, surveillance, biometric, passport number, hostage handling, interrogation, captivity conditions, forensic, system access, substation, node, grid-control.

Use whole-word matching for persona/meta names. Substring matches create false positives (for example `Sam` inside `Same`). Inspect context before editing; do not blindly delete legitimate in-world text.

## Preferred fix pattern

- Rewrite flagged prose in manuscript rather than explaining it away in the review.
- If a safety term is needed in a review file, that is usually fine; the manuscript scan is stricter.
- If a meta/persona name appears in manuscript, remove or rephrase unless it is independently legitimate in-world usage.
- Record the scan/fixes in the chapter review’s `Fixes Applied` section and in the final status verification.
