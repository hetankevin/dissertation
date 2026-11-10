# HANDOFF.md

## Current State

Complete UPenn PhD dissertation draft (`main.tex` -> `main.pdf`, **361 pages total**: 11 front-matter pages `i`–`xi`, **207 pages of main text** across Chapters 1–9, **130 pages of appendices** across Appendices A–G, and 24 pages of Bibliography).

- Compiles cleanly via `/opt/homebrew/bin/tectonic main.tex` with **0 BibTeX errors/warnings** and **0 undefined references or citations**.
- Follows the official UPenn dissertation formatting guidelines (`upennstyle.sty`):
  - Graduate Group: `Statistics and Data Science` (Graduate Group Chairperson: Nancy Zhang; Supervisor: Giles Hooker; Committee: Yuting Wei, Enric Boix-Adsera).
  - Double-spaced body text (`\doublespacing`), single-spaced footnotes, quotations, bibliography entries, and tables/appendices where appropriate.
  - Abstract strictly under the 350-word limit (~289 body words) and fits on a single page (`v`).
  - Chapter-prefixed algorithm numbering (`\thechapter.\arabic{algorithm}`, e.g., `Algorithm 2.1`, `Algorithm 8.1`).
  - Concise, self-contained short titles (`[...]`) for all sections, figures, and tables in the Table of Contents, List of Tables, and List of Illustrations.
- Draft markup (`\draftmarkuptrue` in `macros.tex`, line 842):
  - **Green text (`\aigen{...}` and `\begin{aigenblock}...\end{aigenblock}`)**: Newly drafted synthesis, transition paragraphs, and deferral notes.
  - **Bold red all-caps (`\todoresolve{...}`)**: Open items to verify or resolve before final submission.
  - To produce a clean submission PDF without green/red markup, switch `\draftmarkuptrue` to `\draftmarkupfalse` in [`macros.tex`](./macros.tex).

## Chapter & Appendix Structure (and Page Counts)

1. **Chapter 1: Introduction** ([`chapters/ch01-introduction.tex`](./chapters/ch01-introduction.tex), pp. 1–11, 11 pp.)
2. **Chapter 2: Learning from Offline and Online Data** ([`chapters/ch02-hybrid-rl.tex`](./chapters/ch02-hybrid-rl.tex), pp. 12–32, 21 pp.) — combines *A Natural Extension to Online Algorithms for Hybrid RL with Limited Coverage* (Tan and Xu, RLJ 2024) and *Hybrid Reinforcement Learning Breaks Sample Size Barriers in Linear MDPs* (Tan, Fan, and Wei, NeurIPS 2024).
   - **Appendix A** ([`appendices/app02-hybrid-rl.tex`](./appendices/app02-hybrid-rl.tex), pp. 208–213, 6 pp.): Proof of Theorem 2.1 and unabridged descriptions of Algorithms A.1–A.2, with remaining technical lemmas deferred to the papers.
3. **Chapter 3: Learning Shared Structure from Heterogeneous Data** ([`chapters/ch03-latent-bandits.tex`](./chapters/ch03-latent-bandits.tex), pp. 33–47, 15 pp.) — *Leveraging Offline Data in Linear Latent Contextual Bandits* (Kausik, Tan, and Tewari, NeurIPS 2024).
   - **Appendix B** ([`appendices/app03-latent-bandits.tex`](./appendices/app03-latent-bandits.tex), p. 214, 1 p.): Deferred to Kausik, Tan, and Tewari (2024).
4. **Chapter 4: Statistically and Computationally Efficient Actor–Critic Methods** ([`chapters/ch04-actor-critic.tex`](./chapters/ch04-actor-critic.tex), pp. 48–95, 48 pp.) — combines Part I: *Actor-Critics Can Achieve Optimal Sample Efficiency* (Tan, Fan, and Wei, ICML 2025, pp. 49–77) and Part II: *Optimistic Actor-Critic with Parametric Policies for Linear MDPs* (Lin, Asad, Tan, Ishfaq, Szepesvári, and Vaswani, AISTATS 2026, pp. 78–95).
   - **Appendix C** ([`appendices/app04-actor-critic.tex`](./appendices/app04-actor-critic.tex), pp. 215–231, 17 pp.): Full proof of the flagship rare-switching $Q^*$-critic regret bound (Theorem 4.2), with remaining Part I extensions and Part II proofs deferred to the papers.
