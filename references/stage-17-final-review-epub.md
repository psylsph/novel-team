# Stage 17 Final Review + EPUB Export

Use when the manuscript has passed Stage 16 and the author asks for final review, sign-off package, or EPUB generation.

## Sequence

1. Verify state first:
   - Count chapter files and review files.
   - Recompute chapter/act/manuscript word counts from `chapters/chapter-*.md`.
   - Confirm Stage 16 review exists and points to Stage 17.
2. Run final team review before export:
   - Use a broad team lens: Alex, Morgan, Casey, Jordan, Quinn, Hayes, Vale, Cross.
   - Write `reviews/stage-17-final-review-author-signoff.md`.
   - Include final gate: `PASS WITH RESERVATIONS — READY FOR AUTHOR SIGN-OFF` unless a true blocker appears.
3. Create final supporting docs:
   - `reviews/stage-17-final-concerns-log.md` for unresolved but intentional risks.
   - `reviews/stage-17-retrospective-notes.md` for process lessons and artifact snapshot.
4. Run final pre-export scans:
   - Safety/watchlist scan over chapter prose.
   - Proof-pattern scan: repeated adjacent words, duplicate punctuation, double/trailing spaces, contraction artifacts.
   - Production-room/meta-leak scan for team/persona/workflow terms in chapter prose.
5. Fix only export blockers:
   - Production-room/meta leaks.
   - Tiny proof/spelling/register errors.
   - Do not reopen structure, line edit, copyedit, or fact-check unless the author explicitly asks.
6. Recompute word counts after any final fix and update `progress.md`, `AGENTS.md`, and `rolling-summary.md`.
7. Generate EPUB with pandoc.
8. Verify EPUB:
   - `file exports/<book>.epub` reports EPUB document.
   - `unzip -t exports/<book>.epub` reports no errors.
   - ZIP first entry is `mimetype` with `application/epub+zip`.
   - Metadata contains title.
   - Final chapter is present.
   - EPUB text is clean for production-room/meta names if any were fixed before export.
9. Mark Stage 17 as final team review complete and author sign-off pending unless the author explicitly signs off.

## EPUB Export Artifacts

Recommended paths:

- `exports/<slug>-metadata.yaml`
- `exports/epub-style.css`
- `exports/<slug>-combined.md`
- `exports/<slug>.epub`

If any chapter changes after export, regenerate the combined markdown and EPUB, then rerun EPUB verification.

## Final Status Must Include

- EPUB absolute path.
- File size and hash if available.
- Review gate and required reviewers.
- Final word count and act totals.
- Scan results.
- Author sign-off status.
