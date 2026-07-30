# Chapter Drafting Accelerator

When scene-by-scene breakdowns are detailed enough (the standard Stage 8 deliverable), you can skip the chapter-brief step and draft directly from outline + scenes. This accelerates the drafting cycle significantly.

## Trigger

Stage 10 (First Draft) with complete scene breakdowns.

## Workflow

```
1. Read only the current chapter slice from the scene breakdown, the previous chapter tail, and the compact carry-forward in AGENTS.md/progress.md/rolling-summary.md. Do not reload broad stage files unless continuity is genuinely unclear.
2. Draft chapter directly (~2,000-2,600 words first pass)
3. wc -w, compare to ~3,000 target
4. Expand using these techniques in order:
   - Sensory atmosphere: cold, darkness, sound, smell, light quality
   - Internal texture: POV character's analytical process, training recall, fatigue markers
   - Dialogue subtext: let subtext carry weight, use spare exchanges
   - Marriage/relationship beats: Stuart-Kirsty through-line in every chapter
5. Recheck wc -w, patch in more if needed
6. Present with compact summary + running status table
```

## Token / Context Discipline

User preference from Black Ledger drafting: actively minimise context. For chapter drafting, use narrow reads and compact tool output:

- Read the current chapter's 3-scene slice, not the full scene breakdown.
- Read only the previous chapter tail needed for handoff, not whole prior chapters.
- Read compact carry-forward lines from `AGENTS.md`, `progress.md`, and/or `rolling-summary.md`; do not reread all planning deliverables.
- Do not reload broad style/reference files after they are already in-session unless a new issue requires them.
- Keep terminal-facing completion summaries concise; avoid growing all-chapter tables if the user has reminded you about tokens/context.
- Batch independent narrow reads/searches in one tool turn.
- After context compaction, interruption, or preserved task-list handoff, verify live files/progress/reviews before drafting. If the task list says a chapter is pending but files/reviews/progress show it is complete, do not redraft; finish tracking or move to the next required chapter.
- If the user sends repeated `continue` lines in the same novel project, treat them as repeated approvals for sequential chapter cycles only after verifying current state between cycles.

## State Reconciliation After Handoffs

When a preserved todo, compacted summary, AGENTS/progress, and live files disagree, use this order:

1. Verify live filesystem first: `search_files(target="files")` for the chapter/review, then `wc -w` for chapter and review counts.
2. Verify gate markers in the review (`Missing reviewers, if any: none`, `PASS WITH RESERVATIONS`, `Fixes Applied`, `Author Decisions Needed`) and run the meta-leak scan before deciding the chapter is complete.
3. Compare `progress.md`, `AGENTS.md`, and `rolling-summary.md` carry-forward. If docs lag behind files/reviews, finish tracking updates rather than redrafting.
4. Treat preserved todos as hints, not truth. Mark stale pending chapter todos completed/cancelled once live files prove the work exists.
5. For stacked `continue` messages, process only as many chapter cycles as the current verified state supports; re-verify after each chapter before advancing to the next.

## Pitfalls

- Don't try to hit 3,000 on first pass — you'll slow down. Write lean, expand after.
- Action chapters (3-4 scenes, movement, reversals) naturally run 2,800-3,200. They need less expansion.
- Character-establishment chapters (1-2 scenes, conversation, atmosphere) naturally run 2,200-2,600. They need more expansion — lean into sensory atmosphere and internal texture.
- Never over-expand dialogue. Spare exchanges carry more weight than verbose ones.

## Running Status Table Format

Present chapters with a compact table:

```
| Ch | Title | Words | Status |
|----|-------|-------|--------|
| 1 | Arrival | 2,774 | APPROVED |
| 2 | The Restaurant | 2,562 | APPROVED |
```

Each chapter presentation includes:
- File path and word count
- WHAT HAPPENS section (compact narrative summary, 3-5 paragraphs)
- CARRY-FORWARD TO NEXT CHAPTER section (resource state, character state, unresolved names/threads, continuity constraints, and next-scene setup)
- Key checks/verification against scene breakdown
- Running status table (all chapters)

User preference reinforced in Bikini Black drafting sessions: the chapter handoff summary is not optional polish. Treat “what happens” + “carry-forward” as the standard terminal-facing chapter completion format so the author can quickly verify continuity and momentum before saying “continue”.
- Running status table (all chapters)

Mirror the carry-forward list into `rolling-summary.md`, `AGENTS.md`, and review reservations/fixes where relevant. The author has confirmed this paired “what happens” + “carry-forward” summary is expected after chapter work.

## Expansion Targets by Chapter Type

| Chapter Type | Typical First Draft | Expansion Needed | Focus |
|---|---|---|---|
| Action (3+ scenes) | 2,600-3,200 | 0-400 words | Sensory (cold, sounds, fatigue) |
| Character (1-2 scenes, no action) | 2,200-2,600 | 400-800 words | Internal texture + sensory atmosphere |
| Mixed (2-3 scenes, light action) | 2,400-2,800 | 200-600 words | Marriage beats + environment |

## Author Interaction

- Present chapter + compact summary. Author responds "approved" or "revisions."
- "Approved" = update docs, rolling-summary, advance to next chapter immediately.
- Don't ask for permission to continue — the approval IS the permission.
