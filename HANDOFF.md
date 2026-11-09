# Handoff: Kevin Tan Ph.D. Dissertation

## Current State

- **Title**: *Statistical and Computational Efficiency in Sequential Decision Making*
- **Template**: Official 2026 University of Pennsylvania Ph.D. Dissertation LaTeX template ([`upennstyle.sty`](./upennstyle.sty), [`main.tex`](./main.tex), [`macros.tex`](./macros.tex), [`references.bib`](./references.bib)).
- **GitHub Repository**: `https://github.com/hetankevin/dissertation` (`main` branch).
- **Draft Markup Mode (`\draftmarkuptrue` in [`macros.tex`](./macros.tex))**:
  - **Black text**: Verbatim manuscript text from the underlying papers.
  - **Green text (`\aigen{...}` and `\begin{aigenblock}...\end{aigenblock}`)**: AI-generated prose (Chapter 1 Introduction, Chapter 9 Conclusion, chapter-opening coauthorship/bridge paragraphs, multi-paper transition sections in Chapters 2, 4, and 6, Chapter 8 camera-ready experimental additions, and all plain/numbered algorithm replacements `Algorithm 1`, `Algorithm 2`, `Algorithm 3`).
  - **BOLD RED ALL-CAPS (`\todoresolve{...}`)**: Caveats, placeholders, and open decisions to resolve before final submission.
  - Set `\draftmarkupfalse` in [`macros.tex`](./macros.tex) to compile a clean black-text version without `[RESOLVE: ...]` banners.

## Chapter & Appendix Inventory

1. **Chapter 1: Introduction** ([`chapters/ch01-introduction.tex`](./chapters/ch01-introduction.tex))
   - Synthesizes the dissertation's unifying theme (how the representation and use of information determine both the statistical and computational costs of sequential learning, inference, and control), roadmap, and chapter-by-chapter overview.
2. **Chapter 2: Learning from Offline and Online Data** ([`chapters/ch02-hybrid-rl.tex`](./chapters/ch02-hybrid-rl.tex), Appendix A [`appendices/app02-hybrid-rl.tex`](./appendices/app02-hybrid-rl.tex))
   - Part I: *A Natural Extension to Online Algorithms for Hybrid RL with Limited Coverage* — **Kevin Tan and Ziping Xu** (RLJ / RLC 2024, `arXiv:2403.09701`) [Algorithm 1].
   - Part II: *Hybrid Reinforcement Learning Breaks Sample Size Barriers in Linear MDPs* — **Kevin Tan, Wei Fan, and Yuting Wei** (NeurIPS 2024, `arXiv:2408.04526`) [Algorithms 2 and 3].
3. **Chapter 3: Learning Shared Structure from Heterogeneous Data** ([`chapters/ch03-latent-bandits.tex`](./chapters/ch03-latent-bandits.tex), Appendix B [`appendices/app03-latent-bandits.tex`](./appendices/app03-latent-bandits.tex))
   - *Leveraging Offline Data in Linear Latent Contextual Bandits* — **Chinmaya Kausik, Kevin Tan, and Ambuj Tewari** (ICML 2024, `arXiv:2405.17324`) [Algorithms 1, 2, and 3].
4. **Chapter 4: Statistically and Computationally Efficient Actor–Critic Methods** ([`chapters/ch04-actor-critic.tex`](./chapters/ch04-actor-critic.tex), Appendix C [`appendices/app04-actor-critic.tex`](./appendices/app04-actor-critic.tex))
   - Part I: *Actor-Critics Can Achieve Optimal Sample Efficiency* — **Kevin Tan, Wei Fan, and Yuting Wei** (ICML 2025, `arXiv:2505.03710`) [Algorithms 1–8].
   - Part II: *Optimistic Actor-Critic with Parametric Policies for Linear Markov Decision Processes* — **Max Qiushi Lin, Reza Asad, Kevin Tan, Haque Ishfaq, Csaba Szepesvári, and Sharan Vaswani** (AISTATS 2026, `arXiv:2603.28595`) [Algorithms 9–11].
