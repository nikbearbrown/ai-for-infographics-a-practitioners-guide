# Research: Chapter 06 — Marks, Channels, and the Grammar of Infographics
## Brutalist SVG x Claude: Infographic Design and AI-Assisted Production

**Chapter one-line:** Students learn to apply Bertin's visual variables and the infographic/dataviz distinction to determine which encoding approach is appropriate for a given concept and audience.
**Research date:** 2026-05-30

---

## 1. Primary Sources

### Foundational papers and texts
- **Bertin. _Semiology of Graphics_ (1967 / English translation 1983). University of Wisconsin Press.** Foundational source for visual variables. Supports the marks-and-channels grammar in Chapter 6.
- **Financial Times Visual Journalism Team. _Visual Vocabulary_ (current public guide). Financial Times.** Practical relationship-first chart selection guide. Use as practitioner support, not as a primary research paper.
- **Wilke. _Fundamentals of Data Visualization_ (2019). O’Reilly.** Modern applied reference on chart selection, color, uncertainty, and common visualization failures.
- **Cleveland and McGill. _Graphical Perception: Theory, Experimentation, and Application to the Development of Graphical Methods_ (1984). Journal of the American Statistical Association.** Primary experimental source for ranking visual channels such as position, length, angle, area, and color. It directly supports the claim that some encodings are more accurate than others, not merely more fashionable.
- **Mackinlay. _Automating the Design of Graphical Presentations of Relational Information_ (1986). ACM Transactions on Graphics.** Foundational work on matching data types and tasks to graphical encodings. Useful for explaining why an AI-generated chart can look plausible while choosing the wrong channel.

### Key empirical cases
- **Climate And Energy Data infographic failure/rebuild.** Use a published or instructor-provided infographic from this domain and ask what claim the visual structure makes before assessing whether the underlying data are true. This keeps the chapter grounded in the book's relationship between fact, form, and judgment.
- **Specification-less AI SVG generation.** Give Claude Code or another coding agent a vague request, then compare the generated SVG against a design specification. The contrast is appropriate because the target reader has likely already seen polished but indefensible AI-generated graphics.
- **Student terminal project artifact.** Each chapter should add one decision to the same final infographic package: claim, encoding, hierarchy, annotation, layout, implementation, verification, or disclosure. This turns abstract design theory into cumulative production practice.

---

## 2. The Core Concept — State of the Field

### What is settled
Marks and channels must be chosen from the relationship in the data or concept, not from the designer’s preferred form. Relevant sources for this settled ground include Bertin, Financial Times Visual Journalism Team, Wilke.

### What is disputed
AI can suggest chart types, but relationship-first selection and audience-specific tradeoffs still require human judgment. The chapter should distinguish evidence-based design rules from local editorial judgment, especially when examples depend on audience, medium, or toolchain.

### What has changed recently (last 5 years)
Chart recommendation tools and LLMs can generate candidates, but relationship-first selection still needs verification against the communicative purpose. High-risk operational details include Claude Code behavior, D3 examples, WCAG guidance, Illustrator import behavior, and Node/SVG conversion scripts; these should be verified immediately before publication or course use.

---

## 3. Application Domain Examples

- **Climate And Energy Data infographic failure/rebuild.** Use a published or instructor-provided infographic from this domain and ask what claim the visual structure makes before assessing whether the underlying data are true. This keeps the chapter grounded in the book's relationship between fact, form, and judgment.
- **Specification-less AI SVG generation.** Give Claude Code or another coding agent a vague request, then compare the generated SVG against a design specification. The contrast is appropriate because the target reader has likely already seen polished but indefensible AI-generated graphics.
- **Student terminal project artifact.** Each chapter should add one decision to the same final infographic package: claim, encoding, hierarchy, annotation, layout, implementation, verification, or disclosure. This turns abstract design theory into cumulative production practice.

---

## 4. The Book's Thesis Connection

This chapter serves the book's thesis by isolating one part of the design intelligence layer: **marks, channels, and relationship-first chart choice**. The student may use AI to generate alternatives, code, SVG scaffolds, labels, checklists, or test commands, but the student must supply the decision standard. That standard includes what the visual is claiming, which encoding is appropriate, which information is excluded, which accessibility constraint applies, and what makes the result defensible in review. The chapter should make clear that the AI execution layer is useful only after the human design layer is populated.

Evidence from visualization research supports the thesis because perceptual accuracy, cognitive load, visual hierarchy, and accessibility are not visible from the SVG's surface polish. The human must know enough to distrust a plausible graphic.

---

## 5. The AI Wayback Machine — Candidate Figures

- **Jacques Bertin.** Substantive connection: directly connected to marks, channels, and relationship-first chart choice through visual communication, design systems, information graphics, computing, or production practice. Selection fit: historically meaningful and Wikipedia-accessible; verify exact page title before final Wayback pass. Example prompt: "Explain how Jacques Bertin's work helps an engineer avoid a polished but indefensible infographic."
- **William Playfair.** Substantive connection: offers a complementary lineage for this chapter's principle, especially the relation between visual form and human interpretation. Selection fit: useful for balancing discipline or era. Example prompt: "Connect William Playfair to one design decision in a Brutalist SVG infographic."
- **Leland Wilkinson.** Substantive connection: gives an alternate anchor if the chapter needs a more visual, computational, or editorial figure. Selection fit: check diversity balance across the whole book before selection. Example prompt: "Show how Leland Wilkinson's work anticipates the design intelligence layer this chapter teaches."

Diversity note: the full set risks over-representing European and North American visualization/design figures. The Wayback pass should deliberately include women, non-US figures, and practitioners from science communication and public-interest visualization where the substantive connection is strong.

---

## 6. Pedagogical Delivery Research

Teach this chapter through failure-first comparison. The target reader can already ask an AI tool to produce SVG, so the instructional sequence should begin with a plausible AI-generated or professionally polished failure, then name the principle that explains the failure, then rebuild the artifact under constraint. Common misconceptions: polish equals correctness, prompts replace design specifications, and AI output can be judged by appearance alone. Students understand marks, channels, and relationship-first chart choice when they can defend a design choice in language that survives a skeptical review, not when they can merely reproduce a pretty result.

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
