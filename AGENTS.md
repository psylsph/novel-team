# AGENTS.md — novel-team skill

## What This Is
This is the novel-team pi skill — a novel production pipeline with 8 team personas and a 16-stage development process. Changes here affect any project using this skill.

## Rules for Modifying This Skill
- **Always bump the version** in `SKILL.md` frontmatter after any substantive change
- **Never duplicate information** across files — state it once, reference it elsewhere
- **All markdown links must resolve** from the file they're in (SKILL.md from skill root, ROSTER.md from team/, references/ from their own directory)
- **Run `grep -oP '\]\(\K[^)]+' <file>` and verify paths exist** after editing any markdown file
- **Keep SKILL.md under 250 lines** — it's the rules card that fits in small model context. If it grows, move detail to references/

## Current Version
4.6.0

## File Responsibilities
| File | Purpose | Loaded when |
|---|---|---|
| `SKILL.md` | Rules card — 10 hard rules | Always (must stay small) |
| `references/stages.md` | Full 16-stage plan with checklists | Entering a new stage |
| `references/house-style-higgins.md` | Jack Higgins target style | Writing or reviewing prose |
| `references/pitfalls.md` | Known mistakes | Troubleshooting |
| `references/examples.md` | Real workflow examples | Looking for examples |
| `team/ROSTER.md` | Assignment table + role boundaries | Adopting a persona |
| `team/*/` | Individual persona files | Adopting a specific persona |
| `templates/` | Document templates | Creating characters, chapters, etc. |
| `README.md` | Installation & setup docs | Installing the skill |

## After Making Changes
1. Bump version in `SKILL.md` frontmatter
2. Update version in this file
3. Verify all markdown links resolve
4. `git add -A && git commit -m "vX.Y.Z: description" && git push origin main`
