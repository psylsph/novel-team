# Production Pipeline Run (Stages 10-16)

A single-pass run through Stages 10-16 + EPUB export. Use when the author gives blanket approval or confirms 'continue' through the gated stages.

## Sequence

```
Stage 10: Draft all remaining chapters              → use scene breakdowns directly
Stage 10b: Word-count all chapters (wc -w)          → identify thin chapters
Stage 10c: Expand thin chapters in parallel batches  → use delegate_task 3-per-batch
Stage 11: Run continuity audit                       → 4 parallel subagents (one per act)
         Fix all CRITICAL issues before proceeding
Stage 12: Act break full-stack review                → single subagent, reads all chapters
Stage 13: Developmental edit                         → single subagent, structural review
         Apply all fixes from the review
Stage 14: Line editing                               → batch by act (3 subagents)
Stage 15: Copyediting and fact check                 → batch by act (3 subagents)
Stage 16: Proofreading                               → single subagent, last pass
Stage 17: Final team review + concerns log           → verify final scans, fix only blockers
Stage 17b: EPUB export                               → pandoc recipe, verify EPUB structure/hash
```

## Batching patterns

| Task | Subagents | Per-subagent work |
|------|-----------|-------------------|
| Reviews (backlog) | 3 per call | 2-3 chapters each, write review file |
| Expansion | 3 per call | 1-3 chapters each, write expanded chapter |
| Continuity audit | 4 total | Act 1, Act 2a, Act 2b-3a, Act 3b |
| Line editing | 3 total | Act 1, Act 2, Act 3 |
| Copyediting | 3 total | Act 1, Act 2, Act 3 |

## Tracking file updates

After each stage, update progress.md checklist and AGENTS.md current-stage line.
Update rolling-summary.md after each approved chapter (or after Act 3 is drafted).
