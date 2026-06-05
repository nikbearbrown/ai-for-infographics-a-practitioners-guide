# CAJAL Figure Report — Chapter 4

**Figures: 1**

## Fig 4.1 — One File, Three Readers
- **Concept:** The same SVG means three incompatible things — to a browser it is a rendering instruction (does the raster match?), to a code generator it is a serialization target (what is easy to emit?), to a designer it is a structured document (named layers, live text). Only the human reconciles "renders correctly" with "stays editable."
- **Type:** Three-column comparison, one shared file at the top branching down to three reader-views, each labeled with what that reader cares about and what it ignores.
- **Shows:** Top: one `<svg>` file. Three columns — BROWSER (cares: valid raster; ignores: group names, live text), GENERATOR (cares: easy to produce; ignores: editability), DESIGNER (cares: named layers, live text; needs: semantic ids). A reconciliation band below names the human judgment that satisfies all three.
- **Scope:** Chapter 4 "SVG means three different things." Anchors the chapter's central frame.
- **Red-accent element:** The reconciliation band — the irreducibly human judgment that the browser, generator, and designer cannot each supply alone.
