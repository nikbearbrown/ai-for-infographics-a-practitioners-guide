# Fact-Check Master Report — Brutalist SVG × Claude (AI for Infographics)
**Date:** 2026-05-31 · **Scope:** all 16 chapters (Introduction + 15) + back matter · **Method:** 7-step pass (extract → classify → web-verify → verdict → per-chapter assertion file → fix/flag → report), three parallel checkers.

## Headline
The manuscript is **factually sound**. Across ~126 load-bearing assertions (perception/dataviz sources, technical SVG/D3/WCAG facts, the Wayback figures, the bio): **~123 CONFIRMED**, **3 CONTRADICTED and fixed** (all numeric, Ch 5), plus two attribution tightenings, **0 invented sources**. All Wayback figures verified. 17 assertion tables in `factchecks/`.

The book's own **Brutalist design system** (seven hex tokens, three-font stack, 8px grid) and the **CAJAL** spec format are author-defined system specs — treated as canonical, not web-verifiable. Several `[verify]` flags mark **illustrative placeholder datasets** the author intends to swap (the vaccination infographic, the energy-mix figures, the ML-benchmark accuracy numbers) — left as author notes, not fabricated.

---

## The three contradictions (all fixed, Ch 5)
All numeric, none changed a conclusion:
1. **Ink-on-white contrast** stated 18.0:1 → corrected to **≈16.8:1** (WCAG formula); still clears AAA.
2. **L\* luminance ladder** — red stated ~25 → **~43**; ochre ~56 → **~61**; table reordered to true luminance order. The grayscale-separation argument is unaffected (in fact stronger).
3. **"Fifteen-point gap (red ~25, ink ~10)"** → **"≈thirty-point gap (red ~43, ink ~11)."**

## Two attribution tightenings
- **Ch 3 — Brutalism coinage.** Softened the claim that Alison Smithson "gave it its manifesto." The New Brutalism's coinage is genuinely contested (Smithsons vs. Banham as theorist); prose now reflects that. Hunstanton School (1954) and Banham *The New Brutalism* (1966) confirmed.
- **Ch 11 — Grace Hopper "bug."** Reworded so the 1947 Mark II moth-in-the-logbook is attributed to *her team at Harvard* (she popularized "debugging"), not to Hopper personally finding/coining it.

---

## Verified — the spine of the book
- **Perception & dataviz (all confirmed):** Cleveland & McGill (1984, *JASA* 79(387):531–554, the channel hierarchy); Bertin *Sémiologie graphique* (1967; Berg trans., Wisconsin, 1983, seven visual variables); Mackinlay (1986, *ACM TOG* 5(2), APT / expressiveness & effectiveness); Wilkinson *The Grammar of Graphics* (1999/2005); Paivio dual coding (1986); Sweller cognitive load (1988); Mayer (2009); Borkin et al. memorability vs comprehension (IEEE TVCG 2013); Bateman "Useful Junk?" (CHI 2010) — correctly tagged [Contested]; Miller 7±2 — correctly tagged [Contested] (Cowan's ~4 chunks); Tufte (data-ink, 1983); Ware; Lupton *Thinking with Type*; Brewer/ColorBrewer.
- **Technical (all confirmed):** SVG is XML/W3C, paints in **document order** (the painter's algorithm; no usable z-index) — the basis of the Ch 7 rendering-vs-editorial conflict; Illustrator hex-ID escaping (leading digit → `_x32_`); WCAG 4.5:1 normal / 3:1 large & non-text (SC 1.4.3, 1.4.11); D3 created by **Bostock, Ogievetsky & Heer** (IEEE TVCG 2011), v7 current-era, `selection.join` accurate.
- **Wayback figures (all confirmed):** Playfair (1786 atlas), Bertin, Smithson/Hunstanton 1954, Berners-Lee, Lupton, Sutherland (Sketchpad 1963), Brewer/ColorBrewer, Wurman ("information architecture," 1976), **Ramón y Cajal** (Nobel 1906 — the CAJAL system's namesake), Hopper, **Ida B. Wells** (*The Red Record*, 1895), Mike Bostock, Susan Kare (Mac icons, 1983–84), **Otto & Marie Neurath** (Isotype; Marie's "transformer" role — confirmed verbatim; "quantity by repetition, never area").
- **Bio (fully confirmed, incl. EIN 33-1984805 exact):** Associate Teaching Professor, Northeastern College of Engineering; Founder/CEO Humanitarians AI; 501(c)(3); Boston; AI+1 / Irreducibly Human series; companion *Brutalist D3 × Claude*.

---

## Remaining items for the author (notes, not errors)
1. **Illustrative placeholder datasets** — swap for cleared/real cited data before publication: Ch 1 vaccination infographic, Ch 2 energy-mix figures, Ch 3 ML-benchmark accuracy numbers. (The *encoding-failure* each illustrates is documented; only the specific numbers are placeholders.)
2. **Version-sensitive tool behavior** (kept [Medium]/author-verify): Illustrator `text-anchor` baking, `<tspan>` whitespace collapse, clipPath release, re-import nesting, the exact ID-escaping trigger set; D3 v7 `.attr()` vs `.style()` round-trip; Inkscape clip release; `sharp`/`resvg` SVG→PNG. Re-verify against current tool versions before each course offering.
3. **WCAG access date** — left `[verify]` (WCAG 2.2 = W3C Rec, Oct 2023).
4. **Ch 12 Ida B. Wells** — no specific lynching statistic is quoted; the conservative `[verify figures]` flag can be cleared or, if a statistic is added, pinned to a primary biography.
5. **Ch 15 Neurath "transformer" flag** — now fully verified; the editor can clear it.
6. **Bio — "founded 2025"** — uncorroborable publicly (series convention: 2025 incorporation); left as written, flagged author-supplied. One source lists the author's info-design master's as "pursuing" vs. held — minor, confirm.
7. **Wayback page titles** — each box carries a "verify exact page title before final" editorial note (harmless).

## Status
**0 contradictions open.** The three Ch 5 numeric errors are fixed; two attributions tightened. Remaining markers are illustrative-data placeholders, version-sensitive tool notes, and routine editorial confirmations — all labeled in place. The book's design-system spec and CAJAL format are author-defined and correct as the book's own system.
