# CAJAL — Chapter 12 figures

## Fig 12-01 — The Audit phase gate
- **Concept:** Audit is a binary gate, not a courtesy. Three artifacts (asset inventory, convention inventory, gap map) plus a populated Intent Layer must all exist before generation begins; one unmet condition holds the gate CLOSED.
- **Type:** Gate / flow diagram (conditions feeding a single barrier).
- **Shows:** Four input conditions (Intent populated, asset inventory, convention inventory, gap map) flowing into a gate; the gate's binary state; the blocking condition (incomplete DESIGN.md) that keeps it closed; the "Generate" phase walled off behind it.
- **Scope:** Single panel, left-to-right. Inputs as stacked panels, gate as central barrier, downstream Generate phase greyed/blocked.
- **Red accent (ONE):** The CLOSED gate bar itself — the single barrier that stops the flow. Everything else ink/grey/ochre.

## Fig 12-02 — Source of truth vs. derived artifact
- **Concept:** Editing a derived artifact (PNG) fixes nothing; the SVG is the source. The audit's job is to mark each file SOURCE / DERIVED / UNKNOWN before any one is privileged.
- **Type:** Provenance tree / classification diagram.
- **Shows:** SVG (source) → PNG (derived); a quarantined unknown-provenance file; the futile "fix the PNG" edit shown as a dead end.
- **Scope:** Single panel; source on left, derived downstream, quarantine isolated.
- **Red accent (ONE):** The "do not build on" quarantine marker on the unknown-provenance file.
