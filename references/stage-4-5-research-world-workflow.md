# Stage 4–5 Research and World Workflow

Use this when moving from threat/mission design into research deep dive and operational environment design.

## Trigger

After Stage 3 threat/mission review passes with reservations and the author approves proposed solutions, convert those solutions into concrete Stage 4 research files and Stage 5 world/environment files. Do not leave approved solutions as vague review notes.

## Stage 4 — Research Deep Dive

Create or update:

- `research/research-brief.md`
- `research/source-list.md`
- `research/open-questions.md`
- `research/safety-labels.md`
- optional `research/stage-4-implementation-notes.md`

Required behaviour:

1. Convert every approved reservation/proposed solution into a locked or provisional research decision.
2. Use public-safe sources for geography, institutions, weather, culture, public health, embassy/consular guidance, NATO/allied context, etc.
3. Label claims as `Verified`, `Plausible`, `Unverified`, `Unsafe Detail`, or `Wrong`.
4. Research consequences, constraints, and institutional behaviour — not operational methods.
5. If a detail risks becoming a how-to, replace it with character pressure, public consequence, uncertainty, or command friction.
6. **Verify institutional names from earlier stages.** Cross-check every real-world institution referenced in Stages 1-3 (embassies, consulates, intelligence agencies, military units, government departments) against current public sources. If an error is found, apply the correction protocol in the "When Research Discovers Earlier-Stage Errors" section below.
7. **Use `templates/safety-labels.md`** for the structure of `research/safety-labels.md`. The two-column "Abstract in Prose" / "Safe to Depict in Detail" format ensures every Unsafe Detail has an abstraction strategy.
8. **Batch web research efficiently.** Run 5 web searches per batch, extract 3-5 key pages from the results, then compile into research files. Do not research one topic at a time — batch related topics.

## Safety Labels

Use this table in all research and later planning files:

| Label | Meaning |
|---|---|
| Verified | Supported by reliable public source |
| Plausible | Reasonable fiction extrapolation |
| Unverified | Needs source or author decision |
| Unsafe Detail | Too procedural; abstract or exclude |
| Wrong | Contradicted by reliable source |

Unsafe detail includes cyberattack methods, grid-control procedures, sabotage, breach/evasion, hostage-control techniques, weapons methods, or tactical route instructions.

## Stage 4 Review

Review with Riley, Quinn, and Vale.

The review must include:

- setting richness still missing,
- source reliability issues,
- safety-boundary risks,
- geopolitical specificity gaps,
- proposed fixes/carry-forward actions.

Hard questions and reservations must use the structured form from `references/review-questions-and-reservations.md`.

## When Research Discovers Earlier-Stage Errors

Stage 4 research frequently discovers factual errors in deliverables from Stages 1–3 that were not caught during earlier reviews. This is expected — research deepens verification, and institutional/geographic facts that seemed plausible in earlier stages may prove wrong under source-level scrutiny.

Protocol when this occurs:

1. **Flag the error in the Stage 4 review** under Quinn (fact checker), with the verified fact, the source, and the list of affected files.
2. **Fix all forward-looking files.** Apply the correction to every file that will be used in subsequent stages: mission briefs, threat profiles, faction maps, character profiles, AGENTS.md, progress.md. Use batch find-and-replace (ordered: longer patterns first, preserve valid cognates — e.g. "consulate" to "embassy" but preserve "consular" which is a valid term for the consular section/function).
3. **Do NOT retroactively change historical files.** The seed, premise options, and earlier review files are historical records. Note them as containing the original error, but leave them unchanged — they document the project's evolution.
4. **Track the correction in the review's Fixes Applied** section with: what was wrong, what is correct, which files were changed, and how many replacements were made.
5. **Add the corrected fact to safety-labels.md or research-brief.md** so the verified version is authoritative going forward.

Example from Bikini Black (Unit 985, Book 1): Stage 4 research discovered that Vilnius has a full British Embassy with a resident Ambassador, not a Consulate. The error had propagated through the seed, premise, mission brief, threat profile, faction map, and 4 character profiles across 3 stages. Quinn had reviewed these files in Stages 2-3 without catching it. The correction required 32 replacements across 7 forward-looking files. Root cause: institutional naming was never explicitly verified against real-world diplomatic structures during earlier stages.

## Stage 5 — World and Operational Environment

Create:

- `world-outline.md` — use `templates/world-outline.md` for structure
- setting/location briefs in `settings/` using `templates/location-intel-brief.md`
- update `progress.md` and `AGENTS.md`

World files should convert research into operational story constraints, not repeat notes.

**Parallel location brief creation:** When multiple independent location briefs are needed (e.g. Vilnius, Suwałki Gap, Embassy Warsaw), create them via parallel `delegate_task` subagents (up to 3). Each subagent receives: the template path, the specific location, the story context (season, which characters, which act), the relevant research-brief sections, the safety-labels rules, and the target word count. Verify all briefs have the required 6 template sections after creation.

Each setting brief should define:

- physical environment,
- human environment,
- threat environment,
- political/authority constraints,
- story pressure,
- atmosphere details,
- sources,
- safety-sensitive details to abstract.

## Required Reviewers for Stage 5

Use Riley, Casey, Vale, and Hayes.

Reviewer focus:

- Riley: setting richness and source grounding.
- Casey: timeline, continuity, records, fatigue, who knows what.
- Vale: local sovereignty, geopolitics, institutional friction.
- Hayes: authority chain, non-Hollywood behaviour, professional constraints.

## Pitfalls

1. **Leaving reservations as questions.** If the author approves proposed solutions, implement them in files immediately.
2. **Research as note dump.** Stage 5 must turn research into usable plot pressure: location, constraint, cost, and choice.
3. **Over-specific geography.** Use public geography for texture, not route instructions.
4. **Institutional fantasy.** Host-nation authorities remain active; British/Unit 985 action needs an authority path.
5. **Magic infrastructure plot.** Show consequences and decisions, not mechanisms.
6. **Passive local setting.** Local civilians and authorities must change protagonist options at least once.
7. **Unverified institutional names.** Real-world institutions (embassies vs consulates, agency names, military unit designations) must be verified against actual structures during Stage 4, not assumed from the seed. An embassy is not a consulate; an Ambassador is not a Consul. If the seed uses a real-world institution name, verify it early — errors propagate across all downstream files. Quinn's fact-checking scope in Stages 2-3 should explicitly include "verify all institutional/organisational names match real-world structures" as a checklist item.
8. **Season and climate discovered too late.** Time of year affects every aspect of the story: road conditions, daylight hours, grid strain, exposure risk, military movement visibility, atmospheric texture. Season should be established as an author decision during Stage 1 (premise) or Stage 2 (character/world setup), not surfaced as an open question in Stage 4 research. If it has not been decided by Stage 4, flag it as an author decision needed before Stage 5 location briefs can be written.

## Verification Before Advancing

Before presenting Stage 5 to the author, verify:

- Stage 4 research files exist and use safety labels.
- Stage 4 review exists and fixes/carry-forwards are documented.
- `world-outline.md` exists.
- Relevant `settings/*.md` briefs exist.
- Stage 5 review exists with Riley/Casey/Vale/Hayes.
- `progress.md` and `AGENTS.md` reflect the current stage and approval blocker.
