# SVG Structure for Editability — Research Synthesis

## The Short Version

SVG generated programmatically (via D3 or by hand) can be clean and Illustrator-editable, but only if specific structural decisions are made deliberately. The core problems are: nested clipping masks that Illustrator mishandles, auto-generated meaningless IDs, transform stacking that confuses coordinate systems, text converted to paths, and styling approaches that create conflicts on import. All of these are avoidable. None are automatically handled by D3's defaults.

The critical reframe: **SVG export should be a one-way ticket.** Illustrator is not a native SVG application. Open an SVG in Illustrator to correct specific things, then save as `.ai`. Do not round-trip back to SVG through Illustrator — it will degrade the file.

---

## 1. Grouping and Logical Structure

The `<g>` element is SVG's primary grouping mechanism. In terms of graphics editors, it serves the same function as Group Objects in Illustrator. Every layer in Illustrator maps to a `<g>` element with its own ID when exported; conversely, named `<g>` elements in imported SVG appear as groups within Layer 1 in Illustrator.

**The key limitation:** it is not possible to write SVG code so that Illustrator recognizes `<g>` elements as top-level *layers* rather than groups nested inside Layer 1. An Adobe community expert confirmed this directly: no SVG markup convention forces Illustrator to interpret groups as separate layers on import. Everything lands inside Layer 1 as nested groups. An Illustrator script can promote groups to layers after import, but that is manual post-processing.

**What works:** naming `<g>` elements with meaningful IDs (`id="chart-bars"`, `id="x-axis"`, `id="annotation-layer"`) so they are navigable in Illustrator's Layers panel as named groups. Illustrator copies the layer name from Illustrator exports directly as the group ID with underscores replacing spaces. For hand-coded or D3-generated SVG, the designer controls this entirely.

**D3 specifically:** D3's margin convention appends a single top-level `<g>` with a translate transform (`transform="translate(margin.left, margin.top)"`) to create the inner chart area. This produces one meaningful group wrapping all chart content, which is clean and Illustrator-friendly. The problem is everything D3 appends *inside* that group: axes, bars, lines, labels, etc., get auto-generated or functionally-named classes (`tick`, `domain`, `bar`) but rarely structured into logical editorial groups. For Illustrator editability, D3 code should explicitly group related elements — all bars into a `<g id="bars">`, all annotations into `<g id="annotations">`, the title into `<g id="title-block">` — rather than appending them all as flat siblings.

**Grouping strategy:** group by editorial meaning, not rendering order. An infographic has: title area, chart body, annotations, source/method note. These should be separate named `<g>` elements regardless of how D3 structures them internally.

---

## 2. Text: `<text>` vs. Outlines

This is the most consequential editability decision.

**Keep text as `<text>` elements whenever the infographic contains more than a few words.** Converting text to outlines (`Type > Create Outlines` in Illustrator, or setting fonts to "Convert to Outlines" on export) destroys editability, makes text inaccessible to screen readers and SEO, and significantly increases file size. A label that is a `<text>` element with a few attributes becomes a complex path array when outlined.

**When to convert:** logos and display type where exact rendering across systems matters more than editability. Not infographic body text, axis labels, annotations, or titles.

**The font portability trade-off:** `<text>` elements reference fonts that must be available in the receiving environment. For D3-generated SVG meant for Illustrator editing, this means either using system fonts (which may substitute), embedding web fonts as WOFF, or accepting that the Illustrator editor will need the correct font installed. For a brutalist design system with a fixed, specified font stack, font availability is controlled by the DESIGN.md — use whatever those fonts are and document the requirement.

**Typography-specific:** the `text-anchor` and `dominant-baseline` attributes control text alignment within `<text>` elements. These should be explicit rather than relying on Illustrator's interpretation. Rotated axis labels in D3 often use `transform="rotate(-90)"` on a text element — this round-trips poorly into Illustrator and should be handled via `writing-mode` or avoided in favor of horizontal labels where the design allows.

