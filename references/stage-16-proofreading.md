# Stage 16 — Proofreading Workflow

Use this after Stage 15 copyedit/fact-check is complete. Stage 16 is a fresh-eyes final error catch, not another line edit, fact-check, or structural pass.

## Scope

Stage 16 should catch:
- typos and obvious spelling/register inconsistencies
- punctuation artifacts from earlier edits, especially ellipses and quote-adjacent punctuation
- contraction-cleanup artifacts such as doubled negatives or awkward `n't not` phrasing
- repeated adjacent words, double spaces, trailing spaces, and duplicate punctuation
- small dialogue-register mismatches, especially UK/US terms in British character dialogue
- final consistency issues that do not reopen macro structure

Do not use Stage 16 to:
- reopen developmental structure
- expand lean chapters for word count
- revise broad line style
- harden deliberately flexible fact-check decisions into unsupported specifics
- resolve intentionally unresolved plot statuses
- add technical, hostage, cyber, grid, route, or operational detail

## Required reviewers

- Morgan — reader-facing final clarity / payoff / obvious jarring issues
- Jordan — prose/punctuation/register final catch

## Recommended checks

1. Verify current state from `progress.md`, `AGENTS.md`, and `rolling-summary.md`.
2. Run deterministic proof scans over `chapters/*.md`:
   - repeated adjacent words: `\b([A-Za-z]{2,})\s+\1\b` using Python, not ripgrep backrefs unless PCRE2 is available
   - double spaces inside prose lines
   - trailing spaces
   - obvious contraction artifacts: `n't not`, `n’t not`, `didn't making`, `So didn't`
   - duplicate punctuation: repeated `..`, `!!`, `??`, or doubled comma/semicolon/colon
3. Run the active safety/watchlist scan from prior stages to ensure proofreading did not regress cleanup.
4. If available, run `aspell --lang=en_GB --mode=markdown list` on a temporary concatenated manuscript and inspect only plausible real errors. Expect proper nouns, place-name fragments, institution terms, and deliberate list-confusion misspellings to appear.
5. Patch only small proof fixes in chapter prose.
6. Recompute all chapter/act/manuscript word counts after any chapter edit.
7. Write `reviews/stage-16-proofreading.md` with Morgan and Jordan sections, fixes applied, remaining reservations, and Stage 17 handoff.
8. Update `progress.md`, `AGENTS.md`, and `rolling-summary.md` to Stage 17 with new review count and word totals.
9. Verify: chapter count, review count, Stage 16 review present, review gate, clean proof scan, clean safety/watchlist scan, tracking docs advanced.

## Common pitfalls

- Do not treat spellchecker output as instructions. Proper nouns and intentional in-world list variants may be correct.
- Do not “fix” intentional duplicate-name variants in evidence/list scenes; they often demonstrate confusion and source unreliability.
- Avoid broad quote-count checks in dialogue-heavy fiction: apostrophes in contractions and possessives make simple curly-single-quote balance noisy.
- If a proof fix changes one word, update all affected totals. Even a one-word change can alter act/manuscript counts.
- Keep final status concise: files changed, exact fixes, verification results, updated totals, carry-forward to Stage 17.