5. **Chapter 5: Learning Continuous-Action Diffusion Policies** ([`chapters/ch05-diffusion-policies.tex`](./chapters/ch05-diffusion-policies.tex), pp. 96–124, 29 pp.) — *Learning Diffusion Policies with Sublinear Regret* (Tan, Huang, and Wei, working paper 2026).
   - **Appendix D** ([`appendices/app05-diffusion-policies.tex`](./appendices/app05-diffusion-policies.tex), pp. 232–265, 34 pp.): Regret proofs for Vanilla Diffusion PG, DDIM NPG, and Optimistic/Hybrid Critic Behavior Cloning.
6. **Chapter 6: Statistical Inference for Boosted Regression and Additive Models** ([`chapters/ch06-boosting-inference.tex`](./chapters/ch06-boosting-inference.tex), pp. 125–153, 29 pp.) — combines Part I: *Statistical Inference for Gradient Boosting Regression* (Fang, Tan, and Hooker, NeurIPS 2025) and Part II: *Statistical Inference for Explainable Boosting Machines* (Fang, Tan, Pipping, and Hooker, AISTATS 2026).
   - **Appendix E** ([`appendices/app06-boosting-inference.tex`](./appendices/app06-boosting-inference.tex), p. 266, 1 p.): Deferred to Fang, Tan, and Hooker (2025) and Fang, Tan, Pipping, and Hooker (2026).
7. **Chapter 7: Parameter Estimation under Partial Observability** ([`chapters/ch07-pomp-estimation.tex`](./chapters/ch07-pomp-estimation.tex), pp. 154–181, 28 pp.) — *Automatic Differentiation to Improve Parameter Estimation for Partially Observed Markov Processes* (Tan, Abkemeier, He, Hooker, and Ionides, 2024–2026).
   - **Appendix F** ([`appendices/app07-pomp-estimation.tex`](./appendices/app07-pomp-estimation.tex), pp. 267–301, 35 pp.): Proofs of Theorems 7.1–7.5 and Feynman–Kac Monte Carlo theory, with the higher-order bias–variance expansion and Daphnia case study deferred to the paper.
8. **Chapter 8: Control under Partial Observability** ([`chapters/ch08-pomdp-control.tex`](./chapters/ch08-pomdp-control.tex), pp. 182–202, 21 pp.) — *From POMDP Theory to Deep RL with Particle Filters* (Tan and Xu, NeurIPS 2026).
   - **Appendix G** ([`appendices/app08-pomdp-control.tex`](./appendices/app08-pomdp-control.tex), pp. 302–337, 36 pp.): Belief-tree planning subroutine (`Algorithms G.1–G.2`) and the main 4-way regret proof (Theorem 8.1).
9. **Chapter 9: Conclusion** ([`chapters/ch09-conclusion.tex`](./chapters/ch09-conclusion.tex), pp. 203–207, 5 pp.)

## How to Verify

```bash
/opt/homebrew/bin/tectonic main.tex
```

## Open Items for Author Review (`\todoresolve{...}`)

- Replace placeholder dedication and acknowledgment in [`main.tex`](./main.tex) and verify committee member titles on the title page.
- Review dissertation abstract in [`main.tex`](./main.tex) (< 350 words).
- Review synthesis and chapter transitions in Chapters 1–9 (rendered in green under `\draftmarkuptrue`).
- Verify whether to keep Chapter 6 (Boosting & EBM Inference) or restrict solely to RL/Bandit/POMP/POMDP chapters.
- Resolve the remaining Chapter 8 camera-ready items (`E3`/`E4`) flagged in [`chapters/ch08-pomdp-control.tex`](./chapters/ch08-pomdp-control.tex).
- When ready for final submission, set `\draftmarkupfalse` in [`macros.tex`](./macros.tex) and recompile.
