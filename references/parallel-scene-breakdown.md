# Parallel Scene Breakdown — Subagent Delegation Pattern

## When to Use

Stage 8 (Scene-by-Scene Breakdown) for novels with 20+ chapters. The scene breakdown is large — 80-100 scenes across three acts, 60-100KB of text. A single agent reading outlines and writing breakdowns sequentially risks context exhaustion and inconsistent detail depth. Parallel subagents reduce wall-clock time and keep each act breakdown at consistent detail.

## Pattern

```text
1. Read all chapter outlines (act1-outline.md, act2-outline.md, act3-outline.md)
2. Launch 3 delegate_task subagents, one per act
3. Each subagent receives: the outline file for its act + all shared context
4. Subagents write their act's scene breakdown in parallel
5. After all complete, read all three files for review
```

### Required Context Per Subagent

Each subagent needs:
- Its specific act's chapter outline file (path and content)
- The full character cast with key relationships (prevent invented characters)
- Carry-forward requirements from prior stages
- The scene format template: 7 standard fields (Objective, Obstacle, Pressure, Turn/Reversal, Exit Hook, Continuity Impact, Research Need) + 5 action fields (Starting Positions, Opposing Objectives, Geography, What Goes Wrong, Cost) for ACTION-tagged scenes
- House style notes: lean, plausible, fast, emotionally grounded
- Key locked decisions that affect the act (e.g., winter setting, specific named locations, character fates)
- Cross-act continuity anchors: named locations, key artifacts, character locations at act boundaries, timeline day numbering

### Critical: Cross-Act Continuity Anchors

Pass these explicitly to every subagent — they are the facts that MUST be consistent:
- Timeline: what day does the act start and end on?
- Artifacts crossing act boundaries: notebook, whiteboard, specific objects
- Character locations at act boundaries: who is where when the act begins?
- Named locations: use exact same name strings
- Shared characters: their fates, knowledge states, relationships

## Pitfall: Subagent-Introduced Continuity Errors

Subagents working on isolated acts CANNOT see each other's work. They will invent details that conflict with other acts. This is the dominant failure mode of parallel scene breakdown.

### Error Categories Observed (Real-World Examples)

1. **Invented characters/relationships** — Subagent references a character that doesn't exist in the locked cast, or invents a relationship (e.g., giving protagonists children who aren't present, referencing a non-existent family member). **Concrete example from Bikini Black Act 2 Ch 8:** subagent wrote Turner saying "Your daughter's safe in Warsaw" — the protagonists don't have children with them on holiday. The line should have referenced Rasa/Emilija, not Stuart/Kirsty's non-present child.

2. **Location drift** — A location established in one act is renamed or relocated in another. **Concrete example from Bikini Black Act 3:** subagent wrote "the observation Stuart made on the restaurant balcony" — the drone was observed from the apartment window in Žvėrynas (Act 1, Ch 1, Scene 3). The restaurant (Act 1, Ch 2) is an interior Old Town restaurant with no balcony. The scene breakdown subagent for Act 3 was unaware of the Act 1 location detail and invented a "restaurant balcony" that doesn't exist in the story.

3. **Acronym/term invention** — Subagent expands an acronym into a plausible-sounding but incorrect meaning. **Concrete example from Bikini Black Act 3:** subagent expanded VSD as "Victim Support Desk" and AOTD as "Allied Operational Threat Detection." Correct expansions: VSD = Valstybės saugumo departamentas (State Security Department — Lithuanian domestic intelligence). AOTD = Antrasis operatyvinių tarnybų departamentas (Second Operational Research Department — Lithuanian military intelligence). See `references/baltic-intel-services.md` for the correct reference.

4. **Physical state inconsistency** — Progressive physical trackers (fuel gauge, exhaustion level, cold exposure) become non-linear when different subagents handle different segments of the same journey (e.g., fuel gauge reading rising from quarter to one-third between scenes handled by different subagents)

5. **Knowledge over-attribution** — Subagent gives a character precise technical knowledge they shouldn't have (e.g., a GCHQ signals analyst precisely identifying military vehicle models by sight)

### Mitigation

1. **Pass explicit continuity anchors** to every subagent (see above)
2. **Run a mandatory pre-review scan** after all subagents complete and files are assembled — BEFORE writing the Stage 8 review. Use the following checklist:
   - **Character audit:** Grep each act for character names. Flag any name that doesn't appear in the locked character cast. Pay special attention to dialogue attribution — subagents may put words in a character's mouth that imply facts not in the locked decisions (e.g., Turner referencing "your daughter" when the protagonists' children aren't present).
   - **Location audit:** Check location references against the settings files. "restaurant balcony" vs "apartment window" — verify the location described matches where the event was established.
   - **Terminology audit:** For any acronym or specialist term used in multiple acts, verify the expansion is consistent and matches the research brief. Subagents may invent plausible-sounding but incorrect expansions (e.g., "Victim Support Desk" for VSD).
   - **Progressive tracker audit:** Trace every progressive physical tracker (fuel gauge, temperature, time-of-day, exhaustion markers, battery levels) across act boundaries. Look for non-linearities — a gauge reading that rises between scenes, a time that goes backward, a character who gets less tired.
   - **Knowledge audit:** Check that characters' stated knowledge matches their established expertise. A GCHQ signals analyst shouldn't precisely identify military vehicle models by sight; qualify as "consistent-with" rather than "confirmed."
3. **Run the full Stage 8 review** with all four required reviewers (Alex, Casey, Cross, Hayes). Casey's continuity lens catches what the pre-review scan missed.
4. **Accept that some errors will slip through** — the review step exists to catch them. Don't expect perfect subagent output.

## Review Integration

After parallel scene breakdown assembly:

1. Assemble the act files into a single Stage 8 deliverable (usually `scene-breakdown.md`) so later drafting has one canonical file. Keep the act files as support files if useful.
2. Run a mechanical field audit before persona review: count chapters/scenes and verify every scene has Objective, Obstacle, Pressure, Turn/Reversal, Exit Hook, Continuity Impact, and Research/Safety Note. For ACTION/consequence scenes, verify Starting Positions, Opposing Objectives, Geography, What Goes Wrong, and Cost where applicable.
3. Search the assembled deliverable for unresolved planning placeholders or cross-act drift terms: `Pending`, `TBD`, `author decision`, stale later-stage deferrals, invented family references, invented acronyms, and safety-risk words that may indicate procedural detail. Fix before review.
4. Run cross-act continuity audit (Casey lens: timeline, locations, artifacts, physical trackers, locked fates, and evidence handoffs).
5. Run full Stage 8 review with all four required reviewers (Alex, Casey, Cross, Hayes).
6. Fix all actionable issues in both the act files and the assembled file; if act files are patched, reassemble `scene-breakdown.md` before final verification.
7. Present to author.

The review file should include a section noting which issues were introduced by parallel assembly and caught during review — this builds institutional memory for future sessions. Typical fixes include replacing provisional secondary fates with locked fates, adding missing Turn/Reversal fields to action-tagged scenes, and changing “pending” handoff notes into concrete cross-file carry-forward notes once the later act file contains the beat.
