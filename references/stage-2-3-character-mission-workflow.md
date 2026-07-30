# Stage 2 → Stage 3 Character and Mission Workflow

Use this when the author has approved the Stage 1 premise and wants the military-thriller workflow to continue proactively.

## Author Approval Phrases

Treat phrases such as `continue`, `all sound good, go`, or equivalent approval as confirmation of the current gate when the previous response clearly asked for approval of that gate. Record the approval in `progress.md` and `AGENTS.md`, then advance to the next stage.

Do not reinterpret approval as permission to skip future author gates. Each stage still ends with fixed deliverables presented for approval.

## Stage 2 — Character and Cast Development

1. Read `references/stages.md`, the fixed Stage 1 premise, `progress.md`, and `AGENTS.md`.
2. Create profiles with `templates/character-profile.md` for:
   - protagonist
   - spouse/civilian pressure character
   - handler/commander
   - visible antagonist
   - key institutional/local/technical support roles
3. Make every profile plot-functional, not merely biographical:
   - the protagonist must make choices that change events
   - civilian spouse/partner must have agency that fits their real competence
   - handler must have institutional limits and personal cost
   - antagonist must adapt when the protagonist changes the situation
   - local contacts must have their own priorities, not just guide outsiders
4. Review with Alex, Morgan, and Hayes.
5. Apply all actionable fixes immediately. Common fixes:
   - add a concrete operational choice for the protagonist
   - prevent civilian spouse/partner becoming hostage bait or passive support
   - distinguish technical specialists from the protagonist's analytic function
   - add anti-Hollywood guardrails such as `not sudden combat competence`
   - flag exact ranks/postings/titles for Stage 4 research when uncertain
6. Update `reviews/stage-2-character-review.md`, `progress.md`, and `AGENTS.md`.
7. Present fixed cast for approval before Stage 3.

### Parallel Character Creation with delegate_task

When creating 4+ character profiles, use delegate_task to create them in parallel batches (up to 3 profiles per subagent). This is significantly faster than sequential creation.

Rules for parallel creation:
- Give each subagent the full character template inline (subagents cannot read skill files).
- Give each subagent the approved premise and seed context so profiles are consistent with established story decisions.
- Instruct each subagent to read existing project files (other character profiles, premise, seed) before writing — context-loading improves cross-profile consistency.
- Specify cross-character continuity anchors explicitly (shared events, dates, character relationships) so separate subagents produce consistent detail.
- After all subagents return, verify continuity anchors survived across profiles (e.g., the ultimatum incident must match in both spouse's and protagonist's profiles).
- Standardise formatting across profiles before review — different subagents may use bold vs plain field labels, different heading styles, etc. Specifically: ensure all profiles use the same label format (e.g., `- **Name:**` vs `- Name:`), the same heading structure (`# Character Name` vs `# Character Profile — Name`), and the same use of bold/core sections. Run a quick consistency pass with patch commands.

### Character Fates as Author Decisions

When a profile has an unresolved fate (death vs survival, return for sequel vs closure), write the recommended endpoint into the profile and flag it as an author decision in the review. Do not leave fate as "open — a Stage 3 decision" without a recommendation. Recommendations should serve the story's structural needs:
- Antagonist survival preserves a returning threat for a series.
- Supporting character capture into hostage economy creates a reader-invested hostage thread.
- Avoid the "mentor dies to motivate the hero" cliché unless the author requests it.

## Stage 3 — Threat and Mission Design

1. Once Stage 2 is approved, create:
   - `mission/mission-brief.md`
   - `mission/threat-profile.md`
   - `mission/faction-map.md`

### What to Delegate vs Write Directly

Character profiles (Stage 2) delegate well to subagents because each is self-contained. Stage 3 documents are different:

- **Threat profile** CAN be delegated — it is a single self-contained document. Give the subagent the antagonist's character profile and the approved premise. The subagent should read all existing character profiles before writing. One file per subagent.
- **Mission brief and faction map** should be WRITTEN DIRECTLY by the lead agent. These documents require cross-referencing every character profile, the premise, and each other. Delegating them risks timeout (600s limit) and produces documents that do not integrate existing profiles. They also depend on each other (faction map references mission brief's constraints and vice versa), which a subagent cannot coordinate.
- **New character profiles** (Stage 3 cast expansion) CAN be delegated in parallel batches, same as Stage 2.

If a subagent times out, check whether it wrote partial output before the timeout — files may exist on disk even when the subagent reports failure. Use search_files to verify, then write any missing files directly.

2. Threat/mission package must define:
   - public mission objective
   - protagonist's personal operational objective
   - antagonist objective and adaptation path
   - friendly limitations and command authority
   - political/sovereignty constraints
   - intelligence gaps and deception risks
   - concrete Act 2 reversal
   - final confrontation logic
3. Prefer rational institutional friction over melodramatic betrayal unless the author requests a traitor. Bureaucratic/legal/political resistance should be defensible: incomplete proof, visible hostages, attribution risk, sovereignty, or escalation risk.
4. Keep hybrid/cyber/infrastructure/hostage material fiction-safe:
   - use pressure categories and consequences
   - avoid procedural attack, evasion, hostage-control, sabotage, or grid-operation mechanics
   - mark unsafe technical mechanisms as deliberately abstract
5. Add safety/fact-check labels for Stage 4 research:
   - Verified
   - Plausible
   - Unverified
   - Unsafe Detail
   - Wrong
6. Review with Alex, Hayes, Vale, and Quinn.
7. Apply all actionable fixes immediately, update files and review, then present fixed Stage 3 package for approval before Stage 4.

## Progress Updates

After each stage transition, patch both `progress.md` and `AGENTS.md`:

- current stage
- current required step
- last author-approved deliverable
- blocker/reason
- new files of interest
- completed checklist items
- dissent/open concerns carried forward

Remove stale `Notes for Next Session` items that refer to earlier stages. Stale blockers cause future sessions to repeat completed work.
