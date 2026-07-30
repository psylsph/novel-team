# Proactive Review Gates

Use this whenever a novel-team / military-thriller deliverable has been reviewed.

## Core Lesson

Do not treat a review as the stopping point. Reviews are a work queue.

After reviewers identify issues:

1. Separate issues into:
   - **Actionable fixes** — the agent can apply without author choice.
   - **Author-only decisions** — naming, premise direction, approval gates, major creative alternatives.
   - **Carry-forward requirements** — items that belong in later stages, not blockers now.
2. Apply every actionable fix immediately.
3. Write or patch the revised deliverable.
4. Update the review file:
   - gate status after fixes,
   - fixes actually applied,
   - remaining author decisions,
   - carry-forward concerns.
5. Update `progress.md` and `AGENTS.md` in the same turn.
6. Present the fixed result, not the unfixed critique.
7. Continue to the next mechanically allowed deliverable when no explicit author gate blocks it.

## What Counts as an Author Gate

Stop and ask only when the stage requires author approval or when the choice is genuinely creative and non-obvious:

- approving final Stage 1 premise direction,
- confirming character/cast direction before mission design,
- choosing between mutually exclusive plot engines,
- renaming major characters/organisations,
- approving planning before drafting.

## What Does Not Need Permission

Do not ask before doing these:

- fixing review actions already identified by the team,
- strengthening weak character agency,
- clarifying institutional roles,
- moving review concerns into carry-forward requirements,
- updating `progress.md`, `AGENTS.md`, reviews, or planning files,
- creating the next required reviewed deliverable after the user says "continue".

## Common Pitfall

Bad pattern:

```text
Review complete. There are issues. Do you want me to fix them?
```

Correct pattern:

```text
Review complete. I fixed the actionable issues, updated the review gate and project docs, and carried forward the remaining author-only decisions.
```

## Fixing Review Reservations

When the user says "fix the review reservations", the reservations are not bugs in the review — they are forward-looking mitigations already documented by reviewers. Your job is to convert each one into concrete changes in the deliverable.

Follow this sequence:

1. **Read the review** to identify every reservation from every reviewer. Each has a `Risk:` and `Mitigation / Proposed solution:`.
2. **Convert each proposed solution** into concrete changes in the deliverable. Ask: "What would this look like as text in the deliverable?"
   - A reservation about Act 1 sprawl → add chapter count estimate + per-chapter physical-problem rule.
   - A reservation about coordination-room weight → add alternation rule for civilian consequence beats.
   - A reservation about geopolitical abstraction → add a concrete decision-beats section.
3. **Update the deliverable** with the changes.
4. **Update the review's "Fixes Applied" section** with a bullet for each addressed reservation, e.g.:
   - `**Reservation: Alex (Act 1 sprawl)** — Added chapter count estimate with explicit rule.`
5. **Update "Dissent / Unresolved Concerns"** to show reservations resolved.
6. **Verify every fix was actually applied** by searching for key phrases in the deliverable.
7. **Update `progress.md` and `AGENTS.md`** in the same turn.

## Reporting Format

When reporting back, separate:

- **Created/updated files**
- **Review gate status**
- **Fixes applied** (include reservation-fix tracking if applicable)
- **Only remaining author decisions**
- **Next stage if approved**
