# Fact-check — Chapter 12: Audit: What Exists Before You Touch Anything

Verified May 2026. Tool-version behaviors (Illustrator `_x31_` escaping, SVG ID rules) kept as [Medium]/author-verify — correct in spirit, version-sensitive.

| Assertion | Type | Verdict | Source / URL | Note |
|---|---|---|---|---|
| Ida B. Wells published *The Red Record* in 1895 | HISTORICAL | CONFIRMED | [Project Gutenberg](https://www.gutenberg.org/files/14977/14977-h/14977-h.htm); [US Capitol Visitor Center](https://www.visitthecapitol.gov/artifact/red-record-tabulated-statistics-and-alleged-causes-lynchings-united-states-1892-1893-1894) | Full title *A Red Record: Tabulated Statistics and Alleged Causes of Lynchings in the United States, 1892-1893-1894*; ca. 1895. Chapter's short title "The Red Record" is the conventional name. |
| Wells compiled lynching statistics from white-owned newspapers because their hostile provenance made the count unassailable | HISTORICAL | CONFIRMED | [Womens History Museum](https://www.womenshistory.org/education-resources/biographies/ida-b-wells-barnett); [blackfreedom.proquest.com](https://blackfreedom.proquest.com/a-red-record-tabulated-statistics-and-alleged-causes-of-lynchings-in-the-united-states-1892-1893-1894/) | *A Red Record* used mainstream white newspaper accounts to document mob violence. Core claim accurate. |
| Wells's anti-lynching data journalism / "audit before the argument" framing | HISTORICAL / AUTHOR-FRAMING | CONFIRMED (framing) | as above | The analogical framing is author's; the underlying facts (statistical compilation, hostile sourcing) check out. No specific lynching statistic is quoted verbatim in the chapter, so no single figure to confirm. Existing `[High — verify specific figures]` flag is appropriately conservative; can stand. |
| Sculley et al., *Hidden Technical Debt in Machine Learning Systems*, NeurIPS 2015 — most expensive failures are unmanaged dependencies / silent assumptions | ATTRIBUTION-CITATION | CONFIRMED | [NeurIPS proceedings](https://proceedings.neurips.cc/paper_files/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html) | Authors D. Sculley, G. Holt, et al., NeurIPS 2015. Paraphrase of the "technical debt" thesis is accurate (entanglement, hidden feedback loops, undeclared consumers, data dependencies). |
| Gebru et al., *Datasheets for Datasets*, Communications of the ACM 2021 | ATTRIBUTION-CITATION | CONFIRMED | [CACM / dblp](https://dblp.org/rec/journals/cacm/GebruMVVWDC21.html) | Published CACM 2021 (original arXiv 1803.09010, 2018). Provenance-documentation model accurately invoked. |
| SVG painter's algorithm: later elements paint over earlier; z-order = document order | VERIFIABLE-EMPIRICAL | CONFIRMED | [W3C SVG 2](https://www.w3.org/TR/SVG2/) | Standard SVG rendering model. |
| Illustrator/SVG cannot begin an ID with a digit; leading `1` escaped to `_x31_` (e.g. `1st-floor` → `_x31_st-floor`) | VERIFIABLE-EMPIRICAL (tool/version) | NEEDS-NUANCE / [Medium] | [W3C SVG 2 naming rules](https://www.w3.org/TR/SVG2/); Adobe Illustrator docs | XML/SVG `id` rules forbid a leading digit; `_x31_` is Adobe's documented hex-escape convention (`_x` + hex of char + `_`; `1` = U+0031 = `31`). Correct in spirit. Keep existing `[High — verify exact escaping against current Illustrator version]` flag. |
| WCAG 4.5:1 contrast on all labels (referenced in Schema Layer / gap map) | VERIFIABLE-EMPIRICAL | CONFIRMED | [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | 4.5:1 for normal text is the AA threshold. Accurate. |
| D3 referenced as v7 stack (CLAUDE.md) | VERIFIABLE-EMPIRICAL (version) | CONFIRMED / [Medium] | [d3js.org](https://d3js.org/) | D3 v7 is current-era; `selection.join` supported. Keep version-pin note. |
| Claude Code as repository-aware agent that reads a directory and edits many files in one pass | VERIFIABLE-EMPIRICAL (current-state) | CONFIRMED / [Medium] | Anthropic Claude Code docs (current) | Accurate current-state description; aging risk. Existing `[Medium — tool behavior, current-state]` tag appropriate. |

## Verdict counts
- CONFIRMED: 8
- NEEDS-NUANCE (kept as [Medium], version-sensitive): 1 (`_x31_` escaping)
- CONTRADICTED: 0
- UNVERIFIABLE: 0

## Fixes applied
None required. No contradictions.

## Flags
- Open (pre-existing, appropriate): `[High — verify specific figures]` on Wells; `[High — verify exact escaping]` on `_x31_`. Both correct in spirit; left as author-verify per protocol.
