# Current-Directory Project Boundary

Use this when the author says any version of:

- "do not look for files outside the current directory"
- "begin here"
- "use this attached seed"
- "do not search other project folders"

## Rule

Treat the current working directory as the complete project boundary unless the author explicitly grants an exception.

Do:
- Scan only `.` and its children for project state.
- Use attached files and files in the current directory as the source of truth.
- Create/update project files under the current directory only.
- Report the absolute current directory in status updates so the boundary is visible.
- If a non-project config change is explicitly requested later (for example, Hermes `.env`), treat that as a separate explicit exception and state it.

Do not:
- Search sibling directories for previous versions of the book.
- Import state from similarly named projects elsewhere.
- Use remembered project paths to override the active working directory.
- Patch files in another profile, repo, or project unless the author explicitly says to.

## State Verification Pattern

At project start or stage transition, verify from inside the current directory:

```bash
pwd
find . -maxdepth 2 -type f
printf 'chapter files: '; (test -d chapters && find chapters -maxdepth 1 -type f | wc -l || printf '0\n')
printf 'review files: '; (test -d reviews && find reviews -maxdepth 1 -type f | wc -l || printf '0\n')
```

Then read the local tracking files if present:

- `progress.md`
- `AGENTS.md`
- `rolling-summary.md`
- `progress.json`, if present

If tracking files are absent but a seed is present, initialise local project state in the current directory rather than searching elsewhere.

## Reporting

When presenting results, include:

- `Worked only inside: [absolute cwd]`
- files created/updated relative to that directory
- any explicitly authorised exception outside the directory, if one occurred
