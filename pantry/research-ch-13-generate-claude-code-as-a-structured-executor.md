# Research: Chapter 13 — Generate: Claude Code as a Structured Executor
## Brutalist SVG x Claude: Infographic Design and AI-Assisted Production

**Chapter one-line:** Students learn to use Claude Code as a structured executor of the design specification — not as a creative collaborator — and to enforce the CLAUDE.md constraints at every generation step.
**Research date:** 2026-05-30

---

## 1. Primary Sources

### Foundational papers and texts
- **Anthropic. _Claude Code documentation_ (current documentation). Anthropic Docs.** Current source for Claude Code workflows and constraints. High aging risk; verify before each course offering.
- **D3 Team. _D3 selections and selection.join documentation_ (current documentation). d3js.org.** Primary implementation reference for D3 lifecycle patterns in generated SVG.
- **Sculley et al.. _Hidden Technical Debt in Machine Learning Systems_ (2015). NeurIPS.** Useful analogy for production pipeline discipline: unmanaged generated artifacts create future maintenance debt.
- **W3C SVG Working Group. _Scalable Vector Graphics (SVG) 2 Specification_ (current specification). W3C.** Authoritative source for SVG elements, grouping, text, paths, presentation attributes, and document structure. Essential for chapters on SVG as a design medium and Illustrator editability.
- **Eisenberg and Bellamy-Royds. _SVG Essentials_ (2014 / 2018). O’Reilly.** Practical source for reading and authoring SVG structure. Helpful for learners who know SVG exists but have never inspected the DOM.

### Key empirical cases
- **Science Communication infographic failure/rebuild.** Use a published or instructor-provided infographic from this domain and ask what claim the visual structure makes before assessing whether the underlying data are true. This keeps the chapter grounded in the book's relationship between fact, form, and judgment.
- **Specification-less AI SVG generation.** Give Claude Code or another coding agent a vague request, then compare the generated SVG against a design specification. The contrast is appropriate because the target reader has likely already seen polished but indefensible AI-generated graphics.
- **Student terminal project artifact.** Each chapter should add one decision to the same final infographic package: claim, encoding, hierarchy, annotation, layout, implementation, verification, or disclosure. This turns abstract design theory into cumulative production practice.
- **Instructor production repository.** Use an existing SVG/D3 project with naming, grouping, and handoff defects so students audit real files rather than pristine examples.

---

## 2. The Core Concept — State of the Field

### What is settled
Claude Code and similar agents are strongest as structured executors when the design intelligence layer is already specified. Relevant sources for this settled ground include Anthropic, D3 Team, Sculley et al..

### What is disputed
Whether the agent is a creative collaborator or executor depends on workflow, but this book deliberately constrains it to protect the design layer. The chapter should distinguish evidence-based design rules from local editorial judgment, especially when examples depend on audience, medium, or toolchain.

### What has changed recently (last 5 years)
Agentic code generation is increasingly capable, making constraint files and verification checklists more important, not less. High-risk operational details include Claude Code behavior, D3 examples, WCAG guidance, Illustrator import behavior, and Node/SVG conversion scripts; these should be verified immediately before publication or course use.

---

## 3. Application Domain Examples

- **Science Communication infographic failure/rebuild.** Use a published or instructor-provided infographic from this domain and ask what claim the visual structure makes before assessing whether the underlying data are true. This keeps the chapter grounded in the book's relationship between fact, form, and judgment.
- **Specification-less AI SVG generation.** Give Claude Code or another coding agent a vague request, then compare the generated SVG against a design specification. The contrast is appropriate because the target reader has likely already seen polished but indefensible AI-generated graphics.
- **Student terminal project artifact.** Each chapter should add one decision to the same final infographic package: claim, encoding, hierarchy, annotation, layout, implementation, verification, or disclosure. This turns abstract design theory into cumulative production practice.
- **Instructor production repository.** Use an existing SVG/D3 project with naming, grouping, and handoff defects so students audit real files rather than pristine examples.

---

## 4. The Book's Thesis Connection

This chapter serves the book's thesis by isolating one part of the design intelligence layer: **Claude Code as constrained execution layer**. The student may use AI to generate alternatives, code, SVG scaffolds, labels, checklists, or test commands, but the student must supply the decision standard. That standard includes what the visual is claiming, which encoding is appropriate, which information is excluded, which accessibility constraint applies, and what makes the result defensible in review. The chapter should make clear that the AI execution layer is useful only after the human design layer is populated.

Evidence from visualization research supports the thesis because perceptual accuracy, cognitive load, visual hierarchy, and accessibility are not visible from the SVG's surface polish. The human must know enough to distrust a plausible graphic.

---

## 5. The AI Wayback Machine — Candidate Figures

- **Mike Bostock.** Substantive connection: directly connected to Claude Code as constrained execution layer through visual communication, design systems, information graphics, computing, or production practice. Selection fit: historically meaningful and Wikipedia-accessible; verify exact page title before final Wayback pass. Example prompt: "Explain how Mike Bostock's work helps an engineer avoid a polished but indefensible infographic."
- **Ben Shneiderman.** Substantive connection: offers a complementary lineage for this chapter's principle, especially the relation between visual form and human interpretation. Selection fit: useful for balancing discipline or era. Example prompt: "Connect Ben Shneiderman to one design decision in a Brutalist SVG infographic."
- **Leland Wilkinson.** Substantive connection: gives an alternate anchor if the chapter needs a more visual, computational, or editorial figure. Selection fit: check diversity balance across the whole book before selection. Example prompt: "Show how Leland Wilkinson's work anticipates the design intelligence layer this chapter teaches."

Diversity note: the full set risks over-representing European and North American visualization/design figures. The Wayback pass should deliberately include women, non-US figures, and practitioners from science communication and public-interest visualization where the substantive connection is strong.

---

## 6. Pedagogical Delivery Research

Teach this chapter through failure-first comparison. The target reader can already ask an AI tool to produce SVG, so the instructional sequence should begin with a plausible AI-generated or professionally polished failure, then name the principle that explains the failure, then rebuild the artifact under constraint. Common misconceptions: polish equals correctness, prompts replace design specifications, and AI output can be judged by appearance alone. Students understand Claude Code as constrained execution layer when they can defend a design choice in language that survives a skeptical review, not when they can merely reproduce a pretty result.

---

## 7. Representation and Display Research

Special display required: a three-representation production display showing source/specification, generated SVG structure, and production/handoff artifact. Include one worked example with columns for design intent, generated code structure, verification finding, correction, and remaining risk.

---

## 8. Open Questions and Research Gaps

- **Current tool behavior.** Claude Code, D3, Illustrator, Inkscape, and `svg-to-png.mjs` examples must be tested in the live environment before drafting final instructions.
- **Case permissions.** Published infographics used as critique cases may require redrawing, excerpting, or replacement with instructor-created equivalents for rights reasons.
- **Accessibility depth.** WCAG contrast is necessary but not the whole of accessible graphics; tactile graphics, screen-reader SVG semantics, and full alt-text workflows are out of scope but should be acknowledged.
- **Companion volume boundary.** The relationship to *Brutalist D3 x Claude* must be kept clear: this book teaches infographic design intelligence and production packages, not the full 61-chart pantry.

---

## 9. Sourcing Notes

Prioritize primary or canonical sources where possible: Cleveland and McGill 1984; Bertin 1967/1983; Paivio 1986; Sweller 1988; Bateman et al. 2010; Borkin et al. 2013; W3C SVG and WCAG recommendations; D3 and Anthropic official documentation for current implementation details. Documentation sources are likely to age within 3 years and should carry access dates in final chapter drafts.
