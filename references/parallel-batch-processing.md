# Parallel Batch Processing for Novel Workflows

Use `delegate_task` to parallelize multi-unit work when catching up or scaling. The 3-subagent limit per call is the constraint — plan batches accordingly.

## 1. Mass Chapter Reviews (Backlog)

When 10+ chapters need reviews that were never done, batch 3 per delegate_task call:

**Per-subagent payload:**
- Chapter file path + word count
- Scene breakdown excerpt from `actN-scenes.md`
- Review template (`templates/review-output.md`)
- Required reviewers list (Rule 1 table)
- Relevant references: house-style, military-authenticity

**Reviewer selection by chapter type:**
- Character/relationship: Alex, Jordan, Casey
- Add Hayes for military/action, Vale for geopolitical, Cross for action sequences

**Each subagent writes:** `reviews/chapter-NN-review.md` with full format (5+ issues per reviewer, hard questions, reservations, gate status).

**After all batches:** Verify all review files exist, confirm "Missing reviewers: none" in each, apply critical fixes.

## 2. Post-Draft Expansion Pass

1. `wc -w` all chapters, sort ascending
2. Batch 3 thinnest per call
3. Each subagent receives: file path, word counts, continuity anchors (timestamps, numeric counts, character fates, location names), expansion areas, review file, house style reference
4. After each batch: verify continuity anchors survived, update word counts in progress.md

**Common continuity anchors to protect:** Stuart's GCHQ exit after tenth anniversary, Kirsty as forensic accountant on personal laptop, Rasa as municipal planner, Helen as paediatric cardiologist (Manchester), Davies as WO1 Royal Regiment of Scotland, grid attack at 06:43 Day 2, Morozov as former GRU Spetsnaz, Ch 19 tell (three sources decimal alignment), NordBalt as real target (revealed Ch 20), UNIT 985 file contents NOT shown to reader.

## 3. Continuity Audit (Stage 11)

Split by act: Act 1 (Ch 1-7) + Act 2a (Ch 8-14) in batch 1, Act 2b (Ch 15-22) + Act 3 (Ch 23-28) in batch 2.

**Severity:**
- 🔴 Critical — fix before presenting
- 🟡 Moderate — fix when possible
- 🟢 Minor — note for later

**Common bugs:** Turner gender (she/her), character names, timeline math, temperature bridging, fuel/logistics plausibility, attack-window hour arithmetic.

## 4. Act 3 Drafting (Blanket-Approval Mode)

Draft 3 chapters per batch. Each subagent gets: scene breakdown excerpts, continuity anchors, house style reference. Update progress.md table after each batch. Full reviews only for structurally complex chapters.

## 5. General Guidelines

- Verify subagent output (read file back, check word count) — don't trust "file written" claims
- Retry timed-out subagents solo
- Re-read shared files (progress.md) after sibling subagents may have modified them
