# Fact-check — Chapter 11: The Brutalist System: The Claude Design Project

| Assertion | Type | Verdict | Source / URL | Note |
|---|---|---|---|---|
| Grace Hopper — naval officer, computer scientist, principal force behind machine-independent programming languages | HISTORICAL | CONFIRMED | https://en.wikipedia.org/wiki/Grace_Hopper ; https://www.vassar.edu/grace-hopper/achievements | Hopper devised the theory of machine-independent programming languages; developed FLOW-MATIC; central to COBOL's lineage. Chapter says "a principal force behind machine-independent programming languages" and "compilers and COBOL's lineage" — accurately hedged (does not claim she single-handedly invented COBOL). |
| Hopper is "associated with literally documenting a 'bug' — taping a moth into a logbook" (1947, Harvard Mark II) | HISTORICAL | NEEDS-NUANCE | https://en.wikipedia.org/wiki/Grace_Hopper | The moth was found 9 Sep 1947 in the Mark II by Hopper's *associates/team*; the log entry reads "First actual case of bug being found." Hopper popularized the "debugging" story but did not personally find/coin it, and "bug" predates 1947 (Edison 1878). The chapter's phrasing "associated with" is defensible and does not overclaim authorship, but a reader could infer she taped it in herself. Flag as nuance — recommend the soft phrasing be kept ("associated with"). Logbook now at the Smithsonian. |
| Sculley et al., "Hidden Technical Debt in Machine Learning Systems," *NeurIPS*, 2015 | ATTRIBUTION | CONFIRMED | https://proceedings.neurips.cc/paper_files/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html | NeurIPS (NIPS) 2015, Sculley et al. The "unmanaged artifacts accrue maintenance debt" framing is faithful to the paper. |
| Gebru et al., "Datasheets for Datasets," *Communications of the ACM*, 2021 | ATTRIBUTION | CONFIRMED | https://dl.acm.org/doi/10.1145/3458723 | CACM 2021 (arXiv 2018). Correct. |
| Mitchell et al., "Model Cards for Model Reporting," *FAccT*, 2019 | ATTRIBUTION | CONFIRMED | https://dl.acm.org/doi/10.1145/3287560.3287596 | FAT*/FAccT 2019. Correct. |
| D3 v7 `selection.join()` is the modern data-binding lifecycle pattern; `.attr()` writes presentation attributes that survive SVG→Illustrator, `.style()` writes inline CSS Illustrator may drop | VERIFIABLE (technical) | CONFIRMED (principle) / version-sensitive | https://d3js.org/ (selection.join docs) | `selection.join` introduced in D3 v5+, standard in v7. The `.attr()` vs `.style()` round-trip distinction is sound (presentation attributes vs inline style). Exact Illustrator flattening is version-sensitive — keep as author-verify. |
| `slug()` / leading-digit ID escaping (`"1st Floor"` → `_x31_st-floor`) cross-ref to Ch7 | VERIFIABLE (tool) | CONFIRMED | (verified in Ch7 factcheck) | Consistent with confirmed Illustrator hex-escaping behavior. |

## Author-framing / in-world system (NOT verified, per task instructions)
- Three governing files (CLAUDE.md / DESIGN.md / PROJECT.md); the Intent/Schema two-layer split; the five-phase pipeline (Audit→Schema→Generate→Verify→Handoff); the phase gate; refusal behavior; semantic-layer scaffold; the seven tokens and prohibited-actions list. All Brutalist System design (chapter self-flags lines 18, 141 `*verify — system specifics*`). Left as system spec.
- The "week-long loop" / "eleven-ish defects" opening anecdote — illustrative narrative, author-defined.

## Resolved `[verify]` flags
- Line 111 "[High — Hopper ... verify exact page title]": **RESOLVED** — Wikipedia "Grace Hopper." Wayback note edited into prose; the moth/COBOL claims kept with their existing careful hedging (see NEEDS-NUANCE row).
- Line 140 Sources "[Verify exact page title and dates]" (Hopper): resolved.
- Line 135 Sources "Claude Code documentation [High aging risk; verify access date]": retained — appropriately flagged, version/time-sensitive.
- Lines 18, 54, 141 "*verify — system specifics*": retained as author-defined system notes.

## Note for master report
- Hopper/moth attribution is the one item worth a light editorial eye: the chapter already uses "associated with," which is accurate, but if the author wants maximal precision, a half-clause ("her team taped a moth into the logbook; she popularized the 'debugging' story") would remove any inference she found it personally. Not a contradiction — left to author discretion; no fix forced.

**Verdict counts:** CONFIRMED 6, NEEDS-NUANCE 1, CONTRADICTED 0, UNVERIFIABLE 0.
**Fixes applied:** Hopper Wayback page title resolved in prose.
**Flags resolved:** 1 (Hopper title). **Flags kept:** Claude Code aging-risk + system-specifics (intentional).
