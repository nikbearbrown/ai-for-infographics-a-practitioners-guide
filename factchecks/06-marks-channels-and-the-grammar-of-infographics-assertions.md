# Fact-check — Chapter 6: Marks, Channels, and the Grammar of Infographics

| Assertion | Type | Verdict | Source / URL | Note |
|---|---|---|---|---|
| Jacques Bertin's *Semiology of Graphics* (1967 French original; English trans. 1983) gave visualization its first systematic grammar | ATTRIBUTION-CITATION / HISTORICAL | CONFIRMED | https://en.wikipedia.org/wiki/Jacques_Bertin ; https://www.historyofinformation.com/detail.php?id=3361 | *Sémiologie graphique* published 1967. English trans. by William J. Berg (of the revised 2nd French ed.), foreword by Howard Wainer, University of Wisconsin Press, 1983. Title *Semiology of Graphics: Diagrams, Networks, Maps*. All details correct. |
| Bertin separated marks (point/line/area) from "retinal variables" (channels: position, size, value/lightness, hue, orientation, shape, texture) | ATTRIBUTION-CITATION | CONFIRMED | Bertin 1983; standard dataviz pedagogy | Bertin's term "retinal variables" and the mark/variable separation are accurately described. |
| Cleveland & McGill, "Graphical Perception...," *JASA*, 1984; ranked elementary perceptual tasks by decoding accuracy | ATTRIBUTION-CITATION / VERIFIABLE-EMPIRICAL | CONFIRMED | https://www.tandfonline.com/doi/abs/10.1080/01621459.1984.10478080 | JASA vol. 79, no. 387, pp. 531–554. Ordering: (1) position common scale, (2) position non-aligned scales, (3) length/direction/angle, (4) area, (5) volume/curvature, (6) shading/color. Chapter's 7-rung ladder is a faithful expansion. |
| The accuracy ladder (position > length > angle > area > volume > color) is the central falsifiable result of visualization science | VERIFIABLE-EMPIRICAL | CONFIRMED | Cleveland & McGill 1984 | Accurate characterization. Chapter splits "angle/slope" and lists hue last for *quantity* — consistent with the paper. |
| Jock Mackinlay, "Automating the Design of Graphical Presentations of Relational Information," *ACM Transactions on Graphics*, 1986; APT; expressiveness/effectiveness criteria | ATTRIBUTION-CITATION | CONFIRMED | https://dl.acm.org/doi/10.1145/22949.22950 ; https://en.wikipedia.org/wiki/Jock_D._Mackinlay | *ACM TOG* vol. 5, no. 2, pp. 110–141. Tool named APT ("A Presentation Tool"). Expressiveness and effectiveness criteria; composition algebra; candidate generation automated. All correct. |
| Leland Wilkinson, *The Grammar of Graphics* (1999; 2nd ed. 2005), underlies ggplot2/Vega | ATTRIBUTION-CITATION | CONFIRMED | https://link.springer.com/book/10.1007/0-387-28695-0 | 1st ed. Springer 1999; 2nd ed. Springer 2005. Chapter cites "1999/2005" in prose and "2nd ed. Springer 2005" in Sources — both correct. ggplot2/Vega lineage is well established. |
| FT *Visual Vocabulary* organizes chart families by data relationship (ranking, magnitude, change-over-time, part-to-whole, distribution, correlation, deviation, flow, spatial) | ATTRIBUTION-CITATION | CONFIRMED | https://github.com/Financial-Times/chart-doctor/tree/main/visual-vocabulary ; https://ft-interactive.github.io/visual-vocabulary/ | FT categories: Deviation, Correlation, Ranking, Distribution, Change over Time, Magnitude, Part-to-Whole, Spatial, Flow. Chapter's nine relationships match. Correctly framed as practitioner guide, not research. |
| Humans are bad at estimating area; bubble charts produce systematic underestimation of gaps | VERIFIABLE-EMPIRICAL | CONFIRMED | Cleveland & McGill 1984 (area rung 4–5 of 6) | Area is a low-accuracy channel; the "eye is bad at areas" claim is well supported. |
| Wilke, *Fundamentals of Data Visualization*, O'Reilly 2019 (Sources) | ATTRIBUTION-CITATION | CONFIRMED | Claus O. Wilke, O'Reilly, 2019 | Correct. |

## Resolved `[verify]` flags
- Line 17 "[High — verify edition/translation details]": **RESOLVED**. Berg translation, Wainer foreword, U. Wisconsin Press, 1983, of the revised French edition. Edited prose flag to a confirmed note.
- Line 25 "[Medium — verify Wilkinson edition]": **RESOLVED**. 1999 first / 2005 second confirmed.
- Line 45 "[High — verify]" (Mackinlay): **RESOLVED**. ACM TOG 1986, APT confirmed.
- Source line "[verify translation/edition details]" (Bertin) and "[verify]" (Mackinlay): confirmed; left light editorial flags lightened.

## Author-framing (not verified)
- The "form-first failure" as the most common AI-figure defect; the CAJAL/DESIGN.md decomposability argument; infographic-vs-dataviz distinction by purpose (chapter already self-labels as the book's framing). Left as-is.

**Verdict counts:** CONFIRMED 9, NEEDS-NUANCE 0, CONTRADICTED 0, UNVERIFIABLE 0.
**Fixes applied:** edition/citation `[verify]` notes resolved in prose (see below).
**Flags resolved:** 4. **Flags open:** 0.
