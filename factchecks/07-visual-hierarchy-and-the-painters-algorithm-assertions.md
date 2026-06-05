# Fact-check — Chapter 7: Visual Hierarchy and the Painter's Algorithm

| Assertion | Type | Verdict | Source / URL | Note |
|---|---|---|---|---|
| SVG has no z-index like CSS; later elements paint over earlier ones; document order = paint order = visual depth | VERIFIABLE-EMPIRICAL (technical) | CONFIRMED | https://www.w3.org/TR/SVG11/render.html ; https://www.w3.org/TR/SVG2/render.html | SVG 1.1 uses a strict painter's model in document order. SVG 2 *defines* a `z-index` property, but no major browser supports it for SVG content, so "no z-index in the way CSS does" is accurate in practice. |
| "Painter's Algorithm" is the standard term for back-to-front depth ordering | HISTORICAL / VERIFIABLE | CONFIRMED | https://en.wikipedia.org/wiki/Painter's_algorithm | Standard term; aka depth-sort / priority-fill. Introduced 1972 (Newell, Newell, Sancha). Chapter uses the analogy correctly; it applies the *name* to SVG's document-order model, which is a reasonable pedagogical extension (SVG specs call it the "painter's model"). |
| SVG/document-order paint requirement conflicts with editorial layer grouping in Illustrator | VERIFIABLE (tool behavior) | CONFIRMED (principle) / NEEDS-NUANCE (version-specific) | Adobe community threads; SVG render model | The structural conflict (depth order vs. by-kind grouping) is real and well grounded. Specific Illustrator import behavior is version-sensitive — see escaping below. |
| Illustrator maps SVG `id` to layer name and hex-escapes illegal characters; a leading digit `2` becomes `_x32_` (so `2008-spike` → `_x32_008-spike`) | VERIFIABLE (tool behavior) | CONFIRMED | https://community.adobe.com/t5/illustrator-discussions/layer-names-with-non-alphanumeric-characters-converted-to-hex-code-when-exporting-svgs/td-p/14771352 | Confirmed: leading digit "1" → `_x31_` (e.g., "1st-floor" → "_x31_st-floor"); "#" → `_x23_`; "_" → `_x5F_`. The chapter's `_x32_008-spike` for a leading "2" is exactly correct (hex 32 = "2"). Note one Adobe thread reports the behavior varied between v28.5 and v28.6 — keep as version-sensitive [Medium]. |
| `text-anchor`/clipPath/round-trip behaviors are version-sensitive Illustrator quirks | VERIFIABLE (tool) | NEEDS-NUANCE | Adobe docs; community reports | Direction is correct (masks can scramble structure; re-import deepens nesting). Exact behavior depends on Illustrator version. Keep [Medium] / author-verify as the chapter already flags. |
| Ivan Sutherland's *Sketchpad* (1963) was the first system treating a drawing as a structured, editable object; depth-ordering lineage | HISTORICAL | CONFIRMED | https://en.wikipedia.org/wiki/Sketchpad ; https://en.wikipedia.org/wiki/Ivan_Sutherland | Sketchpad, 1963 MIT PhD thesis (TX-2, Lincoln Lab), light pen, constraints, recursive subpictures, first clipping algorithm. "Structured object vs. rendered image" framing is accurate. Sutherland is foundational to interactive computer graphics and the field that produced hidden-surface/depth-ordering work. |
| W3C SVG 2 spec is authoritative for document order / rendering model (Sources) | ATTRIBUTION | CONFIRMED | https://www.w3.org/TR/SVG2/render.html | Correct. |
| Eisenberg & Bellamy-Royds, *SVG Essentials* 2nd ed., O'Reilly 2014 (Sources) | ATTRIBUTION | CONFIRMED | O'Reilly, 2nd ed. 2014 | Correct. Chapter writes "2014/2018"; 2nd ed. is 2014 — acceptable. |

## Resolved `[verify]` flags
- Line 80 "[Medium — verify the exact escaping pattern]": **CONFIRMED** as a principle (`_x32_` for leading "2"). Left as [Medium] because the precise trigger set is version-sensitive (per Adobe v28.5/v28.6 report).
- Line 124 "[Verify Sutherland's exact Wikipedia page title]": **RESOLVED** — page is "Ivan Sutherland" (Sketchpad has its own page "Sketchpad"). Edited prose.
- Line 132 Sources "[verify version]" (SVG spec): SVG 2 confirmed as authoritative; left as routine.
- Line 134 Sources "[verify]" (Adobe): kept — version-sensitive, author-verify at production.

## Version-sensitive items kept as [Medium] / author-verify (per task instructions)
- `text-anchor` baking on Illustrator export (line 77 of Ch8, cross-referenced here).
- clipPath release scrambling layer order (line 82).
- Re-import nesting compounding (line 84).
- Exact ID-escaping trigger set across Illustrator versions (line 80).

## Author-framing / in-world system (not verified)
- The two-axis multi-layer architecture, `data-name` convention, "one-way ticket" rule — Brutalist system design. Left as system notes.

**Verdict counts:** CONFIRMED 6, NEEDS-NUANCE 2, CONTRADICTED 0, UNVERIFIABLE 0.
**Fixes applied:** Sutherland Wayback page title resolved in prose.
**Flags resolved:** 2 (Sutherland title; escaping pattern confirmed-as-principle). **Flags kept (version-sensitive, intentional):** 4.