5. **Chapter 5: Learning Continuous-Action Diffusion Policies** ([`chapters/ch05-diffusion-policies.tex`](./chapters/ch05-diffusion-policies.tex), Appendix D [`appendices/app05-diffusion-policies.tex`](./appendices/app05-diffusion-policies.tex))
   - *Learning Diffusion Policies with Sublinear Regret* — **Kevin Tan, Zhihan Huang, and Yuting Wei** (Working paper, 2026) [Algorithms 1, 2, and 3].
6. **Chapter 6: Statistical Inference for Boosted Regression and Additive Models** ([`chapters/ch06-boosting-inference.tex`](./chapters/ch06-boosting-inference.tex), Appendix E [`appendices/app06-boosting-inference.tex`](./appendices/app06-boosting-inference.tex))
   - Part I: *Statistical Inference for Gradient Boosting Regression* — **Haimo Fang, Kevin Tan, and Giles Hooker** (NeurIPS 2025, `arXiv:2509.23127`) [Algorithms 1 and 2].
   - Part II: *Statistical Inference for Explainable Boosting Machines* — **Haimo Fang, Kevin Tan, Jonathan Pipping, and Giles Hooker** (AISTATS 2026, `arXiv:2601.18857`) [Algorithm 3].
7. **Chapter 7: Parameter Estimation under Partial Observability** ([`chapters/ch07-pomp-estimation.tex`](./chapters/ch07-pomp-estimation.tex), Appendix F [`appendices/app07-pomp-estimation.tex`](./appendices/app07-pomp-estimation.tex))
   - *Automatic Differentiation to Improve Parameter Estimation for Partially Observed Markov Processes* — **Kevin Tan, A. J. Abkemeier, Kunyang He, Giles Hooker, and Edward L. Ionides** (JRSS-B R&R, `arXiv:2407.03085`) [Algorithms 1, 2, and 3].
8. **Chapter 8: Control under Partial Observability** ([`chapters/ch08-pomdp-control.tex`](./chapters/ch08-pomdp-control.tex), Appendix G [`appendices/app08-pomdp-control.tex`](./appendices/app08-pomdp-control.tex))
   - *From POMDP Theory to Deep RL with Particle Filters* — **Kevin Tan and Ziping Xu** (NeurIPS 2026) [Algorithm 1 + Appendix G Algorithms].
9. **Chapter 9: Conclusion** ([`chapters/ch09-conclusion.tex`](./chapters/ch09-conclusion.tex))

## Open Items / Caveats Marked with `\todoresolve{...}` (RED ALL CAPS)

1. **Front Matter ([`main.tex`](./main.tex))**:
   - Replace placeholder Dedication and Acknowledgment with personal text.
   - Verify full committee member list and titles on the Title Page (currently Co-Supervisors Giles Hooker and Yuting Wei, Committee Member Enric Boix-Adserà, Graduate Group Chair Bhaswar B. Bhattacharya).
   - Review the AI-drafted dissertation abstract (rendered in green).
2. **Chapter 1 & Chapter 9 ([`chapters/ch01-introduction.tex`](./chapters/ch01-introduction.tex), [`chapters/ch09-conclusion.tex`](./chapters/ch09-conclusion.tex))**:
   - Review AI-drafted synthesis and chapter transitions (rendered in green).
3. **Chapter 3 ([`chapters/ch03-latent-bandits.tex`](./chapters/ch03-latent-bandits.tex))**:
   - Confirm whether Section 3.7 (de Finetti theorem for stateless decision processes) should stay in the main chapter or move to Appendix B.
4. **Chapter 6 ([`chapters/ch06-boosting-inference.tex`](./chapters/ch06-boosting-inference.tex), [`appendices/app06-boosting-inference.tex`](./appendices/app06-boosting-inference.tex))**:
   - Confirm whether to keep Chapter 6 at Spot 6 (bridging iterative functional approximation and statistical inference) or omit it if restricting solely to RL/bandit/POMDP chapters.
   - Supply `plots/ne_100_lr_0.3_md_4_sr_0.6_dr_0.6.png` for Figure E.8 in Appendix E (missing from the `arXiv:2509.23127` source tarball).
5. **Chapter 8 ([`chapters/ch08-pomdp-control.tex`](./chapters/ch08-pomdp-control.tex))**:
   - Confirm exact config diff between initial and stabilized MuJoCo Ant runs (`UTD 1/10` + online model updates + weight decay) and notation distinguishing state-level rollout horizon $L$ from belief-tree depth $d=0$.
