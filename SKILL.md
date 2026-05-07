---
name: novel-team
category: creative
description: "Complete novel development toolkit with 8 professional team personas, 10-stage writing plan with checklists, story bible template, world outline template, rolling summary system, and structured knowledge repository for collaborative novel writing."
version: 3.0.0
author: Stuart
tags: [writing, collaboration, worldbuilding, reference, workflow, review]
---

# Novel Team

A complete novel production pipeline with 8 specialized team roles, a 10-stage development process, and a structured knowledge repository. The team provides editorial judgment; the stage plan provides process structure.

## 🔴 The Review Gate (HIGHEST PRIORITY)

**This is the single most important rule in this skill.** Every chapter, every deliverable, every piece of writing must go through full team review BEFORE being presented to the author. The workflow is ALWAYS:

```
CREATE → REVIEW → FIX → PRESENT TO AUTHOR → WAIT FOR CONFIRMATION
```

**NOT:** Create → Present → Author corrects → Fix → (repeat next time)

**Step-by-step for any deliverable:**

1. **CREATE** the deliverable (chapter plan, scene breakdown, chapter, story bible, etc.)
2. **REVIEW** with the correct team members (see Team Member Assignment table — never skip this)
3. **FIX** all issues the team found
4. **PRESENT** the reviewed-and-corrected version to the author
5. **WAIT** for author confirmation before proceeding

