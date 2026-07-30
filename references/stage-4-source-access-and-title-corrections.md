# Stage 4 Source Access and Title Corrections

Use this when Stage 4 research is partly blocked by search/extraction setup or anti-bot pages, or when research finds an earlier-stage title/rank problem.

## Source Access Fallback Pattern

Do not stop research just because a preferred web-search tool is unavailable. Use a source-confidence workflow:

1. Try direct public-source URLs when the likely authority is obvious (GOV.UK, legislation.gov.uk, NATO, EU/EEAS, GOV.PL, ministry sites).
2. Use official-site search pages where general web search is unavailable.
3. Extract only what is needed for story decisions: institutional limits, vocabulary, authority ownership, and safety boundaries.
4. Split sources into:
   - `Accessed / used as evidence`
   - `Partial / source pointer only`
   - `Blocked or attempted / not used as hard evidence`
   - `Internal skill reference / externally verify later`
5. Put this access note in `research/source-list.md` and summarize it in `research/research-brief.md` so source confidence is explicit.
6. Add all accessed/attempted reference URLs to project `IDEAS.md` with a one-line purpose note.

Do not encode the transient tool/setup failure itself as a durable rule. Encode the fallback method and confidence labelling.

## Earlier-Stage Title / Rank Corrections

Stage 4 often discovers that a working title from character or mission design implies an unintended real institution.

When this happens:

1. Treat the title as `Wrong as hard fact; Plausible only as fiction` unless the story deliberately chooses the implied backstory.
2. Fix forward-looking files: character/cast package, mission/faction/world files, AGENTS.md, progress.md, rolling-summary.md.
3. Leave historical seed/review files unchanged; they document project evolution.
4. Record the correction in the Stage 4 review `Fixes Applied` section.
5. Add the corrected usage to `research/research-brief.md` and any relevant open question.

Example pattern: if `Commander` reads as a Royal Navy or police rank but no parent-service decision exists, use function-first language such as `Rafiq Bell, Unit 985 authority/records officer` until the author chooses a specific backstory.

## Review Gate Check

Before presenting Stage 4:

- Research files exist: `research/research-brief.md`, `research/open-questions.md`, `research/source-list.md`, `research/safety-labels.md`.
- `source-list.md` distinguishes accessed, partial, blocked, and internal-reference items.
- `IDEAS.md` contains every source/reference URL used or attempted.
- Review file lists Riley, Quinn, Vale; `Missing reviewers, if any: none`; gate status `PASS WITH RESERVATIONS`.
- Any verified title/rank correction is applied to forward-looking files and documented in `Fixes Applied`.