**The `text-anchor` export mismatch:** Illustrator does not export the `text-anchor` attribute when saving SVG. Instead, it calculates the physical bounding box of the text and writes absolute `x` coordinates directly on the `<text>` element. This means center-aligned text authored in Illustrator loses its `text-anchor="middle"` property on export and behaves as left-aligned when manipulated programmatically. Conversely, D3-generated SVG with `text-anchor="middle"` may render differently than expected when opened in Illustrator. Always verify label alignment in both environments when a pipeline crosses both directions.

**The `<tspan>` whitespace collapse bug:** when a D3 text-wrapping function generates multiple `<tspan>` elements, any whitespace or line breaks between them in the XML source is collapsed to a single space by the browser renderer. With `text-anchor: end` applied, this hidden whitespace character causes horizontal alignment shifts — the text appears offset to the left by the width of a space character. The fix is to minify the markup between `<tspan>` tags, eliminating all whitespace in the source. This is a production bug, not a rendering edge case.

---

## 3. Styling: Presentation Attributes vs. CSS

This is the clearest best-practice split in the literature, with a direct practical answer for Illustrator editability.

**Use presentation attributes for Illustrator-destined SVG.** Presentation attributes are visual styles applied directly as element attributes: `<path fill="#c0392b" stroke="none"/>`. They sit at the bottom of the CSS specificity hierarchy, meaning any CSS rule can override them. They are the most flexible for subsequent editing and the most reliable for Illustrator import.

The three options compared:
- **Presentation attributes** (`fill="#c0392b"`) — easiest to override with CSS, most reliable in Illustrator, best for programmatic SVG destined for design tool editing
- **Inline styles** (`style="fill: #c0392b"`) — override presentation attributes, more specific, used by design tools; Illustrator CS+ exports these by default; risk of class name conflicts when multiple SVGs appear on the same page
- **Internal CSS / `<style>` block** — Illustrator's default export uses generic class names (`.st0`, `.st1`) that will collide with other Illustrator-exported SVGs on the same page, causing visual corruption

For D3-generated SVG: D3 applies styles via `.attr("fill", ...)` which writes presentation attributes — this is already the correct behavior. D3's `.style("fill", ...)` writes inline styles, which should be avoided for Illustrator-destined output.

---

## 4. Clipping Masks and `<clipPath>`

This is the primary source of SVG-to-Illustrator friction and the most common complaint in production workflows.

