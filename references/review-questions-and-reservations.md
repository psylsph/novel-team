# Review Questions and Reservations — Actionable Format

Use this reference whenever producing or revising review gates for novel-team / military-thriller work.

## Why this exists

The author corrected the review style: hard questions and reservations must not be vague prompts or passive blockers. They must be descriptive, diagnostic, and include proposed solutions so the workflow can proceed proactively.

## Hard Questions Format

Every hard question must include:

```markdown
- **Question:** [specific uncertainty]
  - **Why it matters:** [story, plausibility, reader, continuity, or safety risk]
  - **Proposed solution:** [recommended answer, constraint, scene function, or next-file action]
```

Bad:

```markdown
- What is the midpoint proof?
```

Good:

```markdown
- **Question:** What visible Act 2 failure proves Bikini Black is real?
  - **Why it matters:** Analytical confirmation alone may feel abstract; readers need a costly external proof point.
  - **Proposed solution:** Use a rail/logistics failure with hospital knock-on effects, shown through civilian consequences while keeping the mechanism abstract.
```

## Reservations Format

Every reservation must include:

```markdown
- **Risk:** [specific remaining weakness]
  - **Mitigation / Proposed solution:** [what to do next, where to record it, or how to solve it]
```

Bad:

```markdown
- Needs more research.
```

Good:

```markdown
- **Risk:** David Price's exact consular/defence liaison title remains unverified.
  - **Mitigation / Proposed solution:** Stage 4 should research public-safe UK embassy/defence liaison roles; until verified, keep him as "senior warrant officer / defence crisis liaison".
```

## When the Author Says “Implement All Proposed Solutions”

Treat this as approval to convert the proposed solutions into concrete files and project state.

Required sequence:

1. Update the affected deliverable files, not just the review.
2. Convert proposed answers into locked or provisional story decisions.
3. Create or update the next-stage research/planning files when the solution naturally belongs there.
4. Mark which solutions were implemented in the review's `Fixes Applied` or `Dissent / Unresolved Concerns` section.
5. Update `progress.md` and `AGENTS.md` in the same turn.
6. Keep approval gates intact: if a full stage transition requires author approval, record the approval phrase and stage movement clearly.

## Review Gate Status Discipline

- `CONDITIONAL PASS`: fixes still need to be applied before presentation.
- `PASS WITH RESERVATIONS`: actionable fixes have been applied; remaining risks are tracked with mitigation/proposed solutions.
- Do not leave reviewer Approval Position as `CONDITIONAL PASS` after all listed fixes are applied. Update reviewer positions and the overall gate consistently.

## Safety-Aware Proposed Solutions

For technical, military, cyber, hostage, infrastructure, evasion, breach, or weapons material:

- Proposed solutions should prefer consequences, uncertainty, authority friction, character pressure, and public-safe institutional context.
- Mark procedural mechanisms as `Unsafe Detail` and replace them with abstracted story pressure.
- If a solution requires research, specify the safe research target, e.g. “public UK embassy crisis support language” rather than operational procedure.
