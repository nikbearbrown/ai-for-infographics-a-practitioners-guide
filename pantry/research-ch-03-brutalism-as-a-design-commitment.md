# Research: Chapter 03 — Brutalism as a Design Commitment
## Brutalist SVG x Claude: Infographic Design and AI-Assisted Production

**Chapter one-line:** Students learn that Brutalism in infographic design is not a visual style but a set of commitments — exposed structure, functional marks, honest hierarchy — that map directly onto the perceptual science from Chapter 2.
**Research date:** 2026-05-30

---

## 1. Primary Sources

### Foundational papers and texts
- **Bateman et al.. _Useful Junk? The Effects of Visual Embellishment on Comprehension and Memorability of Charts_ (2010). CHI.** Central source for the contested embellishment claim. The chapter should teach the actual finding: meaningful embellishment may improve recall without necessarily harming comprehension; arbitrary decoration remains risky.
- **Tufte. _The Visual Display of Quantitative Information_ (1983 / 2001). Graphics Press.** Canonical minimalist position and source of data-ink thinking. Useful as a foil for Brutalism: this book is not anti-ornament by reflex, but anti-nonfunctional marks.
- **Holmes. _Designer’s Guide to Creating Charts and Diagrams_ (1984). Watson-Guptill.** Historical anchor for pictorial chart design and the debate around illustrative embellishment.
- **Lupton. _Thinking with Type_ (2010 / later editions). Princeton Architectural Press.** Accessible typography source for hierarchy, role, spacing, and typographic discipline.
- **Ware. _Information Visualization: Perception for Design_ (2020, 4th ed.). Morgan Kaufmann.** Bridges perceptual science and applied visualization design. Supports color, hierarchy, and attention claims.

### Key empirical cases
- **Ai/Ml System Performance infographic failure/rebuild.** Use a published or instructor-provided infographic from this domain and ask what claim the visual structure makes before assessing whether the underlying data are true. This keeps the chapter grounded in the book's relationship between fact, form, and judgment.
- **Specification-less AI SVG generation.** Give Claude Code or another coding agent a vague request, then compare the generated SVG against a design specification. The contrast is appropriate because the target reader has likely already seen polished but indefensible AI-generated graphics.
- **Student terminal project artifact.** Each chapter should add one decision to the same final infographic package: claim, encoding, hierarchy, annotation, layout, implementation, verification, or disclosure. This turns abstract design theory into cumulative production practice.

---

## 2. The Core Concept — State of the Field

### What is settled
Design commitments can be evaluated against communicative function; decoration is not automatically bad, but nonfunctional marks add risk. Relevant sources for this settled ground include Bateman et al., Tufte, Holmes.

### What is disputed
Brutalism can be mistaken for an aesthetic style; the chapter must defend it as a functional discipline, not a taste claim. The chapter should distinguish evidence-based design rules from local editorial judgment, especially when examples depend on audience, medium, or toolchain.

### What has changed recently (last 5 years)
Generative tools have revived debates about style versus system, because prompts can imitate surfaces without preserving the underlying design commitments. High-risk operational details include Claude Code behavior, D3 examples, WCAG guidance, Illustrator import behavior, and Node/SVG conversion scripts; these should be verified immediately before publication or course use.

---

## 3. Application Domain Examples

- **Ai/Ml System Performance infographic failure/rebuild.** Use a published or instructor-provided infographic from this domain and ask what claim the visual structure makes before assessing whether the underlying data are true. This keeps the chapter grounded in the book's relationship between fact, form, and judgment.
- **Specification-less AI SVG generation.** Give Claude Code or another coding agent a vague request, then compare the generated SVG against a design specification. The contrast is appropriate because the target reader has likely already seen polished but indefensible AI-generated graphics.
- **Student terminal project artifact.** Each chapter should add one decision to the same final infographic package: claim, encoding, hierarchy, annotation, layout, implementation, verification, or disclosure. This turns abstract design theory into cumulative production practice.

---

## 4. The Book's Thesis Connection

This chapter serves the book's thesis by isolating one part of the design intelligence layer: **Brutalism as exposed structure and honest hierarchy**. The student may use AI to generate alternatives, code, SVG scaffolds, labels, checklists, or test commands, but the student must supply the decision standard. That standard includes what the visual is claiming, which encoding is appropriate, which information is excluded, which accessibility constraint applies, and what makes the result defensible in review. The chapter should make clear that the AI execution layer is useful only after the human design layer is populated.

Evidence from visualization research supports the thesis because perceptual accuracy, cognitive load, visual hierarchy, and accessibility are not visible from the SVG's surface polish. The human must know enough to distrust a plausible graphic.

---

## 5. The AI Wayback Machine — Candidate Figures

- **Alison Smithson.** Substantive connection: directly connected to Brutalism as exposed structure and honest hierarchy through visual communication, design systems, information graphics, computing, or production practice. Selection fit: historically meaningful and Wikipedia-accessible; verify exact page title before final Wayback pass. Example prompt: "Explain how Alison Smithson's work helps an engineer avoid a polished but indefensible infographic."
- **Nigel Holmes.** Substantive connection: offers a complementary lineage for this chapter's principle, especially the relation between visual form and human interpretation. Selection fit: useful for balancing discipline or era. Example prompt: "Connect Nigel Holmes to one design decision in a Brutalist SVG infographic."
- **Edward Tufte.** Substantive connection: gives an alternate anchor if the chapter needs a more visual, computational, or editorial figure. Selection fit: check diversity balance across the whole book before selection. Example prompt: "Show how Edward Tufte's work anticipates the design intelligence layer this chapter teaches."

Diversity note: the full set risks over-representing European and North American visualization/design figures. The Wayback pass should deliberately include women, non-US figures, and practitioners from science communication and public-interest visualization where the substantive connection is strong.

---

## 6. Pedagogical Delivery Research

Teach this chapter through failure-first comparison. The target reader can already ask an AI tool to produce SVG, so the instructional sequence should begin with a plausible AI-generated or professionally polished failure, then name the principle that explains the failure, then rebuild the artifact under constraint. Common misconceptions: polish equals correctness, prompts replace design specifications, and AI output can be judged by appearance alone. Students understand Brutalism as exposed structure and honest hierarchy when they can defend a design choice in language that survives a skeptical review, not when they can merely reproduce a pretty result.

---

## 7. Representation and Display Research

Special display required: side-by-side comparison panels. Show the misleading or weak version next to the corrected/specification-driven version, with the same data or concept held constant so the visual decision is isolated.

---

## 8. Open Questions and Research Gaps

- **Current tool behavior.** Claude Code, D3, Illustrator, Inkscape, and `svg-to-png.mjs` examples must be tested in the live environment before drafting final instructions.
- **Case permissions.** Published infographics used as critique cases may require redrawing, excerpting, or replacement with instructor-created equivalents for rights reasons.
- **Accessibility depth.** WCAG contrast is necessary but not the whole of accessible graphics; tactile graphics, screen-reader SVG semantics, and full alt-text workflows are out of scope but should be acknowledged.
- **Companion volume boundary.** The relationship to *Brutalist D3 x Claude* must be kept clear: this book teaches infographic design intelligence and production packages, not the full 61-chart pantry.

---

## 9. Sourcing Notes

Prioritize primary or canonical sources where possible: Cleveland and McGill 1984; Bertin 1967/1983; Paivio 1986; Sweller 1988; Bateman et al. 2010; Borkin et al. 2013; W3C SVG and WCAG recommendations; D3 and Anthropic official documentation for current implementation details. Documentation sources are likely to age within 3 years and should carry access dates in final chapter drafts.
