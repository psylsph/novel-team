# Design — Military Thriller Skill and Harness

## Goal

Convert the current general novel-team material into a focused system for writing modern adventure / military-based novels, then build a harness that enforces the process programmatically.

The skill provides the writing-room behavior. The harness prevents process drift.

## Current Direction

Skill identity:

> A disciplined fiction production room for modern military adventure thrillers, balancing action, authenticity, safety, character cost, and geopolitical stakes.

Core motto:

> Make it fast. Make it plausible. Make it hurt. Make the reader turn the page.

## Skill Design

### Major Changes Made / Intended

- Replace literary-salon personality model with operational thriller-room model.
- Add military adventure house style.
- Add genre-specific stages: Threat and Mission Design, Operational Environment, Mission Logic Pass.
- Add specialist roles:
  - Hayes — Military Authenticity Advisor
  - Vale — Geopolitical / Intelligence Analyst
  - Cross — Action Scene Director
- Add safety-aware research boundaries.
- Add genre-specific templates:
  - mission brief
  - threat profile
  - location intel brief
  - chapter brief
  - review output
  - progress and AGENTS templates

### Skill Responsibilities

The skill should:

- define stages and review gates
- define team personas
- define house style
- define deliverable templates
- define review standards
- define safety boundaries
- tell the agent what to load and when

The skill should not:

- manage machine state by itself
- trust the model to remember every gate unaided
- manually override harness-owned state

## Harness Design

### Why a Harness Is Needed

Agents forget process. Common failures:

- skip team review
- present drafts before review
- forget progress updates
- forget rolling summary
- advance stages without author confirmation
- fail to include required reviewers
- forget word counts
- drift into research or drafting before approval

The harness should enforce the process as a state machine.

Principle:

> The agent may generate content, but only the harness may advance the workflow.

### Recommended Toolkit

Use:

- TypeScript
- Pi SDK
- TypeBox or Zod for schemas
- Markdown files for human-readable artifacts
- JSON state for machine-readable enforcement
- Node fs/path for validation

Pi SDK is preferred because it can:

- create and manage agent sessions
- load the skill and project context
- subscribe to agent events
- inject corrective prompts
- provide custom tools
- inspect outputs and files between turns

### Harness Architecture

```text
harness/
├── src/
│   ├── index.ts
│   ├── session.ts
│   ├── state-manager.ts
│   ├── checklist-engine.ts
│   ├── validators/
│   │   ├── stage-validator.ts
│   │   ├── review-validator.ts
│   │   ├── file-validator.ts
│   │   └── wordcount-validator.ts
│   ├── prompts/
│   │   ├── corrective-prompts.ts
│   │   ├── stage-prompts.ts
│   │   └── review-prompts.ts
│   └── schemas/
│       ├── project-state.ts
│       ├── checklist.ts
│       └── deliverable.ts
├── checklists/
│   ├── stage-0.json
│   ├── stage-1.json
│   ├── stage-10-chapter.json
│   └── final-review.json
└── package.json
```

### Machine State

Use `progress.json` as harness-owned state. The agent may read it but should not directly edit it unless the harness explicitly delegates that action.

Example:

```json
{
  "project": "Book Title",
  "currentStage": 10,
  "currentChapter": 3,
  "requiredStep": "team_review",
  "blocked": true,
  "requiredReviewers": ["Alex", "Jordan", "Casey", "Hayes"],
  "completed": {
    "chapterBrief": true,
    "draftWritten": true,
    "teamReview": false,
    "fixesApplied": false,
    "presentedToAuthor": false,
    "authorApproved": false,
    "rollingSummaryUpdated": false,
    "progressUpdated": false
  }
}
```

### State Machine Example: Chapter Drafting

```text
read_context
→ create_chapter_brief
→ approve_or_review_brief
→ draft_chapter
→ team_review
→ apply_fixes
→ present_to_author
→ wait_for_author_confirmation
→ apply_author_revisions
→ update_rolling_summary
→ update_progress
→ advance_chapter
```

### Validation Examples

Before presenting a chapter:

- chapter file exists
- chapter brief exists
- review file exists
- required reviewers present
- each reviewer has at least 5 issues or documented exception
- fixes applied section exists
- word count measured with `wc -w`

Before advancing a stage:

- all stage deliverables exist
- review gate complete
- author confirmation recorded
- progress.md updated
- AGENTS.md updated

### Corrective Prompt Pattern

If the agent violates process, the harness sends:

```text
PROCESS VIOLATION: You attempted to [action] before [missing requirement].

Current stage: [stage]
Current required step: [step]
Missing items:
- [item]

Stop advancing. Complete the missing step now using [template/personas].
Do not present to the author until the gate passes.
```

### Minimum Viable Harness

Version 1 should include:

- project initialization
- `progress.json` creation
- stage state machine
- chapter cycle state machine
- review gate validator
- file existence checks
- corrective prompts
- word count verification for chapters

Version 2:

- reviewer-specific section validation
- author decision tracking
- act-break review enforcement
- continuity pass reminders
- dashboard/status command

Version 3:

- TUI or web UI
- approval buttons
- project browser
- timeline/continuity database
- character/faction database

## Implementation Notes

- Do not overbuild first.
- Make the harness boring and strict.
- Keep creative decisions inside the agent/author loop.
- Keep workflow advancement inside the harness.
- Prefer explicit state transitions over LLM self-reporting.
