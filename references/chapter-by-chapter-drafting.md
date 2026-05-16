# Chapter-by-Chapter Drafting Process

**Derived from:** Proven author-preferred workflow — chapter-by-chapter with team review before proceeding

**Why:** The author wants to review each chapter before the next is written. No batching, no "write 10 chapters then review." One at a time, with team editorial standards applied during writing.

---

## The Chapter Cycle

For every chapter in Stage 5 (First Draft):

### 1. Select Next Chapter

Choose the next chapter from the approved scene breakdown. The chapter number, POV, and scene beats are already defined and reviewed.

### 1a. Build Chapter Brief

**Before writing a single word, build a chapter brief** — a consolidated writing packet for this chapter only. The scene breakdown alone is not enough context. The brief pulls together everything needed:

```
chapter-briefs/ch_NN-brief.md
├── Scene breakdown (from scenes/ch_NN.md)
├── Characters in this chapter
│   ├── Names, ages, occupations
│   ├── Current emotional/physical state
│   ├── Key traits relevant to this chapter
│   └── Relationship dynamics with other characters present
├── Setting details
│   ├── Location descriptions from world outline
│   ├── Atmosphere, season, time of day
│   └── Sensory details for authenticity
├── Tone & voice guide (from story bible)
├── Research check (specific facts needed)
├── Continuity markers
│   └── What this chapter plants for later (e.g., "Stuart scans exits → pays off Ch 17")
└── Word count targets per scene
```

The brief is saved in `chapter-briefs/ch_NN-brief.md` for reference. It ensures every chapter is written with full context — character profiles, world details, tone rules — not just the scene breakdown.

**Why this matters:** Without the brief, the writer is flipping between 6+ separate documents (scene breakdown, 2-3 character files, world outline, story bible, research notes) for each chapter. The brief consolidates everything into one file. It takes 2-3 minutes to build and saves significant context-switching overhead.

### 2. Write the Chapter

- Target: 2,000-2,500 words per chapter (verify with `wc -w <filename>`)
- Apply team editorial standards as you write:
  - **Alex:** Is this scene advancing the structure/arc?
  - **Jordan:** Is the prose flowing? Voice consistent?
  - **Casey:** Does this match established character/timeline details?
- Use [RESEARCH] tags for facts to verify later
- Use [CHECK] tags for continuity questions
- Forward motion is prioritised — write it, don't perfect it

### 3. Present to Author

Do NOT batch multiple chapters. Present exactly one.

Format:
```
## Chapter [N]: [Title]

[Full chapter text]

---

Ready for your review. Proceed to Chapter [N+1]?
```

### 4. Apply Author Feedback

Incorporate any changes the author requests. Do not argue. Do not defend. Apply the fix.

### 5. Wait for Confirmation

The author must explicitly say "Proceed to next chapter" or equivalent. Do not assume. Do not "while I wait, I'll write the next one." Wait.

### 6. Repeat

Select next chapter, write, present, get feedback, wait for confirmation.

---

## Midpoint Check-in

After approximately 18 chapters (half the book), convene Alex for a pacing/structure check. This is the only planned interruption. If the author wants additional check-ins, they'll ask.

## Common Pitfalls

- ❌ **Writing ahead while waiting.** Don't. The author may request changes that alter the next chapter.
- ❌ **Batching chapters for review.** The author said one at a time. One at a time.
- ❌ **Apologising for the pace.** The author set the pace. Follow it.
- ❌ **Assuming "looks good" means "proceed."** Wait for explicit confirmation.