**D3 routinely generates nested clipping masks.** The standard D3 pattern clips the chart area to prevent marks from rendering outside the axes — implemented as a `<clipPath>` element in `<defs>` referencing a rectangle, applied to the chart group. When opened in Illustrator, this produces "a string of Groups, Clip Groups, and Clipping Paths going on to infinity" (a practitioner's direct description). The visual result is correct but the structure is unusable for editing.

**The Illustrator workaround:** select the entire layer, then `Object > Clipping Mask > Release` (⌘⌥7) repeatedly until all clip groups are gone. This removes the clipping structure without affecting the visual content, producing flat editable paths. This is necessary cleanup after every D3 SVG import.

**The structural warning:** Illustrator does not correctly handle SVG `<mask>` elements (as opposed to `<clipPath>`). The browser renders masks correctly; Illustrator renders them incorrectly or ignores them. Use `<clipPath>` rather than `<mask>` for any SVG intended for Illustrator editing.

**The roundtrip warning:** saving an SVG with clipping paths back out of Illustrator generates the warning "Clipping will be lost on roundtrip to Tiny." This is Illustrator confirming that SVG is not its native format and that clipping information degrades on re-export. Save as `.ai` after importing and editing. Never re-export to SVG from Illustrator if you intend to re-import.

**The exponential nesting bug:** this is the most dangerous failure mode for iterative workflows. Each export-import cycle through Illustrator compounds the clipping group nesting. A clean `<g clip-path="url(#clip)">` becomes three levels of nested groups after one cycle, five levels after two cycles, and so on. Eventually Illustrator throws "There are too many nested groups than allowed" and the file fails to open. The fix is to run SVGO or the VectorFirstAid plugin to flatten redundant groups before re-importing — but the real fix is not re-importing at all. Save as `.ai` after the first import and work there.

**Design implication for brutalist infographics:** if the design aesthetic does not require marks to be clipped to the chart boundary (because the layout is controlled and marks don't run over), the D3 clipPath can be omitted entirely, producing cleaner SVG. A brutalist design with fixed, constrained data ranges often doesn't need axis clipping at all.

---

## 5. `viewBox`, Dimensions, and Coordinate Systems

**Always include a `viewBox`.** Without it, SVG cannot scale responsively. SVGO's default configuration removes `viewBox` — this must be disabled (`removeViewBox: false`) for any infographic SVG.

**The viewBox / width-height relationship:** Illustrator's artboard size maps directly to the SVG `viewBox` dimensions on export. For programmatically generated SVG, the convention is: set `viewBox="0 0 width height"` with the same values as the explicit `width` and `height` attributes. The explicit dimensions define the default pixel rendering size; the `viewBox` defines the internal coordinate system.

For infographics destined for Illustrator editing, a large integer coordinate space (960×960 or similar) avoids floating-point path coordinates that bloat the file and reduce precision. Illustrator internally scales its coordinate system from the `viewBox` dimensions — a very large or very small `viewBox` relative to the `width`/`height` can produce unexpected scaling on import.

**D3's margin convention:** D3 charts define `width` and `height` as the inner chart area, then add margins to get the outer SVG dimensions. The SVG element should be sized to the outer dimensions (`width + margin.left + margin.right`), with the inner chart `<g>` translated by `(margin.left, margin.top)`. This produces a single clean translate at the chart group level, which Illustrator handles correctly.

**Integer coordinates:** path data with decimal precision (8 or 12 decimal places, which D3 can produce) makes SVG files larger and harder to inspect. D3's scale functions by default produce floating-point output. For Illustrator-editable SVG, rounding to 1–2 decimal places is sufficient for infographic precision and dramatically reduces file clutter.

**The DPI mismatch:** Illustrator uses a legacy internal resolution of 72 DPI (1 px = 1 point = 1/72 inch). Modern browsers, the SVG 2.0 spec, and most other tools use 96 DPI (1 px = 1/96 inch). This causes a systematic scaling discrepancy when moving between the two environments. D3/browser SVG opened in Illustrator renders 33% too large; Illustrator SVG opened in a browser renders 25% too small. For screen-only infographics this is usually invisible because both environments scale to the viewport. For print-destined work it is critical: always define physical units (`mm`, `in`) in the root `<svg>` element rather than relying on unitless pixel values when the output has a physical size requirement. Test with a known-size rectangle — a 100×100 box — before building a print pipeline.

---

## 6. IDs, Classes, and Naming

**IDs map to group/element names in Illustrator.** When Illustrator imports SVG, the `id` attribute of `<g>` elements becomes the group name visible in the Layers panel. This is the primary mechanism for making programmatic SVG navigable for a designer.

**Naming rules:**
- Use alphanumeric characters and hyphens only — no spaces, underscores work but hyphens are conventional in SVG/CSS
- First character must be a letter, not a number
- Names should be semantic: `chart-bars`, `x-axis-labels`, `chart-title`, `annotation-gdp-peak` — not `g4`, `layer1`, or D3's default empty string

**The class-name collision problem:** Illustrator's internal CSS export uses generic class names (`.st0`, `.st1`, `.st2`...) scoped to nothing. If two Illustrator-exported SVGs appear on the same page, their class names will collide and whichever loads last will override the other's styles. This is a known production failure mode. The fix: use presentation attributes rather than Illustrator-style internal CSS, or scope all class names with a unique prefix.

**ID character escaping:** Illustrator silently mangles IDs that violate XML naming rules. An ID starting with a number — `1st-floor` — becomes `_x31_st-floor` on export, because XML IDs cannot begin with a digit. Spaces become underscores. Special characters become Unicode escape sequences. For D3-generated SVGs, always ensure IDs begin with a letter and contain only alphanumeric characters and hyphens. The slug pattern (`id="bar-california-2025"`) is safe; `id="1-california"` or `id="bar california"` will be silently corrupted.

**The `data-name` dual-attribute strategy:** when Illustrator encounters duplicate group names, it appends a numeric suffix to the `id` (`id="item_1"`, `id="item_2"`) but preserves the original human-readable name in a `data-name` attribute (`data-name="item"`). This dual-attribute pattern can be used intentionally: set `id` for unique programmatic targeting and `data-name` for the human-readable label visible in Illustrator's workspace. Collective CSS selection via `[data-name="item"]` then works across all instances without ID conflicts.

**For D3:** D3 assigns classes (`.bar`, `.line`, `.tick`, `.domain`) for CSS targeting. These are functional names for JavaScript/CSS, not editorial names for Illustrator. The solution is to use explicit `id` attributes on groups for Illustrator navigability while keeping D3's functional class names for code targeting — the two naming systems serve different purposes and can coexist.

---

## 7. `<defs>`, `<symbol>`, and Reuse

**`<defs>`** is the SVG container for elements that are defined but not rendered directly — gradients, clip paths, filters, reusable shapes. Anything in `<defs>` is invisible until referenced by another element.

**`<symbol>`** is `<defs>` with its own `viewBox` — a defined, reusable shape unit with its own coordinate system, instantiated with `<use>`. Illustrator symbols convert to SVG symbols automatically on export, and SVG symbols import as Illustrator symbols — this is one of the cleanest round-trip behaviors in the Illustrator/SVG relationship.

**`<use>`** references any element by ID. For brutalist infographic systems with repeated marks (identical icon shapes used at multiple data points), `<defs>` + `<symbol>` + `<use>` is the correct pattern — define once, instantiate many times.

**What Illustrator handles cleanly:** gradients in `<defs>`, `<symbol>` elements (converted to Illustrator symbols), `<clipPath>` elements (with the clipping mask release caveat above).

**What Illustrator handles poorly:** `<mask>` elements (visual corruption), `<filter>` elements with complex SVG filter primitives (partially supported, behavior varies by version), `<use>` elements referencing external files (must be self-contained).

---

## 8. What Illustrator Destroys on Import

Summarizing confirmed failure modes:

- **`<mask>` elements:** not correctly interpreted; use `<clipPath>` instead
- **Nested clipping masks:** renders correctly but produces uneditable layer structure; release all clipping masks after import
- **Text broken into individual letters:** happens when SVG is printed to PDF via Chrome and then opened in Illustrator; each letter becomes a separate path with no word structure
- **SVG filters (`<filter>`):** partial support; complex filter chains may not render correctly
- **`<use>` referencing external files:** must inline all referenced content
- **Embedded fonts declared via `@font-face` in `<style>`:** may or may not substitute depending on Illustrator version and system font availability
- **Complex `transform` stacks:** renders correctly but produces confusing coordinate systems in the Layers panel; flatten transforms where possible before Illustrator import
- **Opacity compounding:** applying both `opacity="0.5"` and `fill-opacity="0.5"` on the same element causes the values to multiply (resulting in 25% opacity rather than 50%) or in some Illustrator versions causes the path to rasterize into a static pixel graphic. Use one opacity mechanism per element — either `opacity` for the whole element or `fill-opacity`/`stroke-opacity` for channel-specific control, never both simultaneously.

---

## 9. Post-Processing: SVGO

**SVGO** (SVG Optimizer, Node.js-based) is the standard tool for cleaning programmatically generated SVG. It removes editor metadata, comments, redundant attributes, unused `<defs>`, and excessive decimal precision. Typical reduction from D3 or Illustrator output: 30–70%.

**For editability-destined SVG, configure SVGO conservatively:**
- `removeViewBox: false` — essential; do not remove
- `cleanupIDs: false` or configure to preserve meaningful IDs — auto-generated short IDs break Illustrator navigability
- `collapseGroups: false` — preserving named groups is the editorial structure
- `removeTitle: false` — titles contribute to accessibility
- `convertShapeToPath: false` — keep `<rect>`, `<circle>`, `<line>` as semantic elements rather than converting to paths

**SVGO default settings are optimized for web delivery, not Illustrator editability.** Running SVGO with defaults on an infographic SVG intended for Illustrator will strip the named group structure, collapse groups, and shorten IDs — destroying exactly what makes the file editable.

**The two-audience problem:** a single SVG file cannot simultaneously be optimized for web delivery (minimal, short IDs, collapsed structure) and for Illustrator editing (semantic names, preserved groups, readable structure). The practical solution is two outputs: a structured source SVG for editing, and an SVGO-processed delivery SVG for production.

---

## 10. Practical Checklist for Brutalist D3 Infographic SVG

**Structure**
- Top-level `<svg>` has explicit `width`, `height`, and `viewBox` with integer coordinates
- `viewBox` uses the full outer dimensions including margins
- One `<g id="chart">` wrapping all chart content, translated by `(margin.left, margin.top)`
- Editorial groups explicitly named: `<g id="bars">`, `<g id="x-axis">`, `<g id="annotations">`, `<g id="title-block">`, `<g id="source-note">`

**Text**
- All text as `<text>` elements, never converted to paths
- `text-anchor` and `dominant-baseline` set explicitly
- No rotated axis labels unless unavoidable
- Font family matches DESIGN.md specification

**Styling**
- All color applied as presentation attributes (`fill`, `stroke`, `stroke-width` on elements directly), not via `style=""` or internal CSS class blocks
- No D3 `.style()` calls on production SVG output; use `.attr()` for all visual properties

**Clipping**
- No `<clipPath>` unless the design genuinely requires bounded rendering
- If `<clipPath>` is present, it is documented in a comment: `<!-- Release clipping mask on Illustrator import: Object > Clipping Mask > Release -->`
- No `<mask>` elements in Illustrator-destined SVG

**IDs and naming**
- Every `<g>` element has a meaningful semantic `id`
- No auto-generated IDs (`g4523`, `path23`)
- Class names prefixed to avoid collision if multiple SVGs will coexist on a page

**Post-processing**
- Source SVG preserved as-is for Illustrator editing
- Separate SVGO-processed version for web delivery, configured to preserve `viewBox`, groups, and IDs
- Illustrator `.ai` saved after any manual correction; never re-export SVG from Illustrator
- When exporting from Illustrator, set coordinate precision to 3+ decimal places — Illustrator's default of 1 decimal place causes visible rounding distortion on curved paths

---

## Sources and Credibility Notes

**Confirmed Illustrator behavior (forum/practitioner):** named `<g>` elements cannot be forced to appear as Illustrator layers on import — they always land as groups inside Layer 1. This is a structural limitation of how Illustrator reads SVG, confirmed by Adobe community experts.

**Confirmed D3 pattern issues (practitioner):** D3's clip path pattern produces Groups, Clip Groups, and Clipping Paths that require manual release in Illustrator. Direct quote from a practitioner who worked through the workflow: "a nightmare to work with in Illustrator."

**ClipPath exponential nesting bug:** documented in multiple Adobe community threads; the compounding behavior on each export-import cycle is a confirmed structural failure, not an edge case. VectorFirstAid plugin cited as the practical fix.

**DPI mismatch (72 vs 96):** technically verified against Illustrator's legacy resolution and the W3C SVG 2.0 specification. The 25%/33% scaling discrepancies are mathematically derivable and practically confirmed by practitioners working across environments.

**SVG `<mask>` vs. `<clipPath>` in Illustrator:** confirmed failure mode in multiple community reports; `<clipPath>` is supported, `<mask>` is not correctly interpreted.

**`text-anchor` export mismatch:** confirmed practitioner finding — Illustrator bakes absolute coordinates rather than exporting the `text-anchor` attribute. Bidirectional pipeline implications confirmed.

**`<tspan>` whitespace collapse bug:** confirmed production bug affecting right-aligned wrapped text; fix is markup minification between `<tspan>` elements.

**ID character escaping:** confirmed Illustrator behavior — IDs starting with numbers become `_x31_...` Unicode escapes. `data-name` dual-attribute strategy is a documented Illustrator export pattern.

**Opacity compounding:** confirmed failure mode; simultaneous `opacity` + `fill-opacity` on same element produces unexpected compound values or rasterization.

**Coordinate precision:** confirmed Illustrator behavior — default 1-decimal precision causes rounding distortion; 3+ decimal places required for curved path fidelity.

**Styling approach (specification + practitioner consensus):** presentation attributes are the most reliable for Illustrator import and downstream CSS overriding; internal CSS with generic class names (.st0, .st1) creates known collision failures when multiple SVGs are on the same page.

**SVGO configuration for editability:** practitioner consensus from multiple sources that default SVGO settings are destructive to editorial SVG structure; must be configured conservatively for infographic work.
