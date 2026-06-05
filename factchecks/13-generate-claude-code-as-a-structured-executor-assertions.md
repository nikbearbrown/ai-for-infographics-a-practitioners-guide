# Fact-check — Chapter 13: Generate: Claude Code as a Structured Executor

Verified May 2026. D3/Illustrator/Claude Code version specifics kept as [Medium].

| Assertion | Type | Verdict | Source / URL | Note |
|---|---|---|---|---|
| D3 created by Mike Bostock, building on earlier Protovis work with Jeffrey Heer | HISTORICAL | CONFIRMED | [Mike Bostock — Wikipedia](https://en.wikipedia.org/wiki/Mike_Bostock); [Stanford Vis](http://vis.stanford.edu/papers/d3) | Bostock is the creator; Protovis (Bostock & Heer) preceded D3. Accurate. |
| Bostock, Ogievetsky & Heer, *D³: Data-Driven Documents*, IEEE TVCG, 2011 | ATTRIBUTION-CITATION | CONFIRMED | [Stanford Vis PDF](http://vis.stanford.edu/files/2011-D3-InfoVis.pdf); [IEEE/ACM DOI 10.1109/TVCG.2011.185](https://dl.acm.org/doi/10.1109/TVCG.2011.185) | IEEE TVCG vol. 17, pp. 2301-2309, 2011. Authors and venue exactly correct. |
| D3 designed as low-level primitive that binds data to the DOM, not a high-level `barChart()` charting library; designer specifies the mapping explicitly | HISTORICAL / AUTHOR-FRAMING | CONFIRMED | [What is D3? — d3js.org](https://d3js.org/what-is-d3); paper abstract | "representation-transparent... direct inspection and manipulation of... the DOM"; "designers selectively bind input data to arbitrary document elements." The specification-driven characterization is accurate. |
| D3 v7's `selection.join()` manages enter/update/exit lifecycle cleanly | VERIFIABLE-EMPIRICAL (version) | CONFIRMED / [Medium] | [d3-selection joining — d3js.org](https://d3js.org/d3-selection/joining); [GitHub d3/d3-selection](https://github.com/d3/d3-selection) | `selection.join` introduced in D3 v5, supported through v7. Description accurate. Keep version-pin note. |
| Presentation attributes via `.attr()` survive Illustrator export better than `.style()`-set inline CSS | VERIFIABLE-EMPIRICAL (tool/version) | NEEDS-NUANCE / [Medium] | Adobe Illustrator SVG docs; [W3C SVG 2 presentation attributes](https://www.w3.org/TR/SVG2/) | Presentation attributes vs. inline styles are handled differently on import; the directional claim (`.attr()` more robust) is correct in spirit but version-sensitive. Keep `[Medium]`. |
| Slug pattern preventing `_x31_` artifacts (prepend `n` to leading digit) | VERIFIABLE-EMPIRICAL | CONFIRMED | [W3C SVG 2 / XML id rules](https://www.w3.org/TR/SVG2/) | IDs cannot start with a digit; the slug remedy is technically sound. |
| Claude Code as structured executor / governing files (CLAUDE.md, DESIGN.md, PROJECT.md) loaded in session | VERIFIABLE-EMPIRICAL (current-state) | CONFIRMED / [Medium] | Anthropic Claude Code docs (current) | Author-defined design stance plus accurate current-state tool behavior. Existing `[High — design stance]` / `[Medium]` tags appropriate. |
| y-axis truncation makes change look more dramatic; truncated axis is a perceptual-accuracy failure | VERIFIABLE-EMPIRICAL | CONFIRMED | Standard data-visualization literature (Cleveland & McGill lineage) | Well-established. |
| Eisenberg & Bellamy-Royds, *SVG Essentials* (2nd ed.), O'Reilly, 2018 | ATTRIBUTION-CITATION | CONFIRMED | O'Reilly catalog | 2nd edition 2018. Accurate. |

## Verdict counts
- CONFIRMED: 7
- NEEDS-NUANCE (kept as [Medium], version-sensitive): 2 (`.attr()` vs `.style()` import; D3 v7 pin)
- CONTRADICTED: 0
- UNVERIFIABLE: 0

## Fixes applied
None required.

## Flags
- Open (pre-existing, appropriate): `[verify against pinned D3 v7]`, `[verify .style() vs .attr() import behavior]`, Claude Code aging note. All correct in spirit; left as author-verify per protocol.
- Illustrative eleven-count violation set is correctly tagged `[Medium — illustrative; varies by model/run]`. No action.
