# Async Delegation Results During Stage Work

Use this when `delegate_task` results return after the lead agent has already drafted, reviewed, or presented a stage deliverable.

## Rule

Late async results are not ignored just because the stage package already exists. Treat them as post-review input and triage them against the current gate.

## Workflow

1. Read the returned summaries or cached summary files only as far as needed to identify durable improvements.
2. Compare suggestions against the already-written deliverable, review file, `progress.md`, `AGENTS.md`, and `rolling-summary.md`.
3. Incorporate only improvements that are:
   - consistent with approved premise/continuity;
   - non-author-decision fixes or refinements;
   - useful as carry-forward constraints;
   - safe and non-procedural.
4. Patch the relevant deliverable file directly.
5. Patch the review file `Fixes Applied` section to record that async refinements were incorporated.
6. Patch tracking files (`progress.md`, `AGENTS.md`, `rolling-summary.md`) when the refinement changes stage carry-forward state.
7. Re-verify file counts/status and keep the current author gate unchanged unless the late result introduces a true author decision or blocker.

## Examples of Good Async Refinements

- A character profile suggestion that sharpens an existing role without changing the premise.
- A safety guardrail such as keeping captivity, intelligence, cyber, or physical action off-page/effect-led.
- A continuity constraint that prevents later drift, e.g. “Stuart is wrong once,” “the ledger remains a physical artefact,” or “Unit 985 has no arrest/field/command authority.”

## Pitfalls

- Do not silently let late subagent output override author-approved direction.
- Do not reopen a completed stage unless the async result reveals a blocker.
- Do not paste whole subagent outputs into project files; distil them into precise carry-forward constraints.
- Do not claim the stage was unchanged if you patched deliverables after async results.
