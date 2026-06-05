# CAJAL — Chapter 14 figures

## Fig 14-01 — Browser-correct vs. production-editable: the gap pipelines skip
- **Concept:** A browser-correct SVG is NOT a production asset until it survives a round trip through a vector editor and comes out editable. Most pipelines stop at "it renders"; the Verify + Handoff phases close the gap by doing the edits a production team will need.
- **Type:** Two-state comparison with a bridging step (the round trip).
- **Shows:** Left — "browser-correct" SVG (renders fine, but drifted text, fighting clip, buried groups lurk). Center — the Illustrator/Inkscape round trip (Open not Place, release clips, reconcile names, fix anchor drift). Right — "production-editable" .ai with named clip-free layers. The middle bridge is the step pipelines skip.
- **Scope:** Single panel, left-to-right; the skipped bridge visually distinct.
- **Red accent (ONE):** The editable-layers result on the right — the production-editable named-layer stack that the round trip produces.

## Fig 14-02 — The one-way ticket: exponential nesting on re-export
- **Concept:** Illustrator is a one-way ticket. Each SVG↔Illustrator round trip re-wraps groups in new anonymous parents and re-introduces clips; nesting compounds roughly geometrically until the structure is unnavigable. Fix the spec and regenerate instead.
- **Type:** Comparison of two paths — disciplined (one-way) vs. repeated round trips (nesting growth).
- **Shows:** One-way path: SVG → import once → correct → .ai (clean, shallow nesting). Round-trip path: each cycle adds a wrapper layer, the nest depth growing 1→2→4→8 (anonymous <g> piling up). The "regenerate from spec" loop offered as the cheap alternative.
- **Scope:** Single panel; the geometric nesting shown as growing nested boxes.
- **Red accent (ONE):** The deepest/runaway anonymous-wrapper nest on the round-trip path — the failure being warned against.
