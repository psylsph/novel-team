# Proactive Stage-Gate Lessons

Use these rules when operating the military-thriller gated workflow for Stuart.

## 1. Treat short approvals as stage approvals when context is clear

If the current state is blocked at an author approval gate and Stuart says things like:

- `continue`
- `all sound good, go`
- `excellent next stage`
- `I agree implement all proposed solutions`

interpret that as approval of the current fixed deliverable and move to the next stage. Do not ask for a second confirmation unless there is a genuine ambiguous creative choice.

## 2. Reviews must produce fixable questions, not vague prompts

Hard questions and reservations must be diagnostic and solution-oriented:

- Question / risk
- Why it matters
- Proposed solution or mitigation

Bad: `Who says no to Turner?`  
Good: `Who says no to Turner, and why are they right enough to matter? Why it matters: institutional friction must create real debate. Proposed solution: create an allied legal-political liaison whose concern is premature attribution endangering hostages and alliance unity.`

## 3. Apply proposed solutions when approved

When Stuart approves proposed solutions:

1. Convert each proposal into concrete deliverable text, research notes, outline beats, character constraints, or setting rules.
2. Update the affected project files.
3. Update the review gate from `CONDITIONAL PASS` to `PASS WITH RESERVATIONS` once fixes are applied.
4. Update `progress.md` and `AGENTS.md` in the same turn.
5. Present the fixed result and stop only at the next author approval gate.

## 4. Preserve formal author gates, but do not stall on internal fixes

The workflow remains gated. Do not advance past an author approval gate without confirmation. But do not stop between review and fixes: apply all non-author-decision fixes proactively before presenting.

## 5. Put reservations into future-stage carry-forward form

A reservation should not be a loose worry. It should become a future-stage requirement, e.g.:

- `Stage 7 must cap Act 1 at Poland/Turner reveal and make each Act 1 chapter add a physical problem.`
- `Stage 7 should alternate coordination-room material with named civilian consequences or live consequence feeds.`
- `Stage 7 must use the legal-political liaison and authority-tagged decisions to dramatise geopolitics.`

## 6. Verify fixes were actually applied

After applying fixes from a review, search the deliverable for key phrases. Do not assume a text replacement worked — character encoding (smart quotes, em dashes, en dashes) and invisible whitespace can cause silent failures.

Pattern:

```text
1. Read the deliverable to find the exact string that needs changing.
2. Apply the change.
3. Search for the new string to confirm it landed.
4. If missing, re-read the line at the target location and try with the exact characters found there.
```

## 7. "Fix the review reservations" is a deploy action, not a planning step

When the user says "fix the review reservations", do not ask which reservations or how. Each reservation already carries a proposed solution. The task is:

1. Identify every reservation across all reviewers.
2. Convert each proposed solution into deliverable changes.
3. Apply the changes.
4. Update the review and project files.
5. Report the fixes.

Do not stop to present the plan. Execute the plan.

## 8. Reservations are fixed before author presentation, not just noted

After writing the review but before presenting to the author:

1. Apply every reservation's proposed solution to the deliverable.
2. Update the review's Fixes Applied section with a line per reservation (e.g. "Reservation: Alex (Act 1 sprawl) — Added chapter count estimate").
3. Update the Dissent / Unresolved Concerns section to reflect what was resolved.
4. Verify no placeholder text ("Pending fixes", "TBD", "Pending") remains in the review file.
5. Only then present the package to the author.

If a reservation cannot be addressed at the current stage (e.g. "Stage 7 must track Act 1 timeline" during a Stage 6 review), convert it to a carry-forward requirement. Both the review and progress.md's Dissent section should show resolved items as addressed and unresolved items as carry-forward.

## 9. Be transparent about how reviews work

When presenting a review, be clear about the methodology:

- The team personas (Alex, Morgan, Vale, etc.) are fictional role-play characters defined in the skill.
- The agent reads each deliverable from each persona's defined perspective and writes structured critique.
- Review files are real written artifacts in the reviews/ directory — they can be opened and read.
- No real people were consulted.

Do not use language that implies real people (e.g. "Alex was sent the file" or "Morgan reviewed overnight"). Say instead: "Review completed with Alex/Morgan/Vale: each persona's perspective was applied to the deliverable and the review file was written to reviews/."

## 10. Chapter word count target: ~3,000 words

Each chapter should target approximately **3,000 words**. This produces a novel of 80,000–100,000 words across 27–33 chapters or approximately 50,000–60,000 words across a shorter 17-chapter draft. Use `wc -w <file>` to verify after every chapter draft.

When expanding a chapter to meet the target, add depth through:
- Character backstory and relationship texture (flashback, internal history, tell)
- Sensory environment and atmosphere (weather, light, sound, cold, fatigue)
- Internal stakes (protagonist's past debts, fears, training, or trauma)
- Threat texture (adversary method, pattern observation, tactical detail at fiction-safe level)
- Institutional friction or political constraint

Do NOT pad with:
- Repetition of information already established
- Excessive technical exposition
- Dialogue that restates what the reader already knows
- Action without consequence or reversal
