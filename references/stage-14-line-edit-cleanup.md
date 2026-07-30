# Stage 14 — Line Edit / Watchlist Cleanup

Use this when Stage 13 has handed off line-level prose/watchlist cleanup and the manuscript structure is already approved.

## Scope

Stage 14 is for prose, rhythm, dialogue, action clarity, chapter hooks, and known watchlist cleanup. Do not perform macro rewrites, chapter reorders, new scene insertions, or structural expansion unless a true line-edit blocker exposes a continuity break.

## Workflow

1. Load `references/prose-tic-watchlist.md` and `references/house-style-modern-military-adventure.md`.
2. Run a whole-manuscript watchlist scan across `chapters/chapter-*.md` for carried terms from Stage 11–13.
3. Patch only chapter prose, not reviews/tracking files, when cleaning manuscript watchlist hits.
4. Prefer targeted wording improvements, but bulk replace is acceptable for a pure prose tic only after checking the construction is consistently safe in that chapter.
5. After edits, rerun:
   - whole-manuscript watchlist scan
   - `wc -w` for all chapters
   - act totals and full manuscript total
6. Update `progress.md`, `AGENTS.md`, and `rolling-summary.md` with changed chapter counts/totals.
7. Create `reviews/stage-14-line-edit.md` with Jordan primary; add Cross/Casey/Quinn when edits touch action clarity, continuity-sensitive language, or safety-watchlist terms.
8. Advance tracking to Stage 15 only after review file exists, missing reviewers are none, gate is PASS WITH RESERVATIONS, and scans are clean.

## Pitfalls

- Do not blindly replace all `did not` with `didn't` without reviewing grammar. Contraction cleanup can create artifacts such as `So didn't making...`; repair these into natural prose (`So did the refusal to...`).
- Avoid weakening plot-critical caveats while tightening sentences. Preserve boundaries such as no public attribution, no rescue/location/custody certainty, no command authority, civilian/advisory only, separate authority lanes, and hidden-institution opacity.
- Do not add operational specificity while trying to add texture. Use sensory, emotional, bureaucratic, and consequence-level texture only.
- Keep watchlist terms out of chapter prose where possible (`surveillance`, `exploit`, `weapon`, etc.) unless independently necessary and fiction-safe. Prefer ordinary-language alternatives like `watching`, `misuse`, or `turn into procedure`.
- If line edits change chapter word counts, update every affected word-count source immediately: `progress.md`, `AGENTS.md`, review verification snapshot, and final user status.

## Verification Snippet

```bash
python - <<'PY'
from pathlib import Path
terms=['Unit 985','SCADA','payload','exploit','hack','breach','weapon','tactical','surveillance','biometric','passport number','hostage handling','interrogation','captivity conditions','forensic','system access','substation','grid-control','did not','kind of','particular']
chapters=sorted(Path('chapters').glob('chapter-*.md'))
flags={}
for p in chapters:
    s=p.read_text()
    hits={t:s.count(t) for t in terms if s.count(t)}
    if hits: flags[p.name]=hits
counts=[len(p.read_text().split()) for p in chapters]
print('flags=', flags)
print('act_totals=', sum(counts[:12]), sum(counts[12:20]), sum(counts[20:29]), sum(counts[29:36]))
print('total=', sum(counts))
PY
```
