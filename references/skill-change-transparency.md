# Skill Change Transparency

Use this when updating the `military-thriller-team` skill or any of its support files during a novel session.

## Rule

If you modify the skill library, report the exact change in the same final status package.

Include:
- skill name
- file path inside the skill
- action used (`patch`, `edit`, `write_file`, etc.)
- one-line purpose
- concise before/after summary when a replacement occurred

## Distinguish read vs write

- `skill_view` is read-only. Do not describe it as a skill change.
- `search_files` over the skill directory is read-only. Do not describe it as a skill change.
- `skill_manage` writes to the skill library and must be reported.
- Direct `patch`/`write_file` to a skill path also writes to the skill library and must be reported.

## Why

Silent or unclear skill edits make it hard for Stuart to tell whether the workflow itself changed or whether only project files changed. Treat skill-library edits as durable process changes and make them explicit.

## Recommended final-status wording

```text
Skill library updated:
- military-thriller-team: references/example.md added — captures X workflow lesson.
- military-thriller-team/SKILL.md patched — added pointer to references/example.md.
```

If no skill files were changed, say that directly when asked. Do not infer a patch from read-only skill loads.