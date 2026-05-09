# Novel Team — Complete Professional Novel Development System

[![Version](https://img.shields.io/badge/version-3.0.0-blue.svg)](SKILL.md)
[![Category](https://img.shields.io/badge/category-creative-ff69b4.svg)](.)

**A full professional editorial team and 10-stage development pipeline, delivered as a structured knowledge system for AI-assisted novel writing.**

This repository contains the SKILL.md, persona files, templates, and reference material that power the novel-team workflow. Designed for use with AI agents (Hermes, Claude, or compatible systems), it gives you a dedicated team of eight publishing professionals with distinct personalities, clear expertise boundaries, and a rigorous stage-based development process.

---

## What's Inside

### 🎭 The Team (8 Professional Personas)

| Role | Name | Expertise |
|------|------|-----------|
| **Developmental Editor** | Alex | Story structure, character arcs, pacing, plot logic |
| **Line Editor** | Jordan | Prose flow, word choice, rhythm, voice consistency |
| **Copyeditor** | Taylor | Grammar, punctuation, style guide, technical polish |
| **Proofreader / Beta Reader** | Morgan | Final error check, formatting, fresh-eyes read |
| **Research Assistant** | Riley | Historical/technical research, setting authenticity |
| **Continuity Editor** | Casey | Timeline, character tracking, world-building consistency |
| **Fact Checker** | Quinn | Factual accuracy, technical detail verification |
| **Writing Coach** | Sam | Goal setting, accountability, overcoming blocks |

Each persona lives in `team/` with a full profile — distinct voice, style, knowledge boundaries, and communication approach.

### 📋 The 10-Stage Workflow

| # | Stage | Lead | Deliverable |
|---|-------|------|-------------|
| 0 | Initial Seed | Author | Raw concept captured |
| 1 | Concept Development | Alex + Riley + Sam | Concept clarification document |
| 2 | Character Development | Alex + Casey + Riley | Complete character profiles |
| 3 | Story Structure | Alex + Casey | Chapter plan + scene breakdown |
| 3c | Planning Approval | All team + Author | Green light to write |
| 4 | Research Deep Dive | Riley + Quinn | Research repository |
| 4.5 | World Outline | Riley + Alex + Casey | World outline document |
| 5 | First Draft | Author + Sam | Complete manuscript |
| 5b | Cross-Chapter Continuity | Casey | Consistency verified every 5-10 ch |
| 5c | Act Break Full-Stack Review | All team | Comprehensive quality gate |
| 6 | Developmental Edit | Alex + Casey + Riley | Revised draft |
| 7 | Line Editing | Jordan + Taylor | Line-edited draft |
| 8 | Copyediting | Taylor + Quinn + Casey | Copyedited draft |
| 9 | Proofreading | Morgan | Final error-free draft |
| 10 | Final Review | Author | Approved manuscript |

### 📁 Documentation

| File | Description |
|------|-------------|
| `SKILL.md` | Complete system documentation (workflow, templates, rules) |
| `QUICKSTART.md` | Quick reference — team members, usage patterns |
| `WORKFLOW.md` | Detailed walkthrough of all stages with checklists |
| `EXAMPLES.md` | Real scenarios showing the team in action |
| `team/ROSTER.md` | Full team member directory |
| `references/` | Research methodology, workflow examples |
| `templates/` | Reusable templates (chapter brief, character profile, etc.) |
| `CHANGELOG.md` | Version history and release notes |
| `CONTRIBUTING.md` | How to contribute — personas, workflows, templates |
| `LICENSE` | MIT License — free to use, modify, share |

---

## How to Use

### Option 1: Start a New Novel

```
"I have a book seed. Let's start with Stage 1: Concept Development."

Then share your concept, character, setting, or scene.
```

### Option 2: Consult a Team Member

```
"As Jordan, review this passage and improve the prose..."
"Riley, I need research on submarine operations..."
"Casey, check if this detail matches what we established earlier..."
```

### Option 3: Hold a Team Meeting

```
"Team meeting: Alex, Casey, and Riley to discuss this scene..."
```

### Option 4: Progressive Refinement

```
1. Alex: "Does this scene work structurally?"
2. Riley: "How can I make the details more authentic?"
3. Jordan: "Now improve the prose flow..."
4. Taylor: "Finally, polish the technical details..."
```

---

## Key Principles

### 🔴 The Review Gate (Highest Priority)

Every deliverable must go through full team review before being presented to the author:

```
CREATE → REVIEW → FIX → PRESENT TO AUTHOR → WAIT FOR CONFIRMATION
```

This is non-negotiable. No skipping, no rubber-stamping, no "just a draft" exceptions.

### 🔍 The Perception Phase

Each reviewer must actually read the work critically — quote specific lines, raise minimum 5 hard questions, flag continuity issues with references. Superficial reviews are rejected.

### 🎯 Quality Over Word Count

Word targets are guides, not gates. A tight 2,200-word chapter that earns every sentence beats a padded 3,000-word chapter with filler.

### 🚦 Author Control at Every Stage

The team advises. The author decides. No gate passes without author confirmation.

---

## Repository Structure

```
novel-team/
├── README.md                  # This file
├── SKILL.md                   # Complete system (workflow, templates, rules)
├── QUICKSTART.md              # Quick reference guide
├── WORKFLOW.md                # Detailed stage walkthrough
├── EXAMPLES.md                # Real team-in-action scenarios
├── team/
│   ├── ROSTER.md              # Team directory
│   ├── editorial/             # Alex, Jordan, Taylor, Morgan
│   ├── specialists/           # Riley, Casey, Quinn
│   └── support/               # Sam
├── references/                # Research methodology, examples
└── templates/                 # Chapter brief, character profile, etc.
```

For book projects, the skill goes in the agent's skills directory and project files go in a separate book project directory:

```
SKILL:  ~/.hermes/skills/creative/novel-team/   ← templates, personas, workflows
PROJECT: ~/writing/your-novel/                   ← chapters, characters, settings
```

---

## Installation

### For Hermes Agent

```bash
# The skill is available as part of the Hermes skill registry
hermes skills download novel-team
```

### For Direct Use

Clone or copy this repository, then load `SKILL.md` as your agent's context or instruction file.

---

## Requirements

- An AI agent system capable of persona adoption (Hermes, Claude, or compatible)
- For the full workflow: ability to create and manage project files
- 8 team persona files (included) for distinct reviewer voices

---

## Quick Start

```
"Alex, review this chapter outline and tell me if the pacing works."
"I have a thriller concept: burned spy discovers his agency is hunting him."
"Team meeting: Alex, Casey, and Riley — let's plan the opening scene."
```

See `QUICKSTART.md` for full usage patterns and team member reference.

---

## Related Projects

Other writing tools from the same author:

| Project | Description |
|---------|-------------|
| [autonomous-booksmith](https://github.com/psylsph/autonomous-booksmith) | Autonomous multi-agent novel writing pipeline |
| [ai-book-writer](https://github.com/psylsph/ai-book-writer) | Experiment: full novel generation via AutoGen agents |
| [novel-writer](https://github.com/psylsph/novel-writer) | Novel writing tool |
| [BookAgent](https://github.com/psylsph/BookAgent) | Book-oriented AI agent system |
| [StoryFoundry](https://github.com/psylsph/StoryFoundry) | Story creation and development framework |
| [prosewrite](https://github.com/psylsph/prosewrite) | Prose writing assistant |

### Model Evaluation & Benchmarking

| Resource | Description |
|----------|-------------|
| [EQ-Bench Creative Writing](https://eqbench.com/creative_writing.html) | Creative writing model evaluation leaderboard — see how LLMs rank on prose, dialogue, and narrative quality |
| [EQ-Bench](https://github.com/EQ-bench) | Open-source model evaluation suite — emotional intelligence and creative writing benchmarks for LLMs |

---

## License

Part of the psylsph/novel-team project. See repository metadata for details.

---

<div align="center">
<i>Your Novel Team awaits. 🎭✨</i>
</div>
