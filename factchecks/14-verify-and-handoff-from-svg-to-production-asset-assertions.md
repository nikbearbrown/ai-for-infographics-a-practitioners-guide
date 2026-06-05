# Fact-check — Chapter 14: Verify and Handoff: From SVG to Production Asset

Verified May 2026. Illustrator/Inkscape import behaviors kept as [Medium]/author-verify — correct in spirit, version-sensitive.

| Assertion | Type | Verdict | Source / URL | Note |
|---|---|---|---|---|
| Susan Kare designed the original Macintosh icons in the early 1980s, working on grid paper pixel by pixel (trash can, watch, etc.) | HISTORICAL | CONFIRMED | [Smithsonian](https://www.smithsonianmag.com/innovation/how-susan-kare-designed-user-friendly-icons-for-first-macintosh-180973286/); [Susan Kare — Wikipedia](https://en.wikipedia.org/wiki/Susan_Kare) | Kare worked at Apple from 1983; used a grid sketchbook (each square = one pixel); created trash can, disk, watch, bomb, etc. Mac shipped January 1984. Chapter's "early 1980s" / "1983–84" framing accurate. |
| Kare's icons were bitmapped, monochrome, built to survive at fixed tiny resolution under hardware constraints | HISTORICAL | CONFIRMED | as above | Bitmapped for Mac screens; monochromatic with shading via pixel density. Accurate. |
| "Production-asset, not just pretty picture" framing for Kare | AUTHOR-FRAMING | CONFIRMED (framing) | Hertzfeld, Folklore.org | Analogy is author's; underlying facts hold. Existing `[High — verify specific details]` flag conservative; can stand. |
| WCAG 4.5:1 contrast required on all text; large text 3:1; non-text 3:1 (1.4.11) | VERIFIABLE-EMPIRICAL | CONFIRMED | [WCAG 2.2 — W3C](https://www.w3.org/TR/WCAG22/); [WebAIM contrast](https://webaim.org/articles/contrast/) | 4.5:1 normal text, 3:1 large text (18pt / 14pt bold), 3:1 non-text per SC 1.4.11. All accurate. Chapter cites WCAG 2.2 (2023 — actually published Oct 2023). |
| WCAG 2.2 is a W3C Recommendation (2023) | VERIFIABLE-EMPIRICAL | CONFIRMED | [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) | Became W3C Recommendation 5 October 2023. The `[access date at final draft]` / `[verify]` flag is correctly left open per protocol. |
| Illustrator: *Open* parses SVG into editable objects; *Place* embeds linked/rasterized object | VERIFIABLE-EMPIRICAL (tool) | CONFIRMED / [Medium] | Adobe Illustrator docs | Behavior accurate. Version-sensitive; keep `[Medium]`. |
| Releasing clipping masks: Illustrator `Object → Clipping Mask → Release`; Inkscape `Object → Clip → Release` | VERIFIABLE-EMPIRICAL (tool) | CONFIRMED / [Medium] | Adobe / Inkscape docs | Menu paths correct as of current versions. Keep version note. |
| `text-anchor` (start/middle/end) anchors text to `x`; some export/import paths bake position and drop the attribute, drifting the label | VERIFIABLE-EMPIRICAL (tool/version) | NEEDS-NUANCE / [Medium] | [W3C SVG 2 `text-anchor`](https://www.w3.org/TR/SVG2/text.html); Adobe docs | `text-anchor` semantics correct. The specific Illustrator drop-and-bake behavior is plausible and documented anecdotally; version-sensitive. Keep existing `[Medium]` flag. |
| `<tspan>` whitespace collapse can damage multi-word labels on import | VERIFIABLE-EMPIRICAL (tool/version) | NEEDS-NUANCE / [Medium] | W3C SVG whitespace handling; Adobe docs | Whitespace handling in SVG text is real; import collapse is version-sensitive. Keep `[Medium]`. |
| Exponential/geometric nesting of wrapper groups across repeated round trips | VERIFIABLE-EMPIRICAL (tool/version) | NEEDS-NUANCE / [Medium] | Adobe docs / practitioner reports | Directionally correct (round trips accrete wrapper `<g>`); "exponential/geometric" is an informal characterization. Keep existing `[Medium — verify]` flag. |
| Inkscape is a free/open-source vector editor; workflow maps near one-to-one | VERIFIABLE-EMPIRICAL | CONFIRMED / [Medium] | [inkscape.org](https://inkscape.org/) | Accurate. |
| SVG user unit / DPI: 96 DPI in CSS contexts, 72 DPI in some print contexts; must declare target DPI | VERIFIABLE-EMPIRICAL | CONFIRMED | [W3C CSS units](https://www.w3.org/TR/css-values/) | CSS reference pixel = 1/96 in; legacy print = 72 DPI. The need to declare target DPI for raster export is accurate. |
| `svg-to-png.mjs` built on a headless renderer such as `sharp` or `resvg`, rasterizes at 300 DPI | VERIFIABLE-EMPIRICAL (current-state) | CONFIRMED / [Medium] | sharp / resvg project docs | `sharp` and `resvg` are real SVG rasterizers. Author-defined script. Keep `[Medium]` current-state. |
| Brewer, ColorBrewer 2.0 (Penn State) | ATTRIBUTION-CITATION | CONFIRMED | [colorbrewer2.org](https://colorbrewer2.org/) | Cynthia Brewer, Penn State. Accurate. |

## Verdict counts
- CONFIRMED: 9
- NEEDS-NUANCE (kept as [Medium], version-sensitive): 4 (text-anchor drop, tspan collapse, exponential nesting, sharp/resvg)
- CONTRADICTED: 0
- UNVERIFIABLE: 0

## Fixes applied
None required.

## Flags
- Open (pre-existing, appropriate): WCAG `[access date at final draft]`; Illustrator/Inkscape `[verify against current version]`; Kare `[verify specific details]`. All correct in spirit; left as author-verify per protocol.
