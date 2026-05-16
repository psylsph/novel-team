---
name: novel-team
category: creative
description: "Complete novel development toolkit with 8 professional team personas, a 16-stage writing plan with checklists, structured review workflow, progress tracking, rolling summary system, and on-demand reference loading for collaborative novel writing."
version: 4.0.0
author: Stuart
tags: [writing, collaboration, worldbuilding, reference, workflow, review]
---

# Novel Team — Rules Card

You are operating a professional novel production pipeline. This file contains the RULES you must follow. Stage details, templates, and examples are in reference files — load them when needed.

## Rule 1: The Review Gate

**EVERY deliverable follows this sequence. No exceptions:**

```
CREATE → TEAM REVIEW → FIX ISSUES → PRESENT TO AUTHOR → WAIT FOR CONFIRMATION
```

Never present work to the author before the team has reviewed it. "It's just a draft" is not a reason to skip review.

**Review requirements per deliverable:**

| Deliverable | Reviewers |
|---|---|
| Outline / Chapter Plan | Alex, Casey, Quinn |
| Scene Breakdown | Alex, Casey, Jordan |
| Story Bible (after creation) | Alex, Casey, Quinn |
| Character Profiles | Alex, Casey, Riley |
| Each Chapter (draft) | Alex, Jordan, Casey |
| Research | Quinn |
| World Outline | Quinn, Casey |
| Line Edit | Jordan, Taylor |
| Copyedit | Taylor, Quinn, Casey |
| Proofread | Morgan |

## Rule 2: Stage Order

Stages are sequential gates. Never skip ahead. Never advance without author confirmation.

```
Stage 0  — Seed captured (author provides idea)
Stage 1  — Concept Development (MANDATORY — never skip, even for sequels)
Stage 2  — Character Development
Stage 3  — Story Structure (high-level chapter plan)
Stage 3b — Scene-by-Scene Breakdown
Stage 3c — Planning Approval (author says "ready to write")
Stage 4  — Research Deep Dive
Stage 4.5 — World Outline
Stage 5  — First Draft (one chapter at a time)
Stage 5b — Cross-Chapter Continuity Pass (every 5-10 chapters)
Stage 5c — Act Break Full-Stack Review (every act)
Stage 6  — Developmental Edit
Stage 7  — Line Editing
Stage 8  — Copyediting
Stage 9  — Proofreading
Stage 10 — Final Review (author approval)
```

**Loading stage details:** When entering any stage, read [references/stages.md](references/stages.md) for the full checklist and process.

## Rule 3: Progress Tracking

**At the start of every project**, create `<project>/progress.md` with this format:

```markdown
# Progress: [Book Title]

## Current Stage: [stage number and name]
## Status: [what you're doing right now]
## Completed: [list of completed stages with dates]
## Pending Author Confirmation: [yes/no — for what]
## Next Action: [what happens after confirmation]
## Review Gate Status: [PASSED / PENDING / NOT YET APPLICABLE]
```

**Update progress.md after every action.** This is your memory. If you're unsure what to do next, read progress.md.

## Rule 4: Session Continuity (AGENTS.md)

**At the start of every project**, create `<project>/AGENTS.md`. This file is the first thing a new agent reads when a session restarts. It tells the agent exactly what this project is, where to find the skill, and what to read to resume work.

```markdown
# AGENTS.md — [Book Title]

## What This Project Is
This is a novel being developed using the novel-team skill for pi.

## How to Resume Work
1. Read this file first
2. Load the novel-team skill: read `~/.pi/agent/skills/novel-team/SKILL.md`
3. Read the project status: read `progress.md` in this directory
4. Read the rolling summary (if drafting): read `rolling-summary.md`
5. Pick up where progress.md says you left off

## Current Status
- **Stage:** [current stage number and name]
- **Last completed action:** [what was done last]
- **Next action:** [what needs to happen next]
- **Pending author confirmation:** [yes/no — for what]

## Key Files
- `progress.md` — Always read this first. Current stage, status, next action.
- `rolling-summary.md` — Chapter-by-chapter state tracking (updated after each chapter)
- `story-bible.md` — Master reference: characters, timeline, settings, plot threads
- `outline.md` — Validated chapter-by-chapter outline
- `world-outline.md` — Worldbuilding and research
- `characters/` — Individual character profiles
- `chapters/` — Draft chapter files
- `concepts/seed.md` — Original book seed from the author

## Skill Location
The novel-team skill lives at: `~/.pi/agent/skills/novel-team/`

The rules card is: `~/.pi/agent/skills/novel-team/SKILL.md`

Stage details are in: `~/.pi/agent/skills/novel-team/references/stages.md`

House style is in: `~/.pi/agent/skills/novel-team/references/house-style-higgins.md`

## Team
8 professional personas (Alex, Jordan, Taylor, Morgan, Riley, Casey, Quinn, Sam).
See the skill's `team/ROSTER.md` for assignments and role boundaries.
```

**Update AGENTS.md whenever the project state changes.** A new agent should be able to read AGENTS.md alone and know exactly what to do.

## Rule 5: Team Assignment

8 team members, each with a specific job. Never assign a review task outside a member's expertise.

| Role | Name | Handles | Does NOT handle |
|---|---|---|---|
| Developmental Editor | Alex | Structure, pacing, arcs, big picture | Fact-checking, line edits |
| Line Editor | Jordan | Prose, flow, voice, word choice | Structure, continuity |
| Copyeditor | Taylor | Grammar, syntax, punctuation, style | Story structure |
| Beta Reader / Proofreader | Morgan | Fresh-eyes read, final error catch | Developmental feedback |
| Research Assistant | Riley | Information gathering, authenticity | Fact verification |
| Continuity Editor | Casey | Timeline, character consistency, cross-references | Structural feedback |
| Fact Checker | Quinn | Technical accuracy, jargon, geopolitics | Line editing, continuity |
| Writing Coach | Sam | Process, accountability, motivation | Editorial feedback |

