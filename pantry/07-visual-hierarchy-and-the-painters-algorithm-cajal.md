# CAJAL — Chapter 7: Visual Hierarchy and the Painter's Algorithm

## Figure 7.1 — The structural conflict, resolved by two axes
- **Concept:** SVG paint order (back-to-front by depth) and editorial grouping (by-kind by meaning) are two different organizations of the same file — reconciled by making depth the OUTER axis and meaning the INNER axis of one tree.
- **Type:** Side-by-side comparison + reconciliation diagram.
- **Shows:** Left = paint-order stack (background → ... → titles, the depth axis). Right = editorial layers each holding semantic sub-groups. The collision point where naive editorial grouping would paint a label behind its mark.
- **Scope:** One figure's layer tree; the depth/meaning conflict.
- **Red accent:** The collision marker — the annotation that slides behind the cell when editorial order fights paint order.
