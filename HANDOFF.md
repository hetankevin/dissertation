# HANDOFF.md

## Current State

Complete UPenn PhD dissertation draft (`main.tex` -> `main.pdf` and `TanStatisticalAndComputationalEfficiencyInSequentialDecisionMaking.pdf`, **332 PDF pages total**: 10 front-matter pages `i`–`x`, **171 pages of main text** across Chapters 1–8, **129 pages of appendices** across Appendices A–F, and 22 pages of Bibliography).

- Compiles cleanly via `/opt/homebrew/bin/tectonic main.tex && cp main.pdf TanStatisticalAndComputationalEfficiencyInSequentialDecisionMaking.pdf` with **0 BibTeX errors/warnings** and **0 undefined references or citations**.
- Follows the official UPenn dissertation formatting guidelines (`upennstyle.sty`):
  - Graduate Group: `Managerial Science and Applied Economics`, Specialization: `Statistics and Data Science` (Graduate Group Chairperson: Nancy Zhang; Supervisor: Giles Hooker; Co-Supervisor: Yuting Wei; Committee: Enric Boix-Adsera).
  - Each research chapter opens with an italicized attribution paragraph naming the paper(s) and stating the dissertation author's contributions at the end of the paragraph.
  - Abstract strictly under the 350-word limit (~255 body words) and fits on a single page (`v`).
  - Chapter-prefixed algorithm numbering (`\thechapter.\arabic{algorithm}`, e.g., `Algorithm 2.1`, `Algorithm 7.1`).
  - Concise, self-contained short titles (`[...]`) for all sections, figures, and tables in the Table of Contents, List of Tables, and List of Illustrations.
- Draft markup (`\draftmarkuptrue` in `macros.tex`, line 842):
  - **Green text (`\aigen{...}` and `\begin{aigenblock}...\end{aigenblock}`)**: Newly drafted synthesis, transition paragraphs, and deferral notes.
  - **Bold red all-caps (`\todoresolve{...}`)**: Open items to verify or resolve before final submission.
  - To produce a clean submission PDF without green/red markup, switch `\draftmarkuptrue` to `\draftmarkupfalse` in [`macros.tex`](./macros.tex).

## Chapter & Appendix Structure (and Page Counts)

1. **Chapter 1: Introduction** ([`chapters/ch01-introduction.tex`](./chapters/ch01-introduction.tex), pp. 1–10, 10 pp.)
2. **Chapter 2: Learning from Offline and Online Data** ([`chapters/ch02-hybrid-rl.tex`](./chapters/ch02-hybrid-rl.tex), pp. 11–31, 21 pp.) — combines *A Natural Extension to Online Algorithms for Hybrid RL with Limited Coverage* (Tan and Xu, RLJ 2024) and *Hybrid Reinforcement Learning Breaks Sample Size Barriers in Linear MDPs* (Tan, Fan, and Wei, NeurIPS 2024).
   - **Appendix A** ([`appendices/app02-hybrid-rl.tex`](./appendices/app02-hybrid-rl.tex), pp. 172–177, 6 pp.): Proof of Theorem 2.1 and unabridged descriptions of Algorithms A.1–A.2, with remaining technical lemmas deferred to the papers.
3. **Chapter 3: Statistically Efficient Actor–Critic Methods** ([`chapters/ch04-actor-critic.tex`](./chapters/ch04-actor-critic.tex), pp. 32–60, 29 pp.) — *Actor-Critics Can Achieve Optimal Sample Efficiency* (Tan, Fan, and Wei, ICML 2025).
   - **Appendix B** ([`appendices/app04-actor-critic.tex`](./appendices/app04-actor-critic.tex), pp. 178–194, 17 pp.): Full proof of the flagship rare-switching $Q^*$-critic regret bound (Theorem 3.2), with remaining extensions deferred to the paper.
4. **Chapter 4: Learning Continuous-Action Diffusion Policies** ([`chapters/ch05-diffusion-policies.tex`](./chapters/ch05-diffusion-policies.tex), pp. 61–89, 29 pp.) — *Learning Diffusion Policies with Sublinear Regret* (Tan, Huang, and Wei, working paper 2026).
   - **Appendix C** ([`appendices/app05-diffusion-policies.tex`](./appendices/app05-diffusion-policies.tex), pp. 195–228, 34 pp.): Regret proofs for Vanilla Diffusion PG, DDIM NPG, and Optimistic/Hybrid Critic Behavior Cloning.
5. **Chapter 5: Statistical Inference for Boosted Regression and Additive Models** ([`chapters/ch06-boosting-inference.tex`](./chapters/ch06-boosting-inference.tex), pp. 90–118, 29 pp.) — combines Part I: *Statistical Inference for Gradient Boosting Regression* (Fang, Tan, and Hooker, NeurIPS 2025) and Part II: *Statistical Inference for Explainable Boosting Machines* (Fang, Tan, Pipping, and Hooker, AISTATS 2026).
   - **Appendix D** ([`appendices/app06-boosting-inference.tex`](./appendices/app06-boosting-inference.tex), p. 229, 1 p.): Deferred to Fang, Tan, and Hooker (2025) and Fang, Tan, Pipping, and Hooker (2026).
6. **Chapter 6: Parameter Estimation under Partial Observability** ([`chapters/ch07-pomp-estimation.tex`](./chapters/ch07-pomp-estimation.tex), pp. 119–146, 28 pp.) — *Automatic Differentiation to Improve Parameter Estimation for Partially Observed Markov Processes* (Tan, Abkemeier, He, Hooker, and Ionides, 2024–2026).
   - **Appendix E** ([`appendices/app07-pomp-estimation.tex`](./appendices/app07-pomp-estimation.tex), pp. 230–264, 35 pp.): Proofs of Theorems 6.1–6.5 and Feynman–Kac Monte Carlo theory, with the higher-order bias–variance expansion and Daphnia case study deferred to the paper.
7. **Chapter 7: Control under Partial Observability** ([`chapters/ch08-pomdp-control.tex`](./chapters/ch08-pomdp-control.tex), pp. 147–167, 21 pp.) — *From POMDP Theory to Deep RL with Particle Filters* (Tan and Xu, NeurIPS 2026).
   - **Appendix F** ([`appendices/app08-pomdp-control.tex`](./appendices/app08-pomdp-control.tex), pp. 265–300, 36 pp.): Belief-tree planning subroutine (`Algorithms F.1–F.2`) and the main 4-way regret proof (Theorem 7.1).
8. **Chapter 8: Conclusion** ([`chapters/ch09-conclusion.tex`](./chapters/ch09-conclusion.tex), pp. 168–171, 4 pp.)

## How to Verify

```bash
/opt/homebrew/bin/tectonic main.tex && cp main.pdf TanStatisticalAndComputationalEfficiencyInSequentialDecisionMaking.pdf
```

## Open Items for Author Review (`\todoresolve{...}`)

- Replace placeholder dedication and acknowledgment in [`main.tex`](./main.tex) and verify committee member titles on the title page.
- Review dissertation abstract in [`main.tex`](./main.tex) (< 350 words).
- Review synthesis and chapter transitions in Chapters 1–8 (rendered in green under `\draftmarkuptrue`).
- Verify whether to keep Chapter 5 (Boosting & EBM Inference) or restrict solely to RL/POMP/POMDP chapters.
- Resolve the remaining Chapter 7 camera-ready items (`E3`/`E4`) flagged in [`chapters/ch08-pomdp-control.tex`](./chapters/ch08-pomdp-control.tex).
- When ready for final submission, set `\draftmarkupfalse` in [`macros.tex`](./macros.tex) and recompile.