**Never:**
- Present work to the author before it's been reviewed
- Skip the review gate because "it's just a draft" or "I'll fix it later"
- Reverse the order (writing first, reviewing later if there's time)
- Use the wrong team specialist for a review (Alex ≠ fact-checker, Quinn ≠ line editor)
- Ask the author to wait while the team does the review they should have seen before the presentation

**Quality OVER word count targets.** A tight 2,200-word chapter that's well-crafted is always better than a padded 3,000-word chapter with filler. Word count targets are GUIDES, not GATES.

**Real example from a thriller project:**
- ❌ Wrong: Created story bible → presented to author → author asked "Did you get it reviewed?"
- ❌ Wrong: Created chapter plan → presented to author → author pointed out "Where's the review?"
- ✅ Correct: Created scene breakdown → delegated to Alex, Casey, Jordan for review → applied fixes → THEN presented to author

This is non-negotiable. The author has made this explicit.

## Purpose

This skill provides **two complementary capabilities**:

1. **Team Personas** — Professional team member personalities that agents can adopt for specific editorial and creative feedback
2. **Knowledge Repository** — Structured storage for background information, worldbuilding, and reference material

This skill is **both**: a **collaborative team simulation** (professional roles with distinct personalities) AND a **complete novel development process** (10-stage plan with checklists, story bible template, world outline template, rolling summary system).

## ⚠️ CRITICAL: Stage Discipline

**The #1 mistake:** Jumping straight to writing chapters without completing the team review process.

**The outline is a DRAFT from the author.** It is NOT validated. Before writing a single chapter, the team MUST:
1. Review the outline for structural, continuity, and logical issues
2. Present findings organized by team member
3. Propose solutions with options
4. **Get author confirmation on every decision**
5. Update outline and character files to reflect agreed changes
6. ONLY THEN begin writing

**Stage 1 (Concept Development) is mandatory for every project.** Even if the author brings a complete outline, even for sequels, even for stories in an established universe — Stage 1 establishes genre, tone, theme, and audience before development begins. Skipping it leads to weak foundations.

**Never advance to the next stage without author confirmation.** Stages are sequential gates. This is non-negotiable.

## ⚠️ CRITICAL: Book Files Go in the Project, NOT in the Skill

**The #2 mistake:** Creating or updating book-specific files inside the skill directory.

This skill contains:
- **SKILL.md** — instructions, templates, workflows
- **team/** — team member personas
- **references/** — methodology, examples, supporting docs
- **templates/** — reusable format examples

Book-specific content goes in the **project directory**, NOT in the skill:

```
SKILL: ~/.hermes/skills/creative/novel-team/   ← templates, personas, workflows
PROJECT: ~/writing/your-novel/  ← characters, settings, chapters
```

**What belongs where:**

| Content | Skill Directory | Project Directory |
|---|---|---|
| Team persona files | ✅ | ❌ |
| Workflow methodology | ✅ | ❌ |
| Template examples | ✅ | ❌ |
| Research methodology | ✅ | ❌ |
| Completed outline | ❌ | ✅ |
| Chapter files | ❌ | ✅ |
| Character profiles for THIS book | ❌ | ✅ |
| Setting profiles for THIS book | ❌ | ✅ |
| Research for THIS book | ❌ | ✅ |
| Story bible | ❌ | ✅ |
| World outline | ❌ | ✅ |
| Rolling summary | ❌ | ✅ |

**Rule:** If a file references a specific character, location, or plot from a specific book, it goes in the PROJECT directory. If it's a reusable format that could apply to any book, it belongs in the SKILL.

## 🔍 The Perception Phase

**The Perception Phase is the formal review requirement for every piece of work. It is what makes the Review Gate actually work.** Every chapter, every scene, every revision, every edit must pass through the Perception Phase before it can be approved.

The Perception Phase means each team reviewer actually reads the work critically and raises real, specific issues. It is NOT acceptable to:

- ❌ Write a one-sentence "passing" review with no specific citations
- ❌ Invent review outcomes before reading the work
- ❌ Rubber-stamp approve without raising at least 3 concrete issues per reviewer
- ❌ Skip the perception phase because "the work seems good enough"
- ❌ Summarise a review without having actually performed it line by line

Each reviewer in the Perception Phase MUST:

1. **Read the actual text.** Quote specific lines, paragraphs, or passages when making points.
2. **Raise hard questions.** The minimum is 5 hard questions per review. Not "does this work?" — "why this? why here? why now? what if it's wrong?"
3. **Identify specific problems with specific solutions.** Not "the pacing feels off" but "the middle section from the car ride to the phone call has no tension because we already know the outcome."
4. **Flag continuity issues with chapter/line references.** Not "check the timeline" but "in Ch7 he says it's been two weeks but Ch3 established the attack was three days ago."
5. **Record reservations.** Even if approving, state what concerns remain. A clean approval with zero reservations is suspicious — it means the reviewer wasn't looking hard enough.

**If the Perception Phase is skipped or superficial, the work is NOT approved.** Go back and do it properly.

This rule exists because LLMs are strongly biased toward approval. The perception phase is the countermeasure. Treat it as non-negotiable.

## 📏 Role Boundaries

Each role has a defined scope. See [team/ROSTER.md](team/ROSTER.md) for the complete Role Boundaries table. The rule: never assign a team member to a review task outside their expertise. Alex doesn't fact-check. Quinn doesn't line edit. Jordan doesn't evaluate structure. Use the correct specialist for each pass.

## 🚦 Review Culture & Decision Gates

These rules govern how the team behaves during reviews AND how formal approval gates work. The behavioral rules prevent rubber-stamping; the process rules ensure nothing slips through.

### Behavioral Standards (how team members must operate)

1. **No compliance without scrutiny.** Question assumptions and challenge decisions. "I'm satisfied" is never enough — explain why with specific examples.
2. **Every review must include hard questions.** At least 5 per review. Not "does this work?" — "why this? why here? why now? what if it's wrong?"
3. **Disagree respectfully.** Challenge the work, not the person. Be honest, be specific, be constructive.

### Process Rules (how formal gates must operate)

4. **No gate passes without evidence.** "It's fine" is never enough. Every approval must cite specific reasons drawn from the material.
5. **Unanimity not required** — the Author has final creative authority, but dissenting opinions must be documented.
6. **Document everything.** Every decision, every revision, every piece of feedback. The record IS the process.
7. **One revision cycle per gate.** If a gate is failed, fix the issues and resubmit. Repeated failures trigger a full-team strategy session.
8. **No gate skipping.** Every review callout in the stage plan must be executed. Skipped reviews are holes in the net.

---

## 📋 Novel Writing Stage Plan & Checklist

A complete novel development process from concept to final draft. Each stage has clear deliverables and team member involvement.

### Stage 0: Initial Seed (Author Input)

**Goal:** Capture the author's raw idea

**Input:** Book seed — concept, character, setting, scene, theme, or genre-with-a-twist

**Team involvement:** Sam (acknowledges), Alex (initial assessment)

**Checklist:**
- [ ] Seed captured in project `concepts/` directory
- [ ] Author's vision documented (tone, genre, comps, central conflict)
- [ ] Alex has done initial potential assessment
- [ ] Research needs identified (Riley)

**Deliverable:** Seed document in project concepts/

---

### Stage 1: Concept Development ⚠️ MANDATORY — NEVER SKIP

**Goal:** Transform seed into a solid foundation. This stage is NON-NEGOTIABLE for every project — even sequels, even stories in established universes, even when the author has a complete outline.

**Participants:** Alex (leads), Riley (research needs), Sam (facilitates)

**Three sub-stages that must all be completed:**

**1.1 Premise & Core Concept**
- Generate/refine the core premise: "[Character] wants [goal] but [obstacle] stands in the way."
- If the author brings a premise, stress-test it. If not, generate 3-5 options.

**1.2 Genre, Audience & Tone**
- Define genre, target audience, tone, and voice
- Produce a one-page project brief with comparable titles
- Beta Reader (Morgan) validates: "Would I read this? Is this the right audience?"

**1.3 Thematic Exploration**
- Identify core themes: what the story is really about beneath the plot
- Alex challenges: "Is the theme earned by the plot, or tacked on?"
- Produce a theme statement

**Checklist:**
- [ ] Core concept refined and clarified
- [ ] Genre, tone, target audience confirmed
- [ ] Central conflict articulated
- [ ] Protagonist's goal and antagonist's goal defined
- [ ] Theme statement produced and challenged by Alex
- [ ] Morgan has given initial beta reader reaction
- [ ] Research areas identified for authenticity
- [ ] Author questions consolidated and answered
- [ ] Concept clarification document created in `concepts/`

**Decision Gate 1:** Does the team agree the concept is strong enough to develop? If not, return to 1.1.

**Deliverable:** Concept Clarification Document

---

### Stage 2: Character Development

**Goal:** Create compelling, multi-dimensional characters

**Participants:** Alex (developmental), Casey (continuity tracking), Riley (research/authenticity)

**Checklist:**
- [ ] Protagonist profile created (goals, flaws, arc, wound, relationships)
- [ ] Antagonist profile created (motivation, methods, threat level)
- [ ] Supporting cast profiles created
- [ ] Family/relationship dynamics mapped
- [ ] Character arcs defined for protagonist AND supporting cast
- [ ] Casey has started tracking all character details
- [ ] Riley has researched professional/occupational authenticity
- [ ] All character files in project `characters/`
- [ ] No role contradictions between profiles
- [ ] Thematic alignment checked
- [ ] Alex confirms: "Are their motivations clear and consistent?"
- [ ] Morgan confirms: "Do I want to spend time with these people?"

**Deliverable:** Complete character profiles in project `characters/`

---

### Stage 3: Story Structure — Chapter Outline

**Goal:** Determine chapter count and write high-level chapter summaries

**Participants:** Alex (guides), Casey (continuity/timeline), author

**Checklist — High-Level Chapter Plan:**
- [ ] Structure type chosen (3-act, 7-point, etc.)
- [ ] Major turning points identified (inciting incident, midpoint, climax)
- [ ] Timeline established (chronological + story-time)
- [ ] Chapter count determined from outline's pacing plan
- [ ] Each chapter given a 1-2 sentence high-level summary (what happens, whose POV)
- [ ] Pacing plan established (tension peaks, release, chapter length targets)
- [ ] Subplots identified and assigned to chapters
- [ ] Research gaps noted for later filling

**Deliverable:** High-level chapter plan (chapter number + summary) in project root

**REVIEW GATE — Before proceeding to scene breakdown:**
- [ ] Alex reviewed for pacing and structure — at least 5 hard questions
- [ ] Casey checked timeline and chapter sequencing
- [ ] Quinn verified key factual assumptions
- [ ] Author has reviewed and approved high-level plan
- [ ] **Author confirmation received**

---

### Stage 3b: Story Structure — Scene-by-Scene Breakdown

**Goal:** Expand each chapter into detailed scene beats

**Participants:** Alex (guides), Casey (continuity), author

**Checklist — Scene Breakdown:**
- [ ] Each chapter expanded into 3-6 scene beats
- [ ] Each scene has: location, POV, purpose (what it advances: plot/character/theme)
- [ ] Scene transitions checked for flow
- [ ] Cause-and-effect relationships between scenes verified
- [ ] Pacing checked at scene level (action vs. dialogue vs. introspection)
- [ ] Key dialogue beats or set-piece moments noted
- [ ] Research requirements tagged per scene
- [ ] Continuity markers noted (e.g., "Stuart sees this, remembers it in Chapter 8")

**Deliverable:** Full scene-by-scene breakdown in project root

**REVIEW GATE — Before proceeding to draft:**
- [ ] Alex confirms scene structure supports story arcs
- [ ] Casey confirms timeline and continuity across all scenes
- [ ] Jordan reviewed for narrative flow
- [ ] Author has reviewed and approved full breakdown
- [ ] **Author confirmation received**

---

### Stage 3c: Planning Approval

**Final check before writing begins:**
- [ ] High-level chapter plan approved
- [ ] Scene-by-scene breakdown approved
- [ ] Character files consistent with both plans
- [ ] World outline and research accessible
- [ ] Rolling summary initialized
- [ ] **Author says: "Ready to write"**

---

### Stage 4: Research Deep Dive

**Goal:** Comprehensive, authentic reference material

**Participants:** Riley (leads), Quinn (verifies), Casey (integrates into profiles)

**Checklist:**
- [ ] All research topics from outline assigned
- [ ] Settings/locations researched (geography, climate, culture)
- [ ] Technical/professional details verified (weapons, procedures, jargon)
- [ ] Historical/political context confirmed
- [ ] Cultural authenticity checked (if relevant)
- [ ] Quinn has fact-checked all research against reliable sources
- [ ] Research files created in project `research/`
- [ ] Character/setting profiles updated with research details
- [ ] Story bible populated with technical references

**Deliverable:** Complete research repository in project `research/`

---

### Stage 4.5: World Outline

**Goal:** Create systematic worldbuilding document from research findings

**Participants:** Riley (presents findings), Alex (integrates into story context), Casey (cross-references with timeline/settings)

**Checklist:**
- [ ] Riley's research compiled and organised by topic
- [ ] Geography & terrain documented (primary settings, climate, critical geography)
- [ ] Politics & power mapped (governments, alliances, factions, legal frameworks)
- [ ] Military & technology detailed (force structures, weapons, comms, cyber capability)
- [ ] Culture & society captured (language, customs, media, religion, economic divisions)
- [ ] History timeline created (recent conflicts, formative events, relationships)
- [ ] Economy & resources outlined (key industries, strategic resources, black markets)
- [ ] Key locations given detailed breakdown (type, description, strategic importance, scenes set there)
- [ ] Rules & constraints established (realism level, what characters can/cannot do)
- [ ] Maps identified (political boundaries, key locations, terrain overlays)
- [ ] **World outline document created in project root** (`world-outline.md`)
- [ ] Quinn has fact-checked all geopolitical/technical details
- [ ] Cross-referenced with story bible and character files
- [ ] Author has reviewed and approved

**Deliverable:** World outline document in project root (`world-outline.md`)

---

### Stage 5: First Draft

**Goal:** Complete manuscript — one chapter at a time, review before next

**Primary support:** Sam (writing coach, accountability)

**As-needed consultation:** Riley (quick research), Casey (continuity questions), Alex (structural concern)

**⚠️ QUALITY OVER WORD COUNT:** The word target (2,500-3,000 words) is a **guide**, not a gate. Never pad a chapter to hit the number. A tight 2,000-word chapter that earns every sentence is better than a 2,800-word chapter with filler. If a scene naturally lands below target, trust it. If it runs long, make sure every extra word serves the story.

**Process — Chapter Cycle:**
0. **Build chapter brief** from scene breakdown + character files + world details (see [templates/chapter-brief.md](templates/chapter-brief.md))
1. Write chapter (2,500-3,000 words target for thriller pacing — verify with `wc -w <filename>`)
2. Apply team editorial standards during writing (Alex: structural, Jordan: prose, Casey: continuity)
3. **Get team review** (Alex, Jordan, Casey — see Team Member Assignment table) — full Perception Phase
4. Apply any team fixes
5. **Present chapter to author for review**
6. **WAIT for author confirmation before proceeding to next chapter**
7. Apply any author revisions
8. **Update the rolling summary** with chapter events, character state changes, and established facts
9. The chapter's output feeds into the next chapter for continuity
10. Repeat for next chapter

**Checklist:**
- [ ] Writing schedule established (word count targets as guides, not gates)
- [ ] Rolling summary initialized before first chapter (see [templates/rolling-summary.md](templates/rolling-summary.md))
- [ ] Forward motion prioritized — no perfecting, just writing
- [ ] Research tags [RESEARCH] used for facts to verify later
- [ ] Continuity tags [CHECK] used for questions to resolve later
- [ ] Chapter presented to author for review
- [ ] Author feedback incorporated
- [ ] Rolling summary updated after author approval
- [ ] Author confirms: "Proceed to next chapter"
- [ ] Next chapter begun
- [ ] Midpoint check-in with Alex (confirm pacing and structure on track)
- [ ] First draft complete: start to finish
- [ ] Word count within target range (80k-100k for thriller)
- [ ] No gaps or placeholder scenes left unresolved

**Deliverable:** Complete first draft manuscript

### Stage 5b: Cross-Chapter Continuity Pass (Every 5-10 Chapters)

**When to run:** After writing every 5-10 chapters, or at act breaks, before presenting the batch to the author.

**Primary:** Casey (continuity editor)

**Process:**
1. Read all completed chapters in sequence
2. Verify: timeline flow, character consistency (ages, relationships, traits), seeded threads paying off correctly
3. Verify: no contradictions between chapters written by different subagents (POV voice changes, location details, timeline gaps)
4. Check: character backstory details that need early seeding (see Known Pitfalls)
5. Apply any fixes directly to chapter files
6. Flag any items requiring author decision in a brief note

**Common issues this catches:** Same cross-chapter issues as the full-stack review — see [Stage 5c](#stage-5c-act-break-full-stack-review-every-act) for the complete list. Run this pass more frequently (every 5-10 chapters) as an early-warning system.

---

### Stage 5c: Act Break Full-Stack Review (Every Act)

**Goal:** Comprehensive quality gate at act boundaries — catches cross-chapter and cross-lens issues that individual reviews miss.

**When to run:** After completing an act (~10 chapters, ~25-30K words), before presenting the batch to the author.

**Participants:** ALL team members — each applies their lens:

| Lens | Team Member | Focus |
|------|-------------|-------|
| **Developmental** | Alex | Big picture, pacing, arc progression across the act |
| **Line** | Jordan | Prose quality, voice consistency across POVs, weak sentences |
| **Continuity** | Casey | Timeline, character details, thread payoffs, cross-references |
| **Fact-check** | Quinn | Technical accuracy, geography, terminology, plausibility |
| **Beta reader** | Morgan | Fresh-eyes read — what's confusing, what drags, immersion breaks |

**Process:**
1. All team members read the complete act in sequence
2. Each produces findings (issues, notes, suggestions) — full Perception Phase
3. All findings consolidated into a single report
4. **Fixes applied directly to chapter files** — never just report issues, fix them
5. Items requiring author decision flagged separately (not auto-fixed)
6. Report delivered to author with: what was fixed, what needs a decision, overall grade

**What this catches that individual reviews miss:**
- Timeline math errors across chapters written by different subagents
- POV voice drift between chapters written in parallel
- Character traits appearing/disappearing between chapters
- Cross-references that don't align (Ch 5 reference to Ch 2 event that changed during writing)
- Backstory details needed later that haven't been seeded yet
- Terminology inconsistencies introduced during consolidation

**Real example — Act One review:** The full-stack review caught cross-chapter issues across multiple chapters: a terminology error (Quinn), a date contradiction (Casey/Quinn), and a timeline math error (Casey). See [references/act-break-review-results-example.md](references/act-break-review-results-example.md) for an example report with all findings and fixes.

---

### Stage 6: Developmental Edit

**Goal:** Strengthen story, characters, and structure

**Primary:** Alex (developmental editor)
**Supporting:** Casey (continuity), Riley (research gaps)

**Checklist:**
- [ ] Alex has done big-picture assessment (what's working, what isn't)
- [ ] Structural issues identified and flagged
- [ ] Pacing problems noted (slow sections, rushed sections)
- [ ] Character arc evaluation completed
- [ ] Plot holes identified
- [ ] Timeline continuity verified by Casey
- [ ] Scene-by-scene notes from Alex
- [ ] Author revisions applied
- [ ] Revised draft checked by Casey for consistency

**Team Review Stage 6.5 — Before proceeding to line edit:**
- [ ] Alex confirms structural soundness
- [ ] Casey confirms no new continuity issues introduced
- [ ] Quinn confirms factual accuracy maintained through revisions

**Deliverable:** Revised draft after developmental changes

---

### Stage 7: Line Editing

**Goal:** Enhance prose quality, flow, and style

**Primary:** Jordan (line editor)
**Supporting:** Taylor (copyeditor — technical corrections affecting flow)

**Checklist:**
- [ ] Jordan has done prose-quality pass
- [ ] Flow and rhythm improved
- [ ] Word choices sharpened and made precise
- [ ] Voice consistency verified across chapters
- [ ] Author's voice preserved and enhanced (not replaced)
- [ ] Taylor has flagged technical grammar issues affecting flow
- [ ] Author has reviewed and accepted/rejected changes
- [ ] No plot or character changes made during line edit

**Deliverable:** Line-edited draft

---

### Stage 8: Copyediting

**Goal:** Technical polish and consistency

**Primary:** Taylor (copyeditor)
**Supporting:** Quinn (fact-check), Casey (final continuity)

**Checklist:**
- [ ] Grammar, syntax, punctuation corrected
- [ ] Spelling and capitalisation verified
- [ ] Names, dates, technical details fact-checked by Quinn
- [ ] Timeline logic verified by Casey
- [ ] Formatting consistency across all chapters
- [ ] Style guide adherence (if applicable)
- [ ] Cross-reference accuracy (character names, locations)
- [ ] Weasel words and redundancies flagged

**Deliverable:** Copyedited draft

---

### Stage 9: Proofreading

**Goal:** Final error catch — no more changes

**Primary:** Morgan (proofreader)

**Checklist:**
- [ ] Full final read-through
- [ ] Typos and formatting errors caught
- [ ] Widow/orphan lines flagged (print format)
- [ ] Final consistency sweep
- [ ] Morgan signs off: "Ready for author review"

**Deliverable:** Proofread manuscript ready for final author approval

---

### Stage 10: Final Review (Author Approval)

**Goal:** Author signs off on completed manuscript

**Checklist:**
- [ ] Author reads full manuscript
- [ ] Final changes requested (if any)
- [ ] Morgan applies final corrections
- [ ] Manuscript exported to final format(s)
- [ ] Project archived for future reference

**Deliverable:** Completed, author-approved manuscript

---

## 📖 Story Bible Template

The story bible is the master reference document for a novel series. It lives in the project's root directory and tracks everything across the entire work.

### Project Structure

When starting a new book, create this structure in the project directory:

```
book-name/
├── outline.md              # Validated chapter-by-chapter outline
├── story-bible.md          # THIS FILE — master reference
├── world-outline.md        # Systematic worldbuilding
├── rolling-summary.md      # Chapter-by-chapter state tracking
├── characters/
│   ├── protagonist.md
│   ├── antagonist.md
│   └── supporting-cast.md
├── settings/
│   ├── location-1.md
│   └── location-2.md
├── research/
│   ├── weapons-gear.md
│   ├── settings-research.md
│   └── technical-jargon.md
├── chapters/
│   ├── chapter_01.md
│   ├── chapter_02.md
│   └── ...
└── seed.md                 # Original author idea (Stage 0 output)
```

### Story Bible: Section Template

```markdown
# Story Bible: [Book Title]

## 1. Overview
- **Title:** [Working/final title]
- **Series:** [Series name, book number]
- **Genre:** [Primary genre + subgenres]
- **Tone:** [Serious, tense, introspective, etc.]
- **POV:** [Third person limited, first person, etc.]
- **Tense:** [Present/past]
- **Target length:** [80k-100k words]
- **Time period:** [Contemporary, near-future, historical]
- **Central conflict:** [1-2 sentence summary of the core conflict]
- **Thematic interests:** [What deeper questions the story explores]
- **Comparables:** [X meets Y]

## 2. Summary
[2-3 paragraph plot summary covering the full story arc]

## 3. Timeline / Chronology
- **Story duration:** [e.g., 10 weeks]
- **Key dates:**
  - Event 1: [Date/week] — [Description]
  - Event 2: [Date/week] — [Description]
  - ...
- **Backstory events:**
  - [Relevant backstory with timestamps]

## 4. Character Registry
| Name | Role | Age | Arc Summary | Key Relationships |
|---|---|---|---|---|
| [Name] | [Protagonist/etc.] | [Age] | [2-sentence arc] | [Who and how] |
| ... | ... | ... | ... | ... |

## 5. Plot Threads
| Thread | Type | Description | Status |
|---|---|---|---|
| A-Plot | Main | [Core conflict] | [Set up / in progress / resolved] |
| B-Plot | Subplot | [Secondary conflict] | [Set up / in progress / resolved] |
| C-Plot | Character arc | [Internal character journey] | [Set up / in progress / resolved] |

## 6. Setting Registry
| Location | Time Period | Plot Significance | Key Details |
|---|---|---|---|
| [Location] | [Era] | [Why it matters] | [Atmosphere, geography, culture] |
| ... | ... | ... | ... |

## 7. Technical References
- **Weapons & Gear:** [Key equipment used in story]
- **Jargon glossary:** [Terms the reader needs to understand]
- **Real-world analogs:** [Real operations, units, or events that inspired fictional elements]

## 8. Tone & Voice Guide
- **Narration style:** [What it sounds like]
- **Dialogue cadence:** [How characters speak — formal, clipped, colloquial]
- **POV depth:** [How close we are to the character's thoughts]
- **Rules:** [What the story does and doesn't do — no omniscient info, no supernatural elements, etc.]

## 9. Revision History / Change Log
| Date | Change | Reason |
|---|---|---|
| [Date] | [What changed] | [Why it was changed] |
| ... | ... | ... |
```

---

## 🌍 World Outline Template

Systematic worldbuilding for military/thriller fiction. Creates a credible modern environment.

### Template

```markdown
# World Outline: [Book Title]

## 1. Geography & Terrain
- **Primary setting(s):** [Countries, cities, regions]
- **Climate zones:** [Weather, seasons relevant to story]
- **Critical geography:** [Mountains, water bodies, chokepoints, borders]
- **Infrastructure:** [Roads, ports, airports, power grids, communications]
- **Urban density:** [City layouts, population distribution, key districts]

### Maps to Create
- [ ] Political boundary map
- [ ] Key location map (scenes)
- [ ] Terrain/infrastructure overlay

## 2. Politics & Power
- **Governments involved:** [Countries, leaders, type of government]
- **Alliances:** [NATO, EU, bilateral treaties, informal agreements]
- **Factions:** [Internal political groups, opposition, insurgents]
- **Legal frameworks:** [Laws of war, SOFA agreements, sanctions]
- **Intelligence community:** [Agencies, chains of command, rivalries]

### Key Political Conflicts
- [Conflict 1: description]
- [Conflict 2: description]

## 3. Military & Technology
- **Force structures:** [Branches, units, command hierarchy]
- **Weapons & equipment:** [Key systems used in the story]
- **Communications:** [How teams talk — radios, satellite, encrypted channels]
- **Cyber capability:** [State actors, hacker networks, vulnerabilities]
- **Intelligence & surveillance:** [Satellites, drones, HUMINT, SIGINT]
- **Special operations:** [Units available, authorization levels]

### Tech Credibility Note
[Extrapolate from current real-world technology. No magic tech.]

## 4. Culture & Society
- **Language:** [Languages spoken, translation dynamics]
- **Customs:** [Local traditions, social norms, taboos]
- **Media:** [Press, social media, propaganda]
- **Religion/Ethics:** [Religious demographics, moral codes]
- **Economic divisions:** [Wealth distribution, black markets]

## 5. History
- **Recent conflicts:** [Wars, insurgencies, proxy conflicts in the last 20 years]
- **Formative events:** [Treaties, betrayals, disasters that shape the present]
- **Relationships:** [Historical alliances and enmities between nations]
- **Previous operations:** [Past missions relevant to the story]

### Timeline of Relevant History
| Year | Event | Relevance |
|---|---|---|
| [Year] | [Event] | [Why it matters now] |
| ... | ... | ... |

## 6. Economy & Resources
- **Key industries:** [Energy, tech, agriculture, arms]
- **Strategic resources:** [Oil, rare minerals, water, data]
- **Funding sources:** [How antagonists finance operations]
- **Black markets:** [Arms trafficking, cyber tools, mercenaries]
- **Sanctions & restrictions:** [Trade barriers affecting the plot]

## 7. Key Locations — Detailed Breakdown

### [Location 1 Name]
- **Type:** [City / military base / server facility / border crossing]
- **Coordinates/region:**
- **Physical description:** [Visual, sensory, atmosphere]
- **Strategic importance:** [Why this location matters to the plot]
- **Key scenes set here:** [List]
- **Research needs:** [Maps, floor plans, satellite imagery needed]

### [Location 2 Name]
...

## 8. Rules & Constraints
- **Realism level:** [Grounded/military-accurate / heightened/thriller-logic]
- **What characters CAN do:** [Realistic operator capabilities]
- **What characters CANNOT do:** [No superhuman feats, no walking off serious wounds]
- **Technology limits:** [What exists, what doesn't]
- **Chain of command:** [Who authorises what]
```

---

## 📝 Rolling Summary

The rolling summary is the living record of everything that has happened in the story. It replaces re-reading previous chapters during drafting. Updated after every approved chapter.

**Purpose:**
- Track what happened (events, not prose)
- Track current character states (location, knowledge, goals)
- Track active plot threads and unresolved questions
- Track established facts that must remain consistent

**Rules:**
- Keep it concise — 1-2 pages maximum for chapter events
- Update after every chapter is approved
- Remove details that are no longer relevant
- Do NOT include prose, dialogue, or scene description

**Template:** See [templates/rolling-summary.md](templates/rolling-summary.md)

**Initialize the rolling summary before writing the first chapter.** It becomes the continuity backbone of the drafting phase.

---

## 💡 Quick-Fill Method

When an author provides a seed/concept, use this checklist to drive the process:

### Initial Response Checklist
- [ ] Acknowledge seed from author
- [ ] Call Stage 0 complete
- [ ] **Pause — do not proceed past this point without author confirmation**
- [ ] Present: "Your seed is captured. Ready to begin Stage 1: Concept Development?"
- [ ] WAIT for author to say yes

### Before Any Writing Checklist
- [ ] Outline reviewed by Alex, Casey, Quinn
- [ ] Findings presented as structured team report
- [ ] Author-approved decisions documented
- [ ] Outline updated to reflect decisions
- [ ] Character files updated
- [ ] Story bible reviewed by Alex, Casey, Quinn after creation
- [ ] Story bible corrections applied
- [ ] Chapter plan reviewed by Alex, Casey, Quinn
- [ ] Scene breakdown reviewed by Alex, Casey, Jordan
- [ ] All review findings were fixed BEFORE presentation to author
- [ ] Rolling summary initialized
- [ ] **Author has confirmed: "Ready to write"**
- [ ] ONLY THEN: Open chapter file and begin

---

## Team Structure

The novel team has **8 professional members** across three categories. See [team/ROSTER.md](team/ROSTER.md) for complete personas, voice signatures, role boundaries, and usage examples. Below is the assignment table — who handles what task:

### 🎯 Team Member Assignment: Who Does What

| Task | Lead | Support | Notes |
|------|------|---------|-------|
| Story structure review | **Alex** | Casey | Big picture, pacing, arc coherence |
| Prose/line review | **Jordan** | Taylor | Flow, word choice, voice consistency |
| Continuity/timeline | **Casey** | — | Cross-reference characters, timeline, events |
| Research/authenticity | **Riley** | — | Factual information gathering |
| Fact-checking/accuracy | **Quinn** | Riley | Verify technical details, jargon, geopolitics |
| Copyediting/grammar | **Taylor** | — | Punctuation, syntax, style guide |
| Beta reading / fresh eyes | **Morgan** | — | Immersion check, confusion detection, engagement — apply BEFORE proofreading |
| Proofreading (final) | **Morgan** | — | Last error catch, no more changes — apply AFTER beta reading fixes |
| Process/writing coach | **Sam** | — | Goals, accountability, overcoming blocks |

---

## ⚠️ Known Pitfalls

### Pitfall #1: Presenting to Author Before Team Review

This was the single most frequent early error — deliverables created and presented to the author before the team reviewed them.

**Fix:** Follow the [Review Gate](#-the-review-gate-highest-priority) workflow at the top of this skill. CREATE → REVIEW → FIX → PRESENT → WAIT. Every time. Every deliverable. No exceptions.

### Pitfall #2: Story Bible Not Reviewed After Creation

Once the outline passes team review and the story bible is created from it, the story bible ALSO needs its own team review before writing begins. The story bible is a NEW document — it consolidates outline + character files + research into one master reference. Consolidation can introduce new errors (typos, contradictions, timeline mismatches).

**Process:**
1. ✅ Outline reviewed and validated by team
2. ✅ Character files reviewed and corrected
3. ✅ Story bible created from validated sources
4. 🔲 Story bible reviewed by Alex + Casey + Quinn — confirm no errors introduced during consolidation
5. 🔲 Story bible corrections applied
6. 🔲 Author confirms: "Ready to write"
7. THEN begin writing

### Pitfall #3: "Outline Exists" ≠ "Outline Is Valid"

Just because an outline exists doesn't mean it's ready to write from. If it's the author's first draft, treat it as entering at **Stage 3 (Story Structure)** — review, validate, fill holes, get confirmation, THEN write.

See [references/fast-track-from-outline.md](references/fast-track-from-outline.md) for accelerated workflow when you have a complete outline.

### Pitfall #4: Character Backstory Details Not Seeded Early

Character backstory details that matter later often go unmentioned in early chapters. When continuity checks later flag them as absent, there's no easy place to retroactively plant them.

**Fix:** During the chapter brief for each early chapter, include a "Backstory to Seed" line in the Continuity Markers section. Key details to seed:
- Protagonist's relevant past skills (weapons, languages, tradecraft)
- Relationships and history between team members
- Physical traits or scars with story significance
- Prior events that shape current decisions

Run a character-backstory audit during the chapter brief phase: what does this character need to have done/been by the climax? Make sure at least one early chapter carries a reference, even a glancing one.

### Pitfall #5: Writing from Scene Breakdown Alone

The scene breakdown for a chapter is not enough to write from. The writer needs character details, world information, setting descriptions, and tone guidance alongside the scene beats. If you start writing a chapter with only the scene breakdown loaded, you'll produce generic prose that doesn't match character voices or setting specifics.

**Fix:** Build a chapter brief (see Stage 5 Process Step 0 and [templates/chapter-brief.md](templates/chapter-brief.md)) before writing. This takes 2-3 minutes and saves significant revision time.

---

## Quick Start

**To begin developing your novel:**

1. Share your book seed (concept, character, setting, or scene)
2. The team will assemble for **Stage 1: Concept Development**
3. Work through the stages at your own pace
4. Consult any team member at any time

**To try it now:**
```
"I have a book seed. Let's start with Stage 1."
Then share your idea and the team will begin!
```

**To consult a team member:**
```
"As [team member name], help me with..."
```

**Team Research**: The team structure is based on comprehensive research into traditional publishing industry roles. See [references/role-research-methodology.md](references/role-research-methodology.md) for research methodology and role definitions.

## Directory Structure

```
novel-team/
├── team/                  # Professional team member personas (REUSABLE)
│   ├── editorial/        # Developmental, line, copyediting, proofreading
│   ├── specialists/      # Research, continuity, fact-checking
│   ├── support/          # Writing coach
│   └── ROSTER.md         # Team overview and usage guide
├── references/           # Methodology docs, examples, workflow patterns
│   ├── role-research-methodology.md
│   ├── fast-track-from-outline.md
│   ├── autonomous-workflow-example.md
│   ├── chapter-by-chapter-drafting.md
│   └── act-break-review-results-example.md
├── templates/            # Reusable format templates
│   ├── chapter-brief.md
│   ├── character-profile.md
│   ├── setting-profile.md
│   └── rolling-summary.md
├── SKILL.md             # This file
└── README.md            # Quick-start guide
```

**Book content goes in the PROJECT directory, not here.** See "Book Files Go in the Project" section above for what goes where.

## Usage Guidelines

### Autonomous Team Workflow

**PRINCIPLE:** Teams should resolve questions autonomously using research, creative decision-making, and consistency checking. Only escalate decisions that fundamentally alter story structure, core character arcs, or emotional outcomes.

**How it works:**

1. **Alex leads** — Developmental Editor makes creative decisions based on outline tone/themes
2. **Riley researches** — Factual questions get delegated research
3. **Casey tracks** — Continuity Editor records all decisions to character/setting files
4. **Quinn verifies** — Fact-checker confirms authenticity of technical/military details
5. **Escalate only when needed** — Flag decisions that change story's core to author

**What teams resolve autonomously:**
- Character motivations, personality traits, mannerisms
- Background details, career paths, professional expertise
- Relationship dynamics (unless core arc)
- Scene specifics, dialogue approaches, pacing details
- Technical details (within realism constraints)
- Secondary character choices
- Setting specifics, atmospheric specifics

### Parallel Chapter Writing with delegate_task

For multi-chapter arcs, chapters can be written in parallel using `delegate_task` subagents, as long as they use different POV characters or cover different time periods/locations.

**When to parallelise:**
- Chapters with **different POV characters** can run simultaneously (e.g., Stuart POV + Dragan POV)
- Chapters covering **different time periods or locations** can run simultaneously
- Chapters covering **simultaneous timeline events from different perspectives**
- Chapters where one **depends on another's output** must run sequentially

**Pattern (proven in practice):**
1. **Build chapter brief** for each chapter using the template (templates/chapter-brief.md)
2. **Delegate each chapter** via delegate_task with:
   - Full chapter brief embedded in context
   - Relevant character files and scene breakdown loaded
   - Instruction to write chapter, THEN run team review (Alex/Jordan/Casey), apply fixes, verify with wc -w
3. **After all subagents return** — run Stage 5b Cross-Chapter Continuity Pass (Casey) to catch cross-chapter issues introduced by parallel writing
4. **Present the batch** to the author

**Important:** Each delegated subagent must run its OWN team review before returning. Never delegate writing without also delegating the review in the same task. The review gate applies to subagents too.

### Communication Format

When presenting team questions or collaborative discussions:
- **CONSOLIDATE** all questions/topics together
- **CLEAR SPEAKER ATTRIBUTION** — always show who's asking/deciding what
- Don't just dump raw dialogue — organize by character/topic
- Use headers to show which team member is speaking

Example format:
```markdown
## CHARACTER NAME

**Questions from Alex (Developmental Editor):**
1. Question one?
2. Question two?

**Questions from Casey (Continuity Editor):**
1. Practical detail?
2. Consistency check?

**Decisions (Alex):**
- Resolution: [what was decided and why]
```

### Using Team Personas

**Individual Consultation:**
```
"As Jordan, review this passage and suggest line-level improvements..."
"Riley, I need research on 1970s Soviet surveillance techniques..."
"Casey, check if this character detail matches what we established earlier..."
```

**Team Meetings:**
```
"Convene Alex (developmental), Casey (continuity), and Riley (research) to discuss this scene..."
"Get editorial input from Jordan and Taylor on this chapter..."
```

**Stage-Based Selection:**
```
"Early draft stage - I need input from Alex and Sam"
"Polishing stage - Jordan and Taylor should review this"
"Final review - Morgan and Quinn, please check this"
```

Each team member has:
- Distinct personality and communication style
- Specific expertise area
- Clear boundaries on what they address
- Professional relationship with author

See [team/ROSTER.md](team/ROSTER.md) for complete team member profiles.

### Using the Knowledge Repository

Book-specific files go in the **project directory** (see Book Files section above).

**Project subdirectories to create:**
- **characters/** — One file per character or character group
- **settings/** — One file per location or setting
- **research/** — Organized by topic
- **timelines/** — Chronological files or event tracking
- **concepts/** — Ideas, themes, inspiration snippets

Use clear, descriptive filenames:
- `characters/protagonist-name.md`
- `settings/london-1940.md`
- `research/spy-techniques-cold-war.md`

## Accessing Information

When working on a novel, agents can reference this material using:
- `/skill novel-team` — Load this skill into context
- Direct file reads from the `novel-team/` directory
- Search within skill files for specific details

## Collaboration Notes

- This is a shared resource — keep entries clear and well-organized
- Use consistent naming conventions
- Update entries as details evolve during writing
- Add continuity notes when details change
