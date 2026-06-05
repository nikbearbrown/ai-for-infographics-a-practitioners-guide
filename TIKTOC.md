# Brutalist SVG × Claude: Infographic Design and AI-Assisted Production
## Full TOC Draft — Tic TOC Planning Document

**Working title:** Brutalist SVG × Claude: Infographic Design and AI-Assisted Production
**Series:** AI+1 · Irreducibly Human: What AI Can and Can't Do · Northeastern University College of Engineering
**Author:** Humanitarians AI · ni.brown@neu.edu · Bear Brown & Company
**Document:** Full TOC Draft — all phase outputs compiled
**Version:** 1.0
**Status:** Pre-proposal

---

## Document structure

1. Book Concept and Thesis
2. Learner Profile
3. Book Type and Deployment Specification
4. Field Positioning
5. Three-Act Learning Arc
6. Prerequisite Map
7. Assessment Structure
8. Chapter-by-Chapter TOC
9. Chapter Anatomy Template
10. Case Study and Exercise Strategy
11. Hard Topics, Contested Claims, Aging Risk
12. Market Positioning
13. Feature List
14. Out of Scope
15. Adoption Risk Register
16. Open Questions

---

# PART 1 — BOOK CONCEPT AND THESIS

## Book concept summary

> This book teaches **the design intelligence layer of SVG infographic production — the decisions about visual hierarchy, marks, channels, annotation, and layout that no AI code generator can make without human judgment** — to **engineers, educators, and practitioners who can already use AI tools to write code**, by **building from perceptual and cognitive theory through a complete Brutalist design system to a CLI-driven production pipeline that proves in every chapter which decisions remain irreducibly human**. It fills the gap left by dataviz theory texts (which assume a statistical reader, not a producer) and tool tutorials (which assume a designer, not an engineer). It succeeds if the reader can **construct a complete SVG infographic from a design brief, articulate every visual encoding decision, produce Illustrator-editable output, and defend every judgment in a design review** after completing it.

**One-sentence logline:**
The theory tells you what makes an infographic work; the system tells you how to produce it; the exercises prove which decisions only you can make.

## Central thesis

"This book argues that the design intelligence layer of SVG infographic production — variable selection, visual encoding choice, hierarchy decisions, annotation placement, and layout — currently requires human judgment that no AI code generator can supply, which means that engineers who use AI to generate infographic SVGs without performing the design layer are producing outputs they cannot defend, and this matters because infographics are claims about the world dressed in visual authority."

## Thesis test

The TOC reflects the thesis at every act:

- ACT ONE (Theory): The student encounters the cognitive science that explains why visual encoding choices matter before any tool is introduced. The theory is not decorative — it makes specific, testable predictions about what will work and what will fail. ✓
- ACT TWO (Design System): The student builds the Brutalist design vocabulary — marks, channels, hierarchy, color, typography, annotation, layout — applied to their own candidate infographic. The tool is present but the judgment remains human. ✓
- ACT THREE (Production Pipeline): The student drives a CLI-based production pipeline using Claude Code, defends every design decision to a skeptical reviewer, and produces Illustrator-editable SVG with embedded metadata. The pipeline serves the design intelligence — it does not replace it. ✓

**Thesis test: PASS**

---

# PART 2 — LEARNER PROFILE

## Primary reader

A graduate student, working engineer, or educator who can write Python or JavaScript and has used AI code generation tools (Claude Code, GitHub Copilot, Codex) in a production or research context. They have produced charts. They want to produce infographics. They are not designers by training and do not have access to a design team.

**Specific person:** A second-year MS student in applied AI or data engineering who was asked to produce an explanatory figure for a paper or presentation, used an AI tool to generate the SVG, got an output that looked "pretty but wrong," and wants to understand why — and how to produce something they can actually defend.

## Prior knowledge assumed

- Python or JavaScript fluency
- Basic statistics and probability (not required for theory sections; required for data-encoding examples)
- Some familiarity with SVG as a file format (knows it exists; has not read one carefully)
- Experience using at least one AI code generation tool

## Prior knowledge NOT assumed

- Graphic design training
- CSS or web design experience
- D3.js or any visualization library
- Adobe Illustrator or any vector editing tool
- Formal typography or color theory

## Prior misconceptions

1. "A good-looking infographic is a good infographic" — visual polish and communicative accuracy are orthogonal; embellishment can improve recall while reducing comprehension accuracy
2. "AI generates SVG; I just prompt it" — the design intelligence layer precedes the prompt; a well-specified prompt is the output of design thinking, not a substitute for it
3. "More information in one figure means more value" — cognitive load theory makes this exactly wrong above 4–7 components
4. "The Brutalist aesthetic is a style choice" — it is a set of design commitments that map directly to perceptual science and editorial clarity
5. "SVG editability doesn't matter if the output looks right in the browser" — the production pipeline requires Illustrator-editable SVG; browser rendering is necessary but not sufficient

## Motivation type

Mixed: professional (they need to produce defensible figures for papers, presentations, and deployed products), intellectual (they are skeptical of "AI-generated graphics" and want the underlying logic), and technical (they want to understand the production pipeline as a system, not just use a tool).

The professional motivation is primary. The terminal deliverable is a complete infographic production package for a real domain problem — not a textbook exercise.

---

# PART 3 — BOOK TYPE AND DEPLOYMENT SPECIFICATION

## Book type

**PRIMARY TYPE:** Course textbook — adopted for a semester, chapter = week, read in sequence.

**SECONDARY TYPE:** Practitioner handbook — Acts One and Two are self-contained enough for professional readers who do not need the CLI pipeline (Act Three). Chapters 1–10 constitute a complete design curriculum without a tool dependency.

**NOT:** Field-defining monograph (the field exists; this book teaches it), reference work (the out-of-scope section is too aggressive for a reference), or tool tutorial (the theory chapters are not optional).

## Deployment specification

**Primary adoption context:**
Graduate engineering courses in AI systems, data communication, or responsible AI. 15-week semester. One chapter per week. Target department: College of Engineering, with secondary adoption in Information Science, Computer Science, and Communication programs that offer graduate courses in data visualization or science communication.

