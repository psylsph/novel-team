# Novel Team — Installation & Setup

This is the novel-team skill for pi. It provides a complete novel production pipeline with 8 professional team roles and a 16-stage development process.

## Skill Files

The skill itself is self-contained in this directory. See `SKILL.md` for the rules card and `references/` for stage details, templates, and examples.

## Session Continuity (AGENTS.md)

Every project using this skill **must** have an `AGENTS.md` file in its root directory (SKILL.md Rule 4). This file is the first thing a new agent reads when a session restarts — it explains what the project is, where the skill lives, and how to resume work.

When a new agent session starts in a project directory, pi's AGENTS.md convention means the agent automatically reads this file. The AGENTS.md tells it:

1. This is a novel project using the novel-team skill
2. Where to find the skill (`~/.pi/agent/skills/novel-team/SKILL.md`)
3. To read `progress.md` for current state
4. To read `rolling-summary.md` if drafting
5. What stage the project is at and what to do next

This means **agent restarts don't lose context**. A fresh session reads AGENTS.md, loads the skill, reads progress.md, and picks up exactly where the last session left off.

## Optional: Workflow Checker Agent

The most common problem with complex skills is the main agent forgetting workflow steps — skipping reviews, missing checklists, jumping ahead. The skill's `progress.md` tracking (Rule 3) helps, but a separate checker agent with its own clean context window is more reliable.

### How It Works

A **novel-checker** agent runs in an isolated pi subprocess. It doesn't share the main agent's context — it reads only the rules and the current project state, then reports what's been missed. The main agent calls it before presenting any deliverable to the author:

```
Use novel-checker to audit the workflow before we present to the author
```

### Setup

**1. Install the subagent extension** (if not already installed):

```bash
mkdir -p ~/.pi/agent/extensions/subagent
mkdir -p ~/.pi/agent/agents
mkdir -p ~/.pi/agent/prompts

EXAMPLES="$(npm root -g)/@earendil-works/pi-coding-agent/examples/extensions/subagent"

ln -sf "$EXAMPLES/index.ts" ~/.pi/agent/extensions/subagent/index.ts
ln -sf "$EXAMPLES/agents.ts" ~/.pi/agent/extensions/subagent/agents.ts

for f in "$EXAMPLES"/agents/*.md; do
  ln -sf "$f" ~/.pi/agent/agents/$(basename "$f")
done

for f in "$EXAMPLES"/prompts/*.md; do
  ln -sf "$f" ~/.pi/agent/prompts/$(basename "$f")
done
```

**2. Create the novel-checker agent:**

```bash
cat > ~/.pi/agent/agents/novel-checker.md << 'EOF'
---
name: novel-checker
description: Audits novel-team workflow compliance — checks that no steps were skipped, the review gate was followed, and progress.md is accurate. Use before presenting any deliverable to the author.
tools: read, grep, find, ls
model: claude-sonnet-4-5
---

You are a novel-team workflow auditor. Your job is to verify that the agent working on a novel has followed all required steps and not skipped anything.

You will be given:
1. The path to the project directory
2. The current stage or deliverable being worked on

**What you must do:**

1. Read the project's `progress.md` — this is the agent's state file
2. Read the skill rules at `~/.pi/agent/skills/novel-team/SKILL.md`
3. Read the relevant stage details at `~/.pi/agent/skills/novel-team/references/stages.md`
4. Cross-check progress.md against the stage checklist
5. Verify the review gate was followed for the current deliverable

**Output format:**

## Workflow Audit: [Deliverable Name]

### Stage Progress
- [x] or [ ] for each completed/skipped stage

### Current Stage Checklist
Copy the checklist from stages.md. Mark each item [x] or [ ] based on what progress.md and the project files show.

### Review Gate
- [x] or [ ] Team review completed
- [x] or [ ] All reviewers listed in SKILL.md Rule 1 table were used
- [x] or [ ] Review output follows Rule 10 format
- [x] or [ ] Fixes applied before presentation

### Issues Found
1. [CRITICAL / WARNING / NOTE]: Description
2. ...

### Verdict: [PASS — ready to present / FAIL — fix these first]

**Rules:**
- Be strict. If progress.md doesn't explicitly say something was done, treat it as not done.
- The review gate is the most common failure point. Check it carefully.
- If the stage checklist in stages.md has an item that isn't reflected in progress.md or project files, flag it.
- Do not fix anything. Only report what's missing or wrong.
- Never approve work that hasn't been through team review. This is non-negotiable.
EOF
```

**3. Verify it works:**

```bash
pi -p "list the available subagents"
```

You should see `novel-checker` in the list alongside `scout`, `planner`, `reviewer`, and `worker`.

### When to Call the Checker

The main agent should call the checker:
- **Before presenting any deliverable to the author** (after team review, before the WAIT step)
- **Before advancing to a new stage** (verify the current stage is complete)
- **After any long context window** (if the agent has been working for many turns)

Example invocation:
```
Use the subagent tool with novel-checker to audit the current workflow state. Project directory: ~/novels/my-book/. Current deliverable: Chapter 3 first draft.
```

### Customisation

- **Model:** Change `model` in the agent file to use a cheaper model for routine checks (e.g., `claude-haiku-4-5`) or a more capable one for complex audits
- **Scope:** The checker only reads files — it cannot modify anything. It's purely an auditor
- **House style:** If you've added a `references/house-style-*.md` file to the skill, the checker can verify prose compliance too — add instructions to the agent definition

## File Structure

```
novel-team/
├── SKILL.md                              # Rules card (always loaded, 10 rules)
├── README.md                             # This file — installation & setup
├── references/
│   ├── stages.md                         # Full 16-stage plan with checklists
│   ├── house-style-higgins.md            # Jack Higgins house style reference
│   ├── pitfalls.md                       # Common mistakes and how to avoid them
│   ├── examples.md                       # Real workflow examples
│   ├── fast-track-from-outline.md        # Accelerated workflow for existing outlines
│   ├── chapter-by-chapter-drafting.md    # Detailed drafting process
│   ├── autonomous-workflow-example.md    # Example of autonomous team resolution
│   ├── act-break-review-results-example.md # Example act-break review report
│   └── role-research-methodology.md      # How team roles were defined
├── team/
│   ├── ROSTER.md                         # Assignment table and role boundaries
│   ├── editorial/                        # Alex, Jordan, Taylor, Morgan
│   ├── specialists/                      # Riley, Casey, Quinn
│   └── support/                          # Sam
└── templates/                            # Reusable document templates
    ├── chapter-brief.md
    ├── character-profile.md
    ├── setting-profile.md
    └── rolling-summary.md
```

## Project Directory Structure

When starting a new book, the project directory will contain:

```
book-name/
├── AGENTS.md                # Session continuity — agent reads this on restart
├── progress.md              # Current stage, status, next action
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
