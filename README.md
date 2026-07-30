# Military Thriller Team

A professional writing-room skill for **Hermes Agent** that produces modern military adventure/thriller novels with a strict gated workflow, tactical plausibility, geopolitical stakes, action clarity, continuity tracking, and safety-aware research boundaries.

## What This Is

This skill transforms a single AI agent into a full writing team — story editor, prose editor, beta reader, researcher, continuity editor, fact checker, military advisor, intelligence analyst, action director, and writing coach — each adopting a defined persona to review deliverables from their specialist lens.

The workflow runs 18 stages from seed capture through final proofreading, with mandatory multi-reviewer gates, proactive fix-and-advance behavior, and strict continuity tracking.

## Core Standard

> Make it fast. Make it plausible. Make it hurt. Make the reader turn the page.

## Structure

```
SKILL.md                          — Rules card (start here)
DESIGN.md                         — Harness/state-machine design
team/
  ROSTER.md                       — Team overview
  editorial/                      — Author, story editor, prose editor, beta reader
  specialists/                    — Continuity, fact checker, researcher, military advisor, intel analyst, action director
  support/                        — Writing coach
references/                       — Stage workflows, house style, action principles, military authenticity, research safety, review methodology
templates/                        — Review output, chapter briefs, character profiles, mission briefs, threat profiles, location intel, AGENTS.md, progress.md
```

## Installation

Copy this directory into your Hermes skills folder:

```bash
cp -r military-thriller-team ~/.hermes/skills/creative/
```

Then load it in a session:

```
skill_view(name='military-thriller-team')
```

## Pairing With the Right Model

Looking for the best LLM for creative writing? Check the [EQ-Bench Creative Writing leaderboard](https://eqbench.com/creative_writing.html) for model recommendations ranked on prose quality, dialogue, and narrative — so you can pair the right model with this team.

## License

MIT
