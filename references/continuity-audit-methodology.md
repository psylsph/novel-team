# Continuity Audit Methodology — Cross-Chapter Consistency Pass

**When to run:** Three distinct phases:
1. **During drafting** — After each 5-10 chapter batch, per Stage 11.
2. **Post-draft full-book audit** — After all 17+ chapters exist and the first draft is structurally complete, run a comprehensive audit across ALL chapters. This catches inconsistencies introduced by parallel expansion or by different subagents handling different chapters.
3. **After expansion pass** — Re-audit after the systematic expansion pass to catch any continuity drift introduced by added text.

**Purpose:** Identify timeline conflicts, numeric contradictions, character inconsistencies, and plot holes across chapters.

## Methodology

### 1. Build a Timeline Anchor

Extract every stated or implied timestamp from each chapter. Build a master timeline:

```
Ch1: "Nearly seven" (18:45) — Vilnius hotel, blackout begins
Ch2: "Almost eight" (19:45) — Hotel lobby, movement to consulate
Ch3: ~19:45-20:15 — Consular trap, escape
...
Ch6: Dawn next day ~06:00 — Train to Warsaw
...
```

**Check for:** Events that happen at different times in different chapters. The most common error is referencing a key event time in a later chapter that contradicts the established timeline.

**Fix:** If a later chapter mis-states the time of an earlier event, update the later chapter to match the established timeline. The earlier chapters' timeline is authoritative — they were written closest to the events.

### 2. Numeric Consistency Check

Extract every number stated in the narrative and create a numeric ledger:

| Number | Value | Chapters | Consistent? |
|--------|-------|----------|-------------|
| Blackout start | ~18:45 | Ch1, Ch2, Ch5 | Check |
| Consulate fall | ~20:00 | Ch3, Ch9 | Check |
| Hostage count (public) | 42 | Ch9, Ch11, Ch12, Ch13 | Check |
| Hotel lobby count | 53 | Ch2, Ch9, Ch11, Ch15 | Check |
| Phantom names | 19 | Ch13 | Check |

**Common numeric traps (check these first):**
- Public claim numbers changing between chapters (e.g. hostage count 42 becomes 32)
- Arithmetic that doesn't balance (e.g. 42 - 23 must equal 19, not 9)
- Hotel/room/location counts that escalate without explanation (e.g. 53 becomes 59)
- "X unaccounted for" must match the arithmetic of the other numbers (e.g. 53 - 42 = 11)
- Elapsed time between events must match between chapters
- The word "approximately" hides a mismatch — audit it explicitly

**Fix:** Pick ONE authoritative number and use it everywhere. Fix all arithmetic derived from it.

### 3. Character Fate Tracking

For every named character, track their state across chapters and whether their fate is resolved by the end.

**Check for:**
- Characters who serve a plot function then vanish without resolution (e.g. David Price, Markus Keller)
- Characters whose fate is implied but never confirmed
- Characters inconsistently named or with title changes across chapters

**Fix:** Add one line in the debrief/aftermath chapter confirming the character's fate.

### 4. Plot Consistency

Check:
- **Duplicate events:** The same scene described in two different chapters as if they're different events. Fix: change one to involve a different location/sector/personnel.
- **Parallel timelines:** Events in Chapter A that should affect Chapter B but don't. Fix: seed the event in the earlier chapter.
- **Knowledge consistency:** Does the team in Chapter N+1 know what they learned in Chapter N?
- **Format consistency:** A later chapter describing something in a format that doesn't match earlier descriptions. Fix: reframe to avoid format claims (e.g. "same hand" not "same format").

### 5. Setting Consistency

If a room/office/location moves (e.g. coordination room from basement to 3rd floor), add a transition note in the later chapter explaining the move.

### 6. Loose Thread Closure

Before marking the draft complete, verify: every named character has a fate, every plot question is answered or deliberately left as a series thread, and the epilogue doesn't introduce format inconsistencies with earlier messaging.

### 7. Post-Expansion Audit (delegate_task risk)

When chapters were expanded via parallel `delegate_task` subagents, run an additional audit pass that checks specifically for character-descriptor errors introduced by the expansion system.

**Known risks of subagent expansion:**
- **Gender pronoun flips** — Subagents can misread character gender from context and introduce he/him → she/her (or vice versa) errors. This is the most common critical bug introduced by parallel expansion. Run `grep -n "Turner.*he\|Turner.*him\|Turner.*his" chapter-*.md` to catch gender mismatches.
- **Descriptor drifts** — Physical attributes (eye colour, height, uniform details), role titles (Defence Attaché vs Colonel), and relationship labels (husband vs partner) can shift between chapters processed by different subagents.
- **Continuity anchor erosion** — Timestamps, numeric values, and named locations that were specified as "critical continuity anchors" in the expansion brief may have degraded or been dropped.

**Fix protocol:** After any parallel expansion batch, read the continuity audit files from the previous pass, then spot-check the expanded chapters against the anchors. Fix all 🔴 and 🟡 items before presenting to the author.

## Severity Rating System

When reporting findings to the author, use severity labels to prioritise fixes:

| Label | Meaning | Examples |
|-------|---------|---------|
| 🔴 **Critical** | Makes the story unreadable or logically impossible | Timeline contradictions (consulate falls at two different times), arithmetic that doesn't balance (42-23=9 instead of 19), characters being in two places at once |
| 🟡 **Moderate** | Confuses the reader or undermines credibility | Duplicate scenes described as separate events, minor numeric drift without explanation, unresolved character fates, parallel timelines that should intersect but don't |
| 🟢 **Minor** | Polishing issues | Duplicate paragraphs from editing artifacts, room changes without transition notes, evolving discrepancy that needs clearer tracking |

**Rule:** Fix all 🔴 items before presenting to the author. Fix 🟡 items when possible; if a 🟡 fix requires an author decision (e.g. choosing a character's fate), flag it in the review. Note 🟢 items for the polishing pass.