**Secondary adoption context:**
Professional development programs, corporate ML training, and science communication workshops for researchers. Chapters 1–10 (Acts One and Two) are the most transferable to non-semester formats. The CLI pipeline (Act Three) works for professional readers with Node.js and Claude Code access.

**What the book is NOT designed for:**
Pure graphic design programs (prerequisites too low; no engineering context); undergraduate courses without coding prerequisites; stand-alone reference use (sequence dependency is too high in Act Three).

**How the TOC signals book type to a faculty reviewer:**
Fifteen chapters, one per week, with explicit act labels (Theory / Design System / Production Pipeline), three milestone deliverables at act transitions, and a terminal project specified in Chapter 15. A faculty member building a 15-week syllabus can map this TOC in under ten minutes.

---

# PART 4 — FIELD POSITIONING

## The positioning statement — consolidated

The competitive landscape has a clean gap:

- Cairo's *The Functional Art* and *How Charts Lie* make the argument for visual honesty and reader-first design. This book assumes those arguments were won and builds the production system.
- Tufte's work establishes the minimalist pole of the debate. This book occupies a different position: not minimalist, not decorative — Brutalist. The Brutalist commitment to exposed structure, functional marks, and honest hierarchy is theoretically grounded, not aesthetic.
- Murray's *Interactive Data Visualization for the Web* covers D3.js for web developers. This book covers SVG infographic production for engineers who use AI code generators — D3 is one tool in the pipeline, not the subject.
- Wilke's *Fundamentals of Data Visualization* covers chart selection and visual encoding comprehensively. This book builds on that foundation and extends it to infographic layout, annotation, AI-assisted production, and Illustrator-editable SVG output.
- Schwabish's *Better Data Visualizations* covers chart makeovers and practitioner guidance. This book covers the full production pipeline from perceptual theory to CLI-driven SVG generation.

The gap this book fills: no course textbook teaches the design intelligence layer of SVG infographic production to ML engineers, with a coherent design system they can operationalize, a CLI-based production pipeline that uses AI code generation, and a consistent framework proving which decisions remain irreducibly human.

## Positioning statements by competitor

**vs. Cairo, *The Functional Art*:**
"Unlike *The Functional Art*, which argues for visualization as communication and provides an analytical vocabulary for reading existing work, this book teaches engineers to produce SVG infographics with a specific design system, a CLI-driven pipeline, and a defensible production process — assuming Cairo's argument was won."

**vs. Wilke, *Fundamentals of Data Visualization*:**
"Unlike *Fundamentals of Data Visualization*, which provides the most comprehensive chart selection and encoding guide for data visualization, this book extends that foundation to infographic layout, annotation, AI-assisted SVG generation, and the full editorial-to-production pipeline that engineers actually need."

**vs. Murray, *Interactive Data Visualization for the Web*:**
"Unlike *Interactive Data Visualization for the Web*, which teaches D3.js for interactive web development, this book teaches SVG infographic production for engineers using AI code generators — D3 is one tool in a system organized around human design judgment."

**vs. Schwabish, *Better Data Visualizations*:**
"Unlike *Better Data Visualizations*, which focuses on chart makeovers and practitioner guidance for existing outputs, this book teaches engineers to construct infographics from brief to Illustrator-editable SVG from scratch, with a complete production pipeline and a coherent design philosophy."

**vs. Brutalist D3 × Claude (companion volume):**
"This book is the infographic design practicum. *Brutalist D3 × Claude* is the chart-type companion (61 chart types, marks-and-channels grammar, D3 v7 patterns). Together they constitute a complete visual communication curriculum for engineering programs."

---

# PART 5 — THREE-ACT LEARNING ARC

## The arc statement

This book takes the reader from **confident user of AI code generation who cannot evaluate or defend the visual output** to **practitioner who can construct, defend, and produce a complete SVG infographic pipeline** by first establishing that visual encoding decisions have a cognitive science basis that makes some choices demonstrably wrong (Act One), then building a coherent design system piece by piece through domain examples the student can apply immediately (Act Two), then driving a CLI-based production pipeline that proves in every exercise which decisions remain irreducibly human (Act Three).

## The opening provocation

Chapter 1 gives the student an infographic that looks professional and communicates incorrectly. The encoding choices are visually polished and perceptually wrong. The student has likely made the same choices themselves. Act One explains why — in the language of cognitive science, not aesthetic preference.

## Act One — Theory (Chapters 1–5)

**Starting state:** The student can produce a chart or SVG with an AI tool. They cannot evaluate whether it communicates accurately.
**Ending state:** The student can identify encoding failures by name (cognitive overload, channel mismatch, memorability/comprehension confusion), apply the dual coding prediction, and state the Brutalist design commitment in one sentence.
**The theoretical core:** Perceptual and cognitive science is not decoration for this book — it makes specific, falsifiable predictions about visual encoding choices. The student learns to use it as a diagnostic tool.
**Act One → Act Two transition:** The student can look at an infographic, identify its encoding decisions, and evaluate whether those decisions are well-matched to the concept's structure and the audience's cognitive constraints.

## Act Two — Design System (Chapters 6–10)

