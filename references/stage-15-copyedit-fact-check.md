# Stage 15 — Copyediting and Fact Check

Use this after Stage 14 line editing when the manuscript is structurally stable and watchlist cleanup is done.

## Purpose

Stage 15 is not another line edit. It verifies grammar/register consistency, factual labels, institution/rank/role terminology, place names, public-source claims, and safety boundaries before proofreading.

## Workflow

1. Load `references/stages.md`, `references/research-safety-boundaries.md`, any domain-specific reference files (for Bikini Black, `references/baltic-intel-services.md`), and the relevant persona files for Quinn, Casey, and Jordan.
2. Read the current state from `progress.md`, `AGENTS.md`, `rolling-summary.md`, Stage 14 review, and any fact-check carry-forward notes.
3. Gather the factual risk list from prior reviews. Common categories:
   - provisional ranks/titles/roles;
   - official institution/place names;
   - acronyms and agency names;
   - public legal/political framing;
   - safety-boundary terms;
   - grammar/register issues created by prior line edits.
4. Check chapter prose first, then current-facing planning/tracking docs. Historical seed/review files can remain as historical records unless they actively guide future work.
5. Prefer official sources for factual claims. If a direct official URL is known, fetch/inspect it directly rather than relying only on search discovery.
6. Apply only targeted fixes. Do not reopen structure, pacing, scene order, or broad prose style.
7. Write `reviews/stage-15-copyedit-fact-check.md` with Quinn, Casey, and Jordan sections, fixes applied, remaining reservations, and Stage 16 handoff.
8. Update `progress.md`, `AGENTS.md`, and `rolling-summary.md` with Stage 15 completion and Stage 16 next action.
9. Verify chapter/review counts, word total, review gate, current-stage tracking, source-link capture, and safety/watchlist scan.

## Title / Role Fact-Check Pattern

When a specific title is unsupported (for example a provisional rank/title in planning), do not replace it with a different precise guess. Prefer a flexible function description that preserves story logic without overclaiming.

Example pattern:

- Bad: hardening a provisional `RSM` into another exact official title without reliable support.
- Better: `Daniel Price — British consular security / military-professional presence`.

Apply this to current-facing docs and manuscript prose. Leave raw seed text and historical review discussion alone unless it would mislead future active workflow.

## Reference-Link Capture

If Stage 15 uses or discovers a new source URL, add it to `IDEAS.md` with a one-line purpose note.

## Verification Checklist

- `reviews/stage-15-copyedit-fact-check.md` exists.
- Required reviewers: Quinn, Casey, Jordan.
- `Missing reviewers, if any: none` present.
- Gate status: `PASS WITH RESERVATIONS` unless a true factual blocker remains.
- Chapter safety/watchlist scan is clean.
- Current-facing docs no longer contain stale provisional-title instructions.
- Historical seed/review files are not over-edited as if they were current manuscript state.
- Word totals still match `wc -w` / computed split totals.
- `progress.md`, `AGENTS.md`, and `rolling-summary.md` all point to Stage 16 next.

## Carry Forward to Stage 16

Stage 16 proofreading should catch typos, grammar/register residue, and consistency slips. It should not reopen broad line-edit or fact-check decisions unless it finds an actual error.