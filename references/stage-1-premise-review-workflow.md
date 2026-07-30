# Stage 1 Premise Review and Fix Workflow

Use this when developing or reviewing Stage 1 concept/premise options for a military-thriller project.

## Core Rule

Do not treat informal review notes embedded in a premise/options file as the final review artifact. Stage 1 needs a standalone review file under the project `reviews/` directory using `templates/review-output.md`.

## Required Files

- `concepts/seed.md` — captured Stage 0 seed and author clarifications
- `concepts/stage-1-premise-options.md` — 3-5 premise options plus an initial recommendation
- `reviews/stage-1-premise-review.md` — formal Alex/Morgan/Vale review
- `concepts/stage-1-final-premise.md` — fixed final premise after review actions
- `progress.md` and `AGENTS.md` — updated after each meaningful step

## Workflow

1. Read the seed and Stage 1 options.
2. Create 3-5 premise options if they do not already exist. Each option should include protagonist, goal, obstacle, antagonist/force, setting, stakes, moral dilemma, and commercial hook.
3. Run a formal review using `templates/review-output.md` with required reviewers:
   - Alex — structure, stakes, agency, mission logic
   - Morgan — reader hook, clarity, emotional investment, page-turn quality
   - Vale — geopolitical logic, deniability, incentives, strategic plausibility
4. Write the formal review to `reviews/stage-1-premise-review.md`.
5. If the review is `CONDITIONAL PASS`, do not stop with the review. Apply the review actions by writing a fixed `concepts/stage-1-final-premise.md`.
6. Patch the review gate to `PASS WITH RESERVATIONS` only after fixes are actually applied.
7. Convert unresolved review concerns into carry-forward requirements for Stage 2/3 instead of leaving them as vague blockers.
8. Update `progress.md` and `AGENTS.md` with the new current required step: author approval of `concepts/stage-1-final-premise.md`.
9. Present the final premise and wait for author approval before advancing to Stage 2.

## Common Fix Patterns

- **Split engine problem:** If an escape plot resolves and then a separate mission begins, make the escape generate the clue/intelligence chain that triggers the mission.
- **Consultant protagonist problem:** Give the protagonist a specific high-level analytic value, not generic clearance or reputation.
- **Abstract codename problem:** Use historical/intelligence terminology as flavour and clue texture, not as the plot engine.
- **Passive spouse problem:** Define the spouse's active pressure role in concrete terms without making them implausibly tactical.
- **Magic infrastructure switch problem:** Frame infrastructure attacks as cascading regional effects and consequences, not a single continent-wide off switch.
- **Faceless antagonist problem:** Carry forward the need for a named operational antagonist who makes decisions and creates costs.

## Verification Checklist

- [ ] Formal review file exists under `reviews/`
- [ ] Review uses `templates/review-output.md`
- [ ] Alex, Morgan, and Vale each have specific issues, hard questions, reservations, and approval positions
- [ ] Fixed final premise exists under `concepts/`
- [ ] Review gate reflects actual state after fixes
- [ ] `progress.md` and `AGENTS.md` name the final premise file as the approval blocker
- [ ] Stage 2/3 carry-forward requirements are explicit