**Starting state:** The student can evaluate infographics but cannot produce them systematically.
**Ending state:** The student has a complete Brutalist design system: color tokens, typography stack, mark vocabulary, channel hierarchy, annotation rules, layout typology. They can produce a complete design specification before writing a line of code.
**Hardest conceptual moment:** Chapter 7 (The Painter's Algorithm vs. Editorial Grouping) — the rendering order SVG requires and the editorial organization Illustrator needs are structurally in conflict, and resolving that conflict requires understanding both.
**Act Two → Act Three transition:** The student has a design specification document that can be given to Claude Code as a system prompt. The specification IS the design intelligence layer — the CLI pipeline executes against it.

## Act Three — Production Pipeline (Chapters 11–15)

**Starting state:** The student has a design specification and the design vocabulary to evaluate the output.
**Ending state:** The student can drive a complete CLI-based production pipeline — Audit → Schema → Generate → Verify → Handoff — using Claude Code to produce Illustrator-editable SVG with embedded metadata, converted to 300 DPI PNG, with a complete AI Use Disclosure.
**The transfer test:** The terminal project requires the student to produce a complete infographic production package for a real domain problem: design brief, design specification, generated SVG, Illustrator-edited version, qualified AI Use Disclosure, and a one-page defense of every encoding decision.

## The CAJAL thread across the arc

CAJAL (the figure intelligence system) appears at three points:
- Act One: as an analytical tool for evaluating existing infographics (SCOPE framework as a reading protocol)
- Act Two: as a specification tool for planning new infographics (the intake sequence as a design process)
- Act Three: as an upstream step in the pipeline (pantry/ → cajal.md → SVG generator)

---

# PART 6 — PREREQUISITE MAP

| Prerequisite | Safe to assume? | If not: where addressed |
|---|---|---|
| Python or JavaScript fluency | Yes | — |
| Basic probability and statistics | Probably | Chapter 8 re-establishes encoding rules |
| Familiarity with SVG as a file format | Probably | Chapter 3 treats SVG from first principles |
| AI code generation tool experience | Probably | Chapter 11 contextualizes Claude Code |
| Graphic design training | No | Excluded — not required; theory replaces it |
| CSS or web design | No | Excluded — not required |
| D3.js | No | Chapter 13 introduces D3 patterns as needed |
| Adobe Illustrator | No | Chapter 14 introduces Illustrator for editability |

**Front-loading decision:** SVG structure is the only prerequisite rated "No" that is not excluded. It is addressed in Chapter 3 as primary instruction. No Chapter 0 or prerequisite appendix required — the one technical gap is covered at first use.

---

# PART 7 — ASSESSMENT STRUCTURE

| Component | Points | Chapters |
|---|---|---|
| Reading Responses (5 × 30 pts) | 150 | 1, 3, 6, 8, 11 |
| Design Critiques (5 × 25 pts) | 125 | 2, 4, 5, 7, 9 |
| Design Specification Checkpoint | 100 | 10 |
| Pipeline Checkpoint | 100 | 13 |
| Final Project | 250 | 15 |
| Workshop participation | 150 | Continuous |
| Weekly exercises (8 × 28 pts) | 224 | Drop lowest |
| **Total** | **1099** | |

**AI Use Disclosure requirement:** Every submitted deliverable includes an AI Use Disclosure identifying at minimum two design decisions that required human judgment that AI could not supply. Submissions without a completed disclosure receive a 15-point deduction. The final project disclosure must name three such decisions across the complete production process.

---

# PART 8 — CHAPTER-BY-CHAPTER TOC

---

## ACT ONE — THEORY (Chapters 1–5)
*What this act does: establishes that visual encoding decisions have a cognitive science basis that makes some choices demonstrably wrong. The student builds a diagnostic vocabulary before touching a tool.*

---

### CHAPTER 1 — The Infographic That Lied While Telling the Truth

**One-line:** Students learn to distinguish visual accuracy from communicative accuracy — an infographic can be factually correct and perceptually misleading simultaneously.

**Learning outcomes:**
1. (Understand) Distinguish between data accuracy and perceptual accuracy using a specific infographic example.
2. (Analyze) Identify at least two encoding decisions in a given infographic that create false impressions without containing false data.
3. (Apply) Classify an infographic claim as accurate, misleading, or indeterminate.

**Opening:** A published infographic — professional source, factually correct data, misleading visual structure. The encoding choices are identified before any theory is introduced. Students see the problem before they have vocabulary for it.

**Core content:** The claim that every infographic makes (explicit and structural); perceptual accuracy vs. data accuracy; why visual authority amplifies misleading encodings; the difference between memorability and comprehension (Borkin).

**Assessment:** Reading Response #1 (30 pts)

**Bridge:** Why do these encoding errors happen? Because visual design is not arbitrary — it is constrained by how human perception works. Chapter 2 introduces the perceptual science.

---

### CHAPTER 2 — How the Visual System Processes Information

**One-line:** Students learn the cognitive and perceptual foundations that make some visual encoding choices demonstrably better than others — not as matters of taste, but as matters of cognitive architecture.

**Learning outcomes:**
1. (Understand) Explain dual coding theory and its implication for text-visual integration in infographic design.
2. (Understand) Apply cognitive load theory to predict when an infographic will fail comprehension.
3. (Analyze) Identify which of Cleveland and McGill's perceptual channels is being used in a given encoding and predict its accuracy.
4. (Evaluate) Assess a given encoding decision against Gestalt grouping principles.

**Opening:** Two infographics on the same dataset — one uses position on a common scale, the other uses area. Students estimate values from each. The measurement error is the lesson.

**Core content:** Dual coding theory (Paivio); cognitive load and working memory constraints; Cleveland and McGill's perceptual channel hierarchy; Gestalt principles as pre-attentive processing; the memorability/comprehension distinction.

**Assessment:** Design Critique #1 (25 pts)

**Bridge:** If encoding choices are constrained by cognitive science, what is the design philosophy that operationalizes those constraints? Chapter 3 introduces Brutalism as a design commitment, not an aesthetic.

---

### CHAPTER 3 — Brutalism as a Design Commitment

**One-line:** Students learn that Brutalism in infographic design is not a visual style but a set of commitments — exposed structure, functional marks, honest hierarchy — that map directly onto the perceptual science from Chapter 2.

**Learning outcomes:**
1. (Understand) State the Brutalist design commitments in relation to cognitive science principles.
2. (Analyze) Distinguish between decoration that aids comprehension (semantically meaningful embellishment) and decoration that harms it (arbitrary visual noise).
3. (Evaluate) Apply the blur test to a candidate infographic.
4. (Apply) Classify a design choice as Brutalist-consistent or Brutalist-violating, with justification.

**Opening:** A Brutalist building and a Brutalist infographic side by side. The structural parallels named: exposed concrete = exposed data structure; no ornament = no non-encoding visual marks; honest material = honest channel selection.

**Core content:** Brutalism as a design philosophy; the Bateman et al. finding and its correct interpretation (semantically meaningful vs. arbitrary embellishment); the blur test; why Brutalism is not minimalism (Tufte) and not decoration (Holmes); the Brutalist design commitments as a checklist.

**Assessment:** Reading Response #2 (30 pts)

**Bridge:** SVG is the medium for this design system. But SVG means different things to a browser, a code generator, and a designer. Chapter 4 introduces SVG as a design medium — with all three audiences in view.

---

### CHAPTER 4 — SVG as a Design Medium

**One-line:** Students learn what SVG is as a file format, why it is the right medium for infographic production, and what structural decisions at generation time determine whether the output is Illustrator-editable or a dead end.

**Learning outcomes:**
1. (Understand) Explain the SVG document object model and how it maps to Illustrator's layer/group structure.
2. (Analyze) Identify the structural decisions in an SVG file that determine Illustrator editability.
3. (Apply) Read a D3-generated SVG and name its editability failures.
4. (Evaluate) Assess whether a given SVG is production-ready for the editorial-to-print pipeline.

**Opening:** The same infographic in three states: browser-rendered (looks right), SVG source (structural mess), Illustrator-opened (editing nightmare). The gap between "looks right" and "editable" is the subject of the chapter.

**Core content:** SVG document structure (`<g>`, `<text>`, `<path>`, `<defs>`); Illustrator's layer model vs. SVG's group model; presentation attributes vs. inline CSS; the clipping mask problem; the DPI mismatch (72 vs. 96); what makes SVG Illustrator-editable; the one-way ticket principle.

**Assessment:** Design Critique #2 (25 pts)

**Bridge:** SVG is the medium. The Brutalist design system is the content. Chapter 5 introduces the design system — the seven color tokens, the typography stack, the spacing grid — as a production-ready specification.

---

### CHAPTER 5 — The Brutalist Design System

**One-line:** Students learn the complete Brutalist design system — seven color tokens, three-font stack, 8px spacing grid, stroke conventions — as a production-ready specification that can be pasted directly into DESIGN.md.

**Learning outcomes:**
1. (Understand) Explain the role of each of the seven color tokens and the rule against using ochre as a data-encoding color.
2. (Apply) Select the correct font family for a given typographic role (display heading, body label, axis tick, source line).
3. (Apply) Construct a chart area that follows the Brutalist layout conventions (margins, grid, fill vs. background).
4. (Evaluate) Test a candidate figure against the luminance ladder in grayscale.

**Opening:** A single infographic built correctly against the design system. Every decision annotated with its design system rule. The annotation is the lesson — students see the system from the output before they learn the rules.

**Core content:** The seven color tokens and their roles; the luminance ladder and grayscale test; the three-font stack (EB Garamond for display, Inter for body and labels, JetBrains Mono for axis ticks); the 8px grid; stroke conventions; arrow conventions; the DESIGN.md specification format.

**Assessment:** Reading Response #3 (30 pts)

**Bridge:** The design system specifies the visual vocabulary. Act Two teaches how to deploy it: marks and channels, hierarchy, annotation, layout, and the complete CAJAL figure intelligence system.

---

## ACT TWO — DESIGN SYSTEM (Chapters 6–10)
*What this act does: builds the full design vocabulary and specification system piece by piece. Each chapter adds one layer of design intelligence. By Chapter 10 the student can produce a complete design specification document that serves as the input to the Claude Code pipeline in Act Three.*

---

### CHAPTER 6 — Marks, Channels, and the Grammar of Infographics

**One-line:** Students learn to apply Bertin's visual variables and the infographic/dataviz distinction to determine which encoding approach is appropriate for a given concept and audience.

**Learning outcomes:**
1. (Analyze) Classify a given concept as better served by data visualization or by editorial infographic design, with justification.
2. (Apply) Select the appropriate mark (bar, dot, line, area, node, icon) for a given data type and comparison task.
3. (Apply) Select the appropriate channel (position, length, area, hue, luminance) for a given attribute type and audience.
4. (Evaluate) Apply the FT Visual Vocabulary principle: start from the relationship in the data, not the designer's preferred form.

**Opening:** The same two variables displayed six ways. Same data. Radically different comprehension rates. The form-first failure is experienced before the relationship-first principle is named.

**Core content:** Bertin's seven visual variables; the infographic/dataviz distinction (editorial vs. analytical); the FT Visual Vocabulary relationship taxonomy (deviation, correlation, ranking, distribution, change over time, magnitude, part-to-whole, spatial, flow); marks vs. channels; the two-data-encoding-color limit; secondary encodings (pattern, direct labels, figure decomposition).

**Assessment:** Reading Response #4 (30 pts)

**Bridge:** Marks and channels govern individual encodings. Visual hierarchy governs how multiple encodings are organized. Chapter 7 introduces hierarchy — and the conflict between rendering order and editorial organization.

---

### CHAPTER 7 — Visual Hierarchy and the Painter's Algorithm

**One-line:** Students learn that SVG rendering order (Painter's Algorithm) and editorial organization (Illustrator editability) are structurally in conflict, and learn the multi-layer architecture that resolves this conflict.

**Learning outcomes:**
1. (Understand) Explain the Painter's Algorithm and why it determines SVG layer order.
2. (Analyze) Identify the conflict between rendering-optimized grouping and editorially-meaningful grouping in a given SVG.
3. (Apply) Design a multi-layer SVG architecture that satisfies both rendering requirements and editorial organization.
4. (Evaluate) Assess the Illustrator-editability of a given SVG group structure.

**Opening:** A D3-generated SVG opened in Illustrator. The layers panel is a pile of anonymous groups. The student is asked to change the annotation color. The experience of navigating an editorially meaningless structure IS the lesson.

**Core content:** The Painter's Algorithm; why rendering groups and editorial groups conflict; the multi-layer architecture (primary layers by visual depth, semantic sub-layers within); the semantic naming convention; the `data-name` dual-attribute strategy; the ID character escaping failure (why `1st-floor` becomes `_x31_st-floor`).

**Assessment:** Design Critique #3 (25 pts)

**Bridge:** Hierarchy organizes the structure. Color and typography communicate the meaning. Chapter 8 covers color systems and the typography conventions that carry editorial weight.

---

### CHAPTER 8 — Color Systems and Typography for Infographics

**One-line:** Students learn to deploy color as a semantic system — not as decoration — and to use typography as hierarchy rather than style.

**Learning outcomes:**
1. (Apply) Deploy the seven Brutalist color tokens according to their roles, with no hardcoded hex values in production files.
2. (Analyze) Identify color as categorical, sequential, or emphasis channel, and select the correct token for each.
3. (Apply) Assign the correct font family, size, weight, and fill for each typographic role in a complete infographic.
4. (Evaluate) Verify that a candidate infographic passes the grayscale test and WCAG contrast requirements.

**Opening:** An infographic that passes aesthetic review and fails accessibility review. Same file. The WCAG 4.5:1 contrast requirement is measured. Two labels fail. The fix demonstrates that accessibility and design quality are not in tension.

**Core content:** The seven-token color system deployed as a semantic system; categorical vs. sequential color; the single-accent principle; the opacity compounding failure (why `opacity="0.5"` + `fill-opacity="0.5"` compounds); the WCAG contrast requirements; typography as hierarchy; the `text-anchor` export mismatch (Illustrator bakes coordinates, loses the attribute); the `<tspan>` whitespace collapse bug.

**Assessment:** Reading Response #5 (30 pts)

**Bridge:** Color and typography carry meaning. Annotation carries explanation. Chapter 9 covers annotation — the highest-leverage design decision in most infographics.

---

### CHAPTER 9 — Annotation: When It Earns Its Place

**One-line:** Students learn the four jobs annotation must do to earn its place, the fallback hierarchy for placement, and the blur test as a practical check for annotation hierarchy.

**Learning outcomes:**
1. (Evaluate) Apply the four-job test to a candidate annotation: interpretation, orientation, context, caveat.
2. (Apply) Apply the spatial proximity rule and the annotation fallback hierarchy (adjacent → leader line → legend as last resort).
3. (Apply) Use the blur test to verify that headline, main visual, and primary annotation form a visible hierarchy at low resolution.
4. (Analyze) Identify annotation that clutters rather than clarifies and specify its removal.

**Opening:** Two versions of the same infographic — one with annotation at Illustrator defaults (positioned wherever the cursor was), one with annotation following the spatial proximity rule. Comprehension measured by a 10-second exposure test.

**Core content:** The four jobs of annotation (interpretation, orientation, context, caveat); the spatial proximity rule (Mayer); direct labels vs. legends; the annotation fallback hierarchy; the blur test; annotation that clutters (labels that restate what the axis already says; decorative text; over-annotated data series); annotation at decision points.

**Assessment:** Design Critique #4 (25 pts)

**Bridge:** Individual encoding elements are specified. Chapter 10 introduces the layout layer — how a complete infographic is organized spatially, and how the CAJAL figure intelligence system turns a concept description into a complete design specification.

---

### CHAPTER 10 — Layout, Composition, and the CAJAL Specification System
**[DESIGN SPECIFICATION CHECKPOINT]**

**One-line:** Students produce their first complete design specification document using the CAJAL SCOPE framework, demonstrating that the design intelligence layer is populated before any code is written.

**Learning outcomes:**
1. (Apply) Select the correct layout type (singular, composite, long-form) for a given communication purpose and delivery medium.
2. (Apply) Produce a complete CAJAL SCOPE specification: Specification, Content, Organization, Presentation, Exclusions.
3. (Evaluate) State the exclusion list for a candidate infographic — and explain why the exclusion list is more important than the inclusion list.
4. (Create) Produce a complete DESIGN.md specification for a candidate infographic that can serve as input to the Act Three pipeline.

**Opening:** The intake sequence demonstrated live. The instructor takes a vague brief ("make a figure showing the relationship between X and Y") through the CAJAL intake process. The concept becomes defensible; the exclusions are named; the figure type is selected. The design specification is the output.

**Core content:** The three layout types (singular, composite, long-form) and their media contexts; the CAJAL SCOPE framework; the 6–8 component limit and the split decision; the exclusion list as the highest-leverage design parameter; the DESIGN.md specification format; the relationship between the specification and the Claude Code prompt.

**Assessment:** Design Specification Checkpoint (100 pts) — a complete CAJAL SCOPE specification and DESIGN.md for the student's terminal project infographic.

**Bridge:** The design specification is complete. Act Three begins: giving that specification to Claude Code, driving the production pipeline, and defending every output against the design specification.

---

## ACT THREE — PRODUCTION PIPELINE (Chapters 11–15)
*What this act does: drives the complete CLI-based production pipeline using Claude Code. Act Three stops providing well-formed design problems and starts giving the student the kind of pipeline problems they will actually encounter. The design intelligence layer from Acts One and Two is deployed, not learned.*

---

### CHAPTER 11 — The Brutalist System: CLAUDE.md, DESIGN.md, PROJECT.md

**One-line:** Students learn the three governing files that define all production before any code is written, and why the phase gate (no generation before both the Intent Layer and Schema Layer are populated) is an enforcement mechanism, not a suggestion.

**Learning outcomes:**
1. (Understand) Explain the role of each of the three governing files and why each is necessary.
2. (Apply) Populate CLAUDE.md for the D3 v7 stack with all naming conventions, canonical patterns, and prohibited actions.
3. (Apply) Populate DESIGN.md from the student's Design Specification Checkpoint output.
4. (Evaluate) Assess a given PROJECT.md for phase gate compliance — both the Intent Layer and Schema Layer must be fully populated before generation begins.

**Opening:** The most common AI code generation failure mode: generation begins before the specification is complete. The output looks plausible. The encoding decisions are wrong. The structure is not editable. Rebuilding from scratch takes longer than specifying correctly would have.

**Core content:** The three governing files and their roles; CLAUDE.md as the coding constitution (stack-specific, changes when the renderer changes); DESIGN.md as the visual constitution (project-specific, contains the seven-token palette and typography stack); PROJECT.md as the project state (Intent Layer never overwritten by AI; Schema Layer maintained by AI); the phase gate as an enforced condition; the Brutalist system's five phases (Audit → Schema → Generate → Verify → Handoff); labor separation and refusal behavior.

**Assessment:** Reading Response — Act Three framing (30 pts)

**Bridge:** The governing files are in place. Chapter 12 audits the existing project state before any generation begins — the Audit phase is not optional.

---

### CHAPTER 12 — Audit: What Exists Before You Touch Anything

**One-line:** Students learn to run the Audit phase before any generation, producing a complete inventory of existing assets, naming conventions in use, and the gap between what exists and what the DESIGN.md specifies.

**Learning outcomes:**
1. (Apply) Run a complete Audit phase: inventory all existing assets, name all existing conventions, map all gaps between current state and DESIGN.md.
2. (Analyze) Identify naming convention violations in an existing codebase using the CLAUDE.md rules.
3. (Apply) Populate the Schema Layer of PROJECT.md from the Audit output.
4. (Evaluate) Determine whether the phase gate condition is met: both layers populated before generation begins.

**Opening:** A project directory with existing SVG files, a partial DESIGN.md, and no CLAUDE.md. The Audit phase run live. Every file inventoried. Every naming violation flagged. The gap between current state and specification mapped. The phase gate condition assessed.

**Core content:** The Audit phase checklist; naming convention audit against CLAUDE.md; existing asset inventory; gap analysis between current state and DESIGN.md; PROJECT.md Schema Layer population; the phase gate condition; why auditing before generating prevents the most costly production failures.

**Assessment:** Audit deliverable for the terminal project (ungraded; required for Pipeline Checkpoint)

**Bridge:** The Audit is complete. The phase gate condition is met. Chapter 13 begins generation — using Claude Code as a structured executor of the design specification.

---

### CHAPTER 13 — Generate: Claude Code as a Structured Executor
**[PIPELINE CHECKPOINT]**

**One-line:** Students learn to use Claude Code as a structured executor of the design specification — not as a creative collaborator — and to enforce the CLAUDE.md constraints at every generation step.

**Learning outcomes:**
1. (Apply) Construct a Claude Code prompt that encodes the complete CAJAL SCOPE specification and DESIGN.md constraints.
2. (Apply) Generate a D3-driven SVG infographic using the clean D3 patterns from CLAUDE.md (semantic layer scaffold, `.join()` lifecycle management, presentation attributes via `.attr()`).
3. (Evaluate) Apply the CLAUDE.md verification checklist to generated output: correct naming, correct color tokens, correct font stacks, no hardcoded hex values, no D3 `.style()` calls for visual properties.
4. (Create) Generate the complete SVG output for the terminal project, with the CAJAL metadata block embedded.

**Opening:** The same design specification given to Claude Code twice — once without a system prompt, once with the complete CLAUDE.md and DESIGN.md. The outputs compared. The specification-less output is visually plausible and technically wrong on 11 counts. The specification-driven output requires zero corrections.

**Core content:** The Claude Code prompt structure; the semantic layer scaffold (`const layers = { background: svg.append("g").attr("id", "background"), ... }`); the `.join()` pattern for clean lifecycle management; presentation attributes vs. `.style()` calls; the slug function for stable IDs; the CAJAL metadata block structure; the verification checklist; the generate-one-unit-at-a-time rule.

**Assessment:** Pipeline Checkpoint (100 pts) — a complete generated SVG with embedded CAJAL metadata, verified against the CLAUDE.md checklist, for the terminal project infographic.

**Bridge:** Generation is complete. The SVG exists. Chapter 14 covers the Verify and Handoff phases — including the critical step most pipelines skip: Illustrator editing for production.

---

### CHAPTER 14 — Verify and Handoff: From SVG to Production Asset

**One-line:** Students learn the Verify phase (human reviews every output before the next is issued) and the Handoff phase (SVG to Illustrator, Illustrator to `.ai`, `.ai` to PNG via `svg-to-png.mjs`), including the manual corrections that every AI-generated SVG requires.

**Learning outcomes:**
1. (Apply) Run the Verify phase against the four-category checklist: structure, text, styling, and naming.
2. (Apply) Open a D3-generated SVG in Illustrator, release all clipping masks, verify group names, correct text alignment, and save as `.ai`.
3. (Apply) Run `node SCRIPTS/svg-to-png.mjs` to produce 300 DPI PNG output.
4. (Evaluate) Produce the complete AI Use Disclosure for the terminal project, naming three identification decisions requiring human judgment.

**Opening:** The Verify phase run on the Pipeline Checkpoint SVG. Every generated SVG has corrections. The corrections are not failures — they are the human judgment layer in the pipeline. Students who skip the Verify phase are not using AI tools; they are being used by them.

**Core content:** The Verify phase checklist (structure: named groups, viewBox, dimensions; text: `<text>` elements, font family, `text-anchor`; styling: presentation attributes, color tokens, no hardcoded hex; naming: semantic IDs, no auto-generated names); the Illustrator workflow (open SVG → release clipping masks → verify groups → correct text → save as `.ai`); the exponential nesting bug and why it forces the one-way ticket rule; the `svg-to-png.mjs` conversion script; the Handoff phase documentation requirements; the AI Use Disclosure.

**Assessment:** Design Critique #5 (25 pts) — a peer Verify phase run on another student's Pipeline Checkpoint output, with a written correction list.

**Bridge:** The terminal project is one chapter away. Chapter 15 brings every design decision together into one complete production package.

---

### CHAPTER 15 — The Complete Pipeline: One Brief, Every Decision
**[FINAL PROJECT]**

**One-line:** Students produce a complete infographic production package for a real domain problem — design brief, CAJAL SCOPE specification, DESIGN.md, generated and corrected SVG, PNG, and a full AI Use Disclosure naming every irreducibly human decision.

**Learning outcomes:**
1. (Create) Produce a complete infographic production package: brief, SCOPE specification, DESIGN.md, CLAUDE.md, PROJECT.md, generated SVG, Illustrator-corrected `.ai`, 300 DPI PNG.
2. (Evaluate) Apply the CAJAL blur test, the WCAG contrast check, and the grayscale test to the final output.
3. (Evaluate) Defend every encoding decision — mark, channel, color token, font role, annotation placement, layout type — in a 10-minute design review.
4. (Create) Produce the final AI Use Disclosure: three design decisions across the complete pipeline that required human judgment no AI tool could supply.

**Opening:** What does "done" look like? The complete production package structure is shown before any student work begins. A professional example is walked through in its entirety. The student's task is clear.

**Core content:** Complete production package structure; the design review protocol (10 minutes: brief → specification → output → three encoding decisions defended); the full AI Use Disclosure (higher bar: three decisions, not two); what "production-ready" means in the context of editorial publishing.

**Assessment:** Final Project (250 pts) — complete production package + design review presentation.

---

# PART 9 — CHAPTER ANATOMY TEMPLATE

All 15 chapters follow this structure:

1. Learning objectives (Bloom's level explicit)
2. Opening case (failure-first; real domain infographic or production problem)
3. Prerequisites stated as specific capabilities
4. Core content sections (4–6): concept → example → application
5. Mid-chapter checkpoint (ungraded; surfaces confusion before worked example)
6. Worked example (failure case for Act One; design decision for Act Two; pipeline segment for Act Three)
7. Assessable exercises (minimum 3; at least one at Apply or above)
8. AI Use Disclosure (standard form; domain-specific prompt for Act Three chapters)
9. Chapter summary (capabilities gained, not topics covered)
10. Key terms (5–10; plain language definitions)
11. Bridge question (one question; raises what next chapter answers)
12. Further reading (3–5 sources with one-sentence annotation; credibility status noted)
13. CAJAL Exercise (intake sequence for a chapter-relevant concept; produces a complete SCOPE specification)
14. Claude Code Exercise (copy-paste-ready prompt; produces an assessable SVG artifact)

**Enforcement:** A draft chapter missing items 5, 6, 13, or 14 is an incomplete draft. Do not advance to peer review without resolving it.

---

# PART 10 — CASE STUDY AND EXERCISE STRATEGY

## Domain coverage map

| Domain | Chapters |
|---|---|
| Public health / epidemiology | 1, 8 |
| Climate and energy data | 2, 6 |
| AI/ML system performance | 3, 11 |
| Economic and financial data | 4, 12 |
| Social/demographic data | 5, 9 |
| Science communication | 7, 13 |
| Infrastructure and operations | 10, 14 |
| Student's own domain | 15 |

## Case escalation

Act One cases: a single encoding failure, clear diagnosis, clear fix.
Act Two cases: a design decision with defensible alternatives; the student must choose and justify.
Act Three cases: a real production failure from the instructor's own pipeline — the actual correction log shown.

## Worked example format (all chapters)

Problem statement → First attempt (what an AI tool produces without specification) → Design diagnosis (which principle was violated) → Corrected version (what specification-driven production produces) → The lesson (one sentence) → The limit (where this approach requires judgment the tool cannot supply).

## CAJAL exercise format (all chapters)

Every chapter includes a CAJAL intake sequence for one chapter-relevant concept. The intake produces a complete SCOPE specification — Specification, Content, Organization, Presentation, Exclusions — that serves as the input for the Claude Code exercise in the same chapter. The CAJAL exercise is the design intelligence layer; the Claude Code exercise is the execution layer. Together they instantiate the thesis in every chapter.

---

# PART 11 — HARD TOPICS, CONTESTED CLAIMS, AGING RISK

## Contested claims summary

| Claim | Status | Book's position |
|---|---|---|
| Minimalism (Tufte) is always better | Disputed | Bateman et al. finding correctly interpreted: semantically meaningful embellishment can improve recall without harming comprehension; arbitrary decoration harms both |
| AI can select the right chart type for a dataset | Partially | Functional: useful for candidate generation; unreliable for relationship-first selection without a specification |
| Infographics and data visualizations are the same thing | Conflated in practice | Named as a distinction with design consequences: editorial vs. analytical purpose requires different optimization |
| Claude Code / Codex can replace a graphic designer | Disputed | "Currently requires": the design intelligence layer is the book's subject; the AI Use Disclosure is the empirical test |
| The Brutalist aesthetic is a stylistic preference | Mischaracterized | Grounded in cognitive science; the design commitments are derivable from perceptual accuracy requirements |

## Hard chapters

**Chapter 7 (Painter's Algorithm vs. Editorial Grouping):** Requires an instructor who has worked with D3-generated SVG in Illustrator. The conflict is not intuitive to students who have only seen SVG in a browser.

**Chapter 9 (Annotation):** The four-job test is easy to state and hard to apply without domain knowledge. The worked example must use a domain the students recognize.

**Chapter 13 (Generate):** The gap between specification-driven and specification-less output must be experienced, not described. The opening demonstration requires a live Claude Code session or a very carefully staged before/after.

## Aging risk summary

| Content type | Risk | Review cadence |
|---|---|---|
| Claude Code API and prompt patterns | High | Before each offering |
| Specific CDN versions (D3 7.9.0) | High | Before each offering |
| LLM exercise prompts | High | Before each offering |
| Identification layer thesis | Medium | Every 2 years |
| Perceptual science foundations | Low | On major new results |
| SVG specification | Very low | On major SVG version changes |
| Design system tokens | Low | On brand refresh |

---

# PART 12 — MARKET POSITIONING SUMMARY

The gap this book fills: no course textbook teaches the design intelligence layer of SVG infographic production to ML engineers, with a coherent design system they can operationalize, a CLI-based production pipeline using AI code generation, and a consistent framework proving which decisions remain irreducibly human.

**Market size estimate:**
80–120 course adoptions per year at steady state.
15–35 students per adoption.
1,500–4,000 copies annually at steady state.
Secondary market (professional development, science communication workshops): ~30–40% additional.

---

# PART 13 — FEATURE LIST SUMMARY

| Feature | Priority | Production effort |
|---|---|---|
| 15-chapter architecture, three-act structure | ESSENTIAL | Low |
| Weekly exercises with AI Use Disclosure | ESSENTIAL | Medium |
| Three milestone assessments | ESSENTIAL | Medium |
| Final production package project | ESSENTIAL | Medium |
| CAJAL exercise in every chapter | ESSENTIAL | Medium |
| Claude Code exercise in every chapter | ESSENTIAL | Medium |
| Complete Brutalist design system (DESIGN.md spec) | ESSENTIAL | Low |
| Complete CLAUDE.md for D3 v7 stack | ESSENTIAL | Low |
| Worked example pipeline segments (Act Three) | IMPORTANT | High |
| Three-representation display (SVG → Illustrator → PNG) | IMPORTANT | High (production) |
| CAJAL SVG Generator (Cowork automation) | IMPORTANT | Medium |
| Instructor's manual | IMPORTANT* | High |
| Exercise bank | VALUABLE | Medium |
| Companion website with example SVGs | VALUABLE | Medium |
| Slide decks | VALUABLE | High |
| Video walkthroughs (Act Three pipeline) | ASPIRATIONAL | High |

*The instructor's manual is effectively ESSENTIAL for adoption by any faculty member who is not the author. The Claude Code exercises require an active Claude Code subscription and working Node.js environment — the manual must document the setup.

---

# PART 14 — OUT OF SCOPE

Permanently excluded (no reopen condition without structural revision):

| Topic | Covered better in |
|---|---|
| Interactive D3 visualizations (web-first) | Murray, *Interactive Data Visualization for the Web* |
| 61-chart-type pantry | *Brutalist D3 × Claude* (companion volume) |
| Statistical analysis and causal inference | *Causal Reasoning: Irreducibly Human* (series companion) |
| Motion graphics and animation | Adobe After Effects documentation; CSS animation tutorials |
| Print production (CMYK, bleed, press-ready PDF) | Publisher-specific production guides |
| Infographic marketing and SEO | Content marketing literature |
| Accessibility beyond WCAG 2.1 (e.g., tactile graphics) | NCAM, APH technical guidelines |
| Full formal color theory (Munsell, CIELAB) | Color appearance model literature |

All exclusions acknowledged in the preface with pointers to the better source. The *Brutalist D3 × Claude* relationship (infographic design layer vs. chart-type pantry) is named explicitly as a designed curriculum architecture, not a coverage gap.

---

# PART 15 — ADOPTION RISK REGISTER

| # | Risk | Likelihood | Impact | Status |
|---|---|---|---|---|
| 1 | Claude Code API availability and pricing | Med-High | High | Mitigated: exercises designed to be runnable with any Claude API access; standard Anthropic API fallback documented |
| 2 | D3 version lock (7.9.0 CDN) | Medium | Medium | Mitigated: CLAUDE.md pins CDN URL; version pinning is a feature |
| 3 | Illustrator access (students may use Inkscape) | Medium | Low-Med | Mitigated: Inkscape documented as alternative in Chapters 4 and 14 |
| 4 | SVG-to-PNG pipeline (sharp/Node dependency) | Low-Med | Medium | Mitigated: SCRIPTS/svg-to-png.mjs tested; npm install documented |
| 5 | Instructor preparation for Act Three live demos | Med-High | High | Requires instructor's manual with staged before/after sessions |
| 6 | LLM exercise prompt decay | Med-High | Medium | Test before each offering; update guidance note in Chapter 13 |
| 7 | Students treating CAJAL as optional | Medium | Medium | AI Use Disclosure requirement makes CAJAL non-optional for full credit |
| 8 | Aging risk: identification layer thesis | Medium | Med-High | "Currently requires" qualifier + AI Use Disclosure as empirical test per chapter |
| 9 | Three-representation display production cost | Medium | Medium | Budget graphic designer; CAJAL SVG Generator automates initial drafts |
| 10 | Node.js / npm environment setup in classroom | Medium | Medium | Setup documented in Chapter 11; instructor's manual includes troubleshooting |

---

# PART 16 — OPEN QUESTIONS

| # | Question | Stakes | Decision deadline | Owner |
|---|---|---|---|---|
| 1 | Which Act Three case study domain? The instructor's own domain drives Chapters 12–15 | Quality of worked examples; adoption by non-author faculty | Before manuscript drafting | Author |
| 2 | Will the CAJAL SVG Generator be open-sourced or bundled as a Cowork prompt? | Adoption economics; student access | Before Chapter 10 draft | Author + publisher |
| 3 | Inkscape vs. Illustrator: should Inkscape be a first-class alternative throughout, or only documented in notes? | Accessibility for students without Adobe licenses | Before Chapter 4 draft | Author |
| 4 | Should the book ship with a companion GitHub repository of all generated SVGs and DESIGN.md examples? | Adoption support; instructor confidence | Publisher proposal stage | Author + publisher |
| 5 | AI Use Disclosure rubric: how is "irreducibly human" graded for students in radically different domains? | Assessment fairness; TA workload | Before first course run | Author + TA |
| 6 | Series relationship with *Brutalist D3 × Claude*: should Chapter 6 (Marks, Channels) link explicitly to the companion, or be self-contained? | Adoption as standalone vs. two-course sequence | Publisher proposal stage | Author + publisher |

---

*Full TOC Draft v1.0*
*All phases complete: Vision, Learning Architecture, Chapter Architecture, Scope and Market*
*No blockers before publisher proposal*
*Risk 1 (Claude Code API availability) is the highest ongoing operational risk — documented and mitigated*
