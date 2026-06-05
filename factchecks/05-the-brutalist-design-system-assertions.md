# Fact-check — Chapter 5: The Brutalist Design System

Per the brief, the Brutalist design system itself (seven hex tokens, font stack, 8px grid, stroke conventions) is the book's **author-defined** system — treated as canonical, not web-verifiable. Only the externally-checkable facts woven around it are verified here: the WCAG contrast claim, the L* luminance values, the rationing-of-hue rationale, and the Lupton attribution.

| Assertion | Type | Verdict | Source / URL | Note |
|---|---|---|---|---|
| Seven color tokens / roles / allowed-prohibited uses | AUTHOR-FRAMING (canonical) | n/a | — | Author-defined design system; not web-verifiable by instruction. |
| Typography stack (EB Garamond / Inter / JetBrains Mono), 8px grid, margins, stroke conventions | AUTHOR-FRAMING (canonical) | n/a | — | Author-defined. EB Garamond, Inter, JetBrains Mono, Fira Code are all real, freely-available type families (confirmed they exist), so the stack is implementable. |
| Hue rationing rests on Cleveland & McGill: hue is a low-accuracy channel [High] | VERIFIABLE-EMPIRICAL | CONFIRMED | Cleveland & McGill 1984; Bertin 1967 | Correct — hue/color sits at the bottom of the channel-accuracy hierarchy; rationing it for category-not-quantity is well-founded. |
| Static SVG does not reliably resolve CSS custom properties across the export boundary; write literal hex [High] | VERIFIABLE-EMPIRICAL | CONFIRMED (NEEDS-NUANCE) | SVG/CSS var support; Illustrator export behavior (Ch4) | CSS custom properties (`var(--x)`) are not reliably preserved by vector editors on import; writing literal hex is the safe practice. Consistent with Ch4's presentation-attribute rule. |
| Ink (#2a1a0e) ~18.0:1 against white; clears WCAG AAA | VERIFIABLE-EMPIRICAL | **CONTRADICTED → FIXED** | WCAG 2.x relative-luminance formula (computed) | Computed contrast of #2a1a0e on #FFFFFF is **≈16.8:1**, not 18.0:1. Both clear AAA (≥7:1), so the conclusion stands, but the number was wrong. **FIXED in prose** to "≈16.8:1 ... AAA bar (7:1)". |
| L* ladder values: ink ~10, red ~25, secondary ~36, ochre ~56, border ~84, fill ~96, white ~100 | VERIFIABLE-EMPIRICAL | **CONTRADICTED → FIXED** | CIE L* computed from sRGB | Red #C8102E computes to L*≈43 (not ~25); ochre #C8860E to ≈61 (not ~56); ink ≈11, secondary ≈36, border ≈85, fill ≈97. The stated red value was substantially off, which also broke the table's ladder order (red was listed below secondary). **FIXED:** corrected all L* values, reordered the table to ladder correctly (ink → secondary → red → ochre → border → fill → white). |
| "Fifteen-point gap" between ink (~10) and red (~25) keeps them distinct in grayscale | VERIFIABLE-EMPIRICAL | **CONTRADICTED → FIXED** | Computed | With corrected values (ink ~11, red ~43) the gap is ≈32 points — the separation conclusion is *stronger*, not weaker. **FIXED:** prose now reads "L* ≈ 43 and ink at L* ≈ 11 — a gap of roughly thirty points." |
| Ellen Lupton, *Thinking with Type*: typography as a system of functional roles / hierarchy | ATTRIBUTION-CITATION | CONFIRMED | https://en.wikipedia.org/wiki/Ellen_Lupton ; Princeton Architectural Press | Lupton's hierarchy-as-roles framing is correctly attributed. *Thinking with Type*, 2nd ed., 2010, Princeton Architectural Press — correct. In-text `[Verify Lupton's exact Wikipedia page title]` is a trivial editorial note. |
| Ware (2020), Wong (2010 WSJ Guide), WCAG 2.2 (2023), ColorBrewer (Brewer) | ATTRIBUTION-CITATION | CONFIRMED | Standard references | All real and correctly cited. WCAG 2.2 became a W3C Recommendation in Oct 2023 — correct. |
| First-marriage-age demographic chart | AUTHOR-FRAMING (illustrative) | n/a | — | Narrative device; no factual claim. |

**Verdict counts:** CONFIRMED 5, CONTRADICTED-then-FIXED 3, AUTHOR-FRAMING/canonical 3.
**Fixes applied:**
1. Ink contrast 18.0:1 → ≈16.8:1 (added AAA threshold "(7:1)").
2. L* ladder table values corrected and reordered to true luminance order.
3. "fifteen-point gap (red ~25, ink ~10)" → "≈thirty-point gap (red ~43, ink ~11)."
**Flags:** the chapter's existing `[Medium — L* values are approximate; verify against a measured conversion...]` hedge was well-placed; the measured conversion has now been done and the values corrected. No open flags.
**Note for master report:** the three numeric corrections (contrast ratio + two L* errors) are the only CONTRADICTED items found across all six chapters. None changes a conclusion — ink still clears AAA, the grayscale ladder still separates — but the printed numbers were wrong and are now corrected.
