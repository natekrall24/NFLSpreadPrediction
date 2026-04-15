# Final Presentation Outline
**Stat 345: Sports Analytics**
Target length: 15–20 minutes | 16 slides

---

## Section 1: Refresher (3 slides)

1. **Title** — team, course, presentation title
2. **The Paper in 60 Seconds** — Warner (2010): can a GP trained on box-score stats predict NFL margins, and how does it compare to Vegas?
3. **Our Extension** — same methodology, shifted data window to 2015–2024; core question: has Vegas gotten sharper in 15 years?

---

## Section 2: Gaussian Processes (4 slides)

4. **Why Not Linear Regression?** — GP gives a prediction *and* a confidence interval; motivate with a concrete game example
5. **What is a GP?** — the intuition: teams with similar stats should have similar outcomes; kernel encodes that similarity
6. **The RBF Kernel** — the squared exponential formula, what length scale and noise level mean in plain terms
7. **Computed Strength** — the eigenvalue ranking from Section 2.2.1, brief visual of how team strength flows through the matrix

---

## Section 3: Our Data & Model (3 slides)

8. **Feature Set** — 46 features: 10 base stats × avg/streak × H/A, win %, computed strength; how leakage was avoided
9. **Warner's 4 Features vs. Our Selection** — what the forward search found, why away team stats dominate
10. **Train/Test Setup** — 2015–2022 train, 2023–2024 test; why we chose this window

---

## Section 4: Results (3 slides)

11. **The Main Finding** — era comparison table (GP accuracy flat ~64%, Vegas jumped 68.5% → 72.1%)
12. **Feature Selection Results** — 8-feature set improves winner accuracy to 67.1% but MAE unchanged; what this means
13. **Betting Framework** — k-threshold results, no profitable edge at scale; what that implies about market efficiency

---

## Section 5: Wrap-Up (3 slides)

14. **Takeaways** — Vegas has gotten sharper; box-score stats aren't enough anymore; the model can't exploit modern lines
15. **Limitations & Future Work** — no injury data, no weather, no line movement, no in-season roster changes; what a stronger model might include
16. **Student Assignment** — brief overview of what we built for the class: fit a GP yourself, explore kernels, try to beat Vegas

---

## Notes

- Slide 11 (era comparison) is the anchor moment — consider a before/after reveal: show Warner's 2008-09 numbers first, then bring in the 2023-24 column
