# Fact-check — Chapter 8: Color Systems and Typography for Infographics

| Assertion | Type | Verdict | Source / URL | Note |
|---|---|---|---|---|
| WCAG (2.2) minimum contrast for normal text is 4.5:1 | VERIFIABLE (standard) | CONFIRMED | https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html | SC 1.4.3 (Level AA): 4.5:1 for normal text, 3:1 for large text. Correct. |
| Non-text/graphical-object contrast minimum is 3:1 | VERIFIABLE (standard) | CONFIRMED | https://www.w3.org/TR/WCAG22/ (SC 1.4.11) | SC 1.4.11 Non-text Contrast = 3:1. Chapter focuses on 4.5:1 for text, correct for its labels case. |
| WCAG 2.2 is a W3C Recommendation (2023) | ATTRIBUTION | CONFIRMED | https://www.w3.org/TR/WCAG22/ | WCAG 2.2 became a W3C Recommendation on 5 Oct 2023. Sources line correct. |
| Opacity compounds: group `opacity="0.5"` × child `fill-opacity="0.5"` → 25% effective | VERIFIABLE (technical) | CONFIRMED | SVG render/compositing model (W3C SVG); standard group-opacity behavior | Group opacity applies to the composited group as a whole and multiplies with element-level opacity. 0.5 × 0.5 = 0.25 is correct. |
| Luminance reads as ordered magnitude reliably; hue reads as category — so sequential data needs a luminance ramp, categorical needs hue | VERIFIABLE-EMPIRICAL | CONFIRMED | Ware, *Information Visualization* 4th ed. 2020; ColorBrewer scheme-type docs | Standard perceptual finding; the vaccination-figure failure (ramping hue for ordered data) is a textbook ColorBrewer-style error. |
| Grayscale test: hue-only encodings collapse for colorblind / monochrome readers | VERIFIABLE-EMPIRICAL | CONFIRMED | ColorBrewer accessibility rationale; color-vision literature | Sound. |
| `text-anchor="middle"` centers text on its anchor; Illustrator may bake alignment and drop the attribute on re-export | VERIFIABLE (tool, version-sensitive) | NEEDS-NUANCE | SVG spec for text-anchor semantics; Adobe behavior version-dependent | text-anchor semantics confirmed. The Illustrator baking behavior is version-sensitive — keep as [Medium]/author-verify per task instructions. |
| `<tspan>` whitespace collapse on Illustrator import | VERIFIABLE (tool) | NEEDS-NUANCE | Version-sensitive Illustrator/XML whitespace handling | Plausible, version-dependent. Keep [Medium]. |
| Cynthia Brewer (cartographer, Penn State) created ColorBrewer; classifies schemes as sequential / diverging / qualitative; flags colorblind- and print-safe | ATTRIBUTION / HISTORICAL | CONFIRMED | https://colorbrewer2.org/ ; https://en.wikipedia.org/wiki/ColorBrewer | Cynthia A. Brewer, Dept. of Geography, Penn State. ColorBrewer launched 2002 (Brewer, Mark Harrower, Penn State). Sequential/diverging/qualitative taxonomy and colorblind/print-safe flags all correct. |
| Ware, *Information Visualization: Perception for Design*, 4th ed., Morgan Kaufmann, 2020 (Sources) | ATTRIBUTION | CONFIRMED | Morgan Kaufmann, 4th ed. 2020 | Correct. |
| Lupton, *Thinking with Type*; Stone, *A Field Guide to Digital Color* (2003) (Sources) | ATTRIBUTION | CONFIRMED | A K Peters 2003 (Stone); Princeton Architectural Press (Lupton) | Correct. |
| Monospace (JetBrains Mono) aligns digits by place value, aiding numeric comparison | VERIFIABLE | CONFIRMED | Typographic common knowledge (tabular/monospace figures) | Accurate; monospaced digits column-align. |

## Notes on the worked-example numbers
- The "≈1.9:1" contrast for pale-yellow-on-white and the "well above 4.5:1" for ink-on-white are illustrative/order-of-magnitude. Ink `#2a1a0e` on white is ~15–16:1 (far above 4.5:1); secondary gray `#545454` on white is ~7:1 (above 4.5:1). Directionally correct; chapter already flags "[verify exact ratios at production]." Left as author-verify.

## Resolved `[verify]` flags
- Line 7 / line 99 WCAG 4.5:1: **CONFIRMED**; the [High] tags are accurate.
- Line 107 "[High — ColorBrewer ... verify exact page title]": **RESOLVED** — Wikipedia page "ColorBrewer"; Brewer's bio page "Cynthia Brewer." Left Wayback note.
- Line 77, 79 text-anchor / tspan "[Medium, verify]": kept as version-sensitive per instructions.
- Line 131 Sources WCAG "[Verify access date ... version-sensitive]": routine, kept.

## Author-framing / in-world system (not verified)
- Seven-token table (hex values, roles), three-font stack, two-data-color ceiling, "ochre never encodes data," "red is not danger" — Brutalist design system, author-defined. Left as system spec.

**Verdict counts:** CONFIRMED 11, NEEDS-NUANCE 2, CONTRADICTED 0, UNVERIFIABLE 0.
**Fixes applied:** none to prose (all empirical claims confirmed; ratios already flagged for production-verify).
**Flags resolved:** 2 (WCAG ratios; ColorBrewer title). **Flags kept (version-sensitive):** 2 (text-anchor, tspan).