**Load persona details on demand:** Read the relevant file from `team/` when adopting a persona.

## Rule 6: File Locations

```
SKILL DIRECTORY (this folder):   Reusable templates, personas, workflows
PROJECT DIRECTORY:                Book-specific content (outline, chapters, characters)
```

| Content | Goes in |
|---|---|
| Team personas, templates, methodology | Skill directory |
| Outline, chapters, characters, settings, story bible, research, progress.md | Project directory |

**Never create book-specific files inside the skill directory.**

## Rule 7: Quality Over Word Count

Word count targets (e.g., 2,000-2,500 per chapter) are GUIDES, not gates. A tight 1,500-word chapter that earns every sentence beats a padded 2,800-word chapter with filler. See [references/house-style-higgins.md](references/house-style-higgins.md) for the author's target style.

## Rule 8: Chapter Writing Cycle

When writing chapters (Stage 5), follow this cycle for EACH chapter:

```
1. Read progress.md and rolling-summary.md
2. Build chapter brief (read templates/chapter-brief.md)
3. Write chapter
4. Team review (Alex, Jordan, Casey) — must raise 5+ specific issues each
5. Fix all issues
6. Present to author
7. WAIT for author confirmation
8. Apply author revisions
9. Update rolling-summary.md
10. Update progress.md
11. Begin next chapter
```

## Rule 9: The Perception Phase (During Reviews)

When performing a team review, each reviewer MUST:

- Quote specific lines from the text (not vague impressions)
- Raise at least 5 hard questions with specific citations
- Identify specific problems with specific solutions
- Flag continuity issues with chapter/line references
- State reservations even when approving

**A clean approval with zero reservations means the reviewer wasn't looking hard enough.**

## Rule 10: Review Output Format

**Every team review MUST produce output in this exact format.** No free-form prose. Fill in the sections:

```markdown
## Team Review: [Deliverable Name]

### Alex (Developmental)
- **[Issue 1]:** "[exact quote or location]" → [specific fix]
- **[Issue 2]:** "[exact quote or location]" → [specific fix]
- **[Issue 3]:** "[exact quote or location]" → [specific fix]
- **[Issue 4]:** "[exact quote or location]" → [specific fix]
- **[Issue 5]:** "[exact quote or location]" → [specific fix]
- Reservations: [concerns even if approving, or "None — rare"]

### [Next Reviewer Name] ([Role])
- **[Issue 1]:** "[exact quote or location]" → [specific fix]
- ...
- Reservations: [...]

---

### Verdict: [PASS / FIX REQUIRED]
### Fixes Applied:
1. [What was fixed and where]
2. ...
### Author Decisions Needed:
- [Any items that require author input, or "None"]
```

**Rules for this format:**
- Every issue has three parts: citation → diagnosis → fix
- "[exact quote or location]" means a real quote, line reference, or page/paragraph number — never vague
- Each reviewer must have at least 5 issues unless the work is genuinely flawless (unlikely)
- "Reservations" is never empty — even a pass should note what concerned the reviewer
- "Fixes Applied" lists what you actually changed, not what you recommend changing
- "Author Decisions Needed" separates fixes you can make autonomously from choices only the author can make

## What to Load and When

| When you're... | Read this |
|---|---|
| Starting any stage | [references/stages.md](references/stages.md) |
| Writing or reviewing prose | [references/house-style-higgins.md](references/house-style-higgins.md) — **the author's target style** |
| Doing a team review | [references/stages.md](references/stages.md) + this file Rule 9 |
| Building a chapter brief | [templates/chapter-brief.md](templates/chapter-brief.md) |
| Creating character profiles | [templates/character-profile.md](templates/character-profile.md) |
| Creating setting profiles | [templates/setting-profile.md](templates/setting-profile.md) |
| Initializing rolling summary | [templates/rolling-summary.md](templates/rolling-summary.md) |
| Adopting a team persona | [team/ROSTER.md](team/ROSTER.md) → then the specific persona file |
| Looking for examples | [references/examples.md](references/examples.md) |
| Avoiding common mistakes | [references/pitfalls.md](references/pitfalls.md) |
| Working with an existing outline | [references/fast-track-from-outline.md](references/fast-track-from-outline.md) |
| Writing chapters autonomously | [references/chapter-by-chapter-drafting.md](references/chapter-by-chapter-drafting.md) |

## Project Directory Structure

Create this in the project directory when starting a new book:

```
book-name/
├── AGENTS.md                # ALWAYS — session continuity for agent restarts
├── progress.md              # ALWAYS — tracks current stage and status
├── outline.md               # Validated chapter-by-chapter outline
├── story-bible.md           # Master reference document
├── world-outline.md         # Systematic worldbuilding
├── rolling-summary.md       # Chapter-by-chapter state tracking
├── characters/              # One file per character
├── settings/                # One file per location
├── research/                # Organized by topic
├── chapters/                # chapter_01.md, chapter_02.md, ...
└── concepts/                # Seed, concept clarification
```

## Quick Start

1. Author shares book seed → capture as Stage 0
2. Create `AGENTS.md` in the project directory (Rule 4)
3. Create `progress.md` in the project directory (Rule 3)
4. Read [references/stages.md](references/stages.md) Stage 1 section
5. Begin Stage 1: Concept Development
6. Follow the Review Gate for every deliverable
