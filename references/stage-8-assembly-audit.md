# Stage 8 Assembly Audit — Scene Breakdown

Use after parallel act-level scene breakdowns are produced and before the Stage 8 review is presented.

## Why

Parallel act subagents often create useful scene detail but can leave cross-act inconsistencies or review-blocking placeholders. The most common failures are not prose quality; they are state locks and format drift.

## Required Assembly Steps

1. Assemble a single canonical `scene-breakdown.md` from act files.
   - Keep supporting act files (`act1-scenes.md`, `act2a-scenes.md`, `act3-scenes.md`) if useful.
   - Put locked decisions at the top of the assembled file.
   - Normalize status lines to `REVISED AFTER TEAM REVIEW` only after fixes are applied.

2. Run a required-field audit across every scene.
   - Every scene needs: Objective, Obstacle, Pressure, Turn/Reversal, Exit Hook, Continuity Impact, Research/Safety Note.
   - Action/consequence scenes also need: Starting Positions, Opposing Objectives, Geography, What Goes Wrong, Cost.
   - Do not assume action scenes with an `Action Elements` block already satisfy the standard fields; explicitly check for `Turn/Reversal`.

3. Search for review-blocking placeholders and deferred-decision language.
   - Flag: `Pending`, `TBD`, `author decision`, `Stage 15`, `Stage 16`, `provisional`, `author options`.
   - Some later-stage fact-check notes are valid, but Stage 8 story-state decisions must not be deferred if the Stage 8 brief required them to be locked.
   - If a fate/record handoff/institutional role is required by Stage 8, lock it in the scene plan and carry only terminology/fact-check polish forward.

4. Cross-act locks to verify manually.
   - Secondary fates: Price/Eleanor/Tomas or equivalent named pressure characters.
   - Evidence handoffs: exact chapter/scene where records are copied, handed off, or retained.
   - Knowledge state: who knows codename/threat/secret organisation; ensure opaque hints are not exposition.
   - Hesitant institution/channel: keep fictionalised/composite unless factually neutral and necessary.
   - Safety: no procedural cyber, route, hostage, mercenary, weapons, breaching, evasion, or grid-control detail.

## Useful Python Audit Snippet

Run from the project root after `scene-breakdown.md` exists:

```python
from pathlib import Path
import re
text = Path('scene-breakdown.md').read_text()
scenes = list(re.finditer(r'^(#{3,4})\s+Scene\s+([0-9]+\.[0-9]+)\s+—', text, flags=re.M))
required = ['Objective','Obstacle','Pressure','Turn/Reversal','Exit Hook','Continuity Impact','Research/Safety Note']
missing = []
for i, scene in enumerate(scenes):
    block = text[scene.end():scenes[i+1].start() if i+1 < len(scenes) else len(text)]
    miss = [f for f in required if not re.search(r'\*\*' + re.escape(f) + r':\*\*', block)]
    if miss:
        missing.append((scene.group(2), miss))
print('chapters', len(re.findall(r'^#{2,3}\s+Chapter\s+\d+\s+—', text, flags=re.M)))
print('scenes', len(scenes))
print('missing_required', missing)
for bad in ['Pending','TBD','author decision','Stage 15','Stage 16','provisional','author options']:
    print(bad, len(re.findall(re.escape(bad), text, flags=re.I)))
```

## Review File Must Mention

In the Stage 8 review, include a short section named `Parallel Assembly Issues Caught and Fixed` listing:
- Missing fields found by audit.
- Deferred locks converted into story decisions.
- Placeholder/status cleanup.
- Continuity fixes made before presentation.
