# Dissertation Handoff

## Title
*Statistical and Computational Efficiency in Sequential Decision Making*

## Current State
- Workspace initialized at `/Users/kevin/Library/CloudStorage/OneDrive-Personal/Documents/UMich/Research/dissertation`.
- Structure and paper selection confirmed with Kevin (**Spot 1**, 7 research chapters + Introduction and Conclusion = 9 chapters total).
- Algorithm naming rule: Do **not** use acronym names for algorithms (`DISC-GOLF`, `RAPPEL`, `HYRULE`, `SOLD`, `LOCAL-UCB`, `ProBALL-UCB`, `DOUHUA`, `NORA`, `Boulevard`, `DMOP`, `IFAD`, `PF-MCTQ`, etc.). Number algorithms sequentially within each chapter as **Algorithm 1**, **Algorithm 2**, **Algorithm 3**, and refer to them by plain descriptive names.
- Coauthorship rule: Credit each chapter's underlying paper(s) in the original source author order without individual contribution statements. Never guess first names from initials; use the verified author lists below.

## Verified Chapter Outline & Author Credits

1. **Chapter 1: Introduction** (`chapters/ch01-introduction.tex`)
2. **Chapter 2: Learning from Offline and Online Data** (`chapters/ch02-hybrid-rl.tex`)
   - *A Natural Extension to Online Algorithms for Hybrid RL with Limited Coverage* — Kevin Tan and Ziping Xu (RLJ / RLC 2024, `arXiv:2403.09701`). Local TeX: `/Users/kevin/.codex/.chatgpt-projects/g-p-69eaae8dcd6c8191b2061599e4c1f9a6/working/author_sources/2403.09701/main.tex`.
   - *Hybrid Reinforcement Learning Breaks Sample Size Barriers in Linear MDPs* — Kevin Tan, Wei Fan, and Yuting Wei (NeurIPS 2024, `arXiv:2408.04526`). Local TeX: `/Users/kevin/Downloads/Hybrid_RL_for_Linear_MDPs/`.
3. **Chapter 3: Learning Shared Structure from Heterogeneous Data** (`chapters/ch03-latent-bandits.tex`)
   - *Leveraging Offline Data in Linear Latent Contextual Bandits* — Chinmaya Kausik, Kevin Tan, and Ambuj Tewari (ICML 2024, `arXiv:2405.17324`).
4. **Chapter 4: Statistically and Computationally Efficient Actor–Critic Methods** (`chapters/ch04-actor-critic.tex`)
   - *Actor-Critics Can Achieve Optimal Sample Efficiency* — Kevin Tan, Wei Fan, and Yuting Wei (ICML 2025, `arXiv:2505.03710`). Local TeX: `/Users/kevin/Downloads/Hybrid_RL_for_Linear_MDPs/actor_critic_arxiv.tex`.
   - *Optimistic Actor-Critic with Parametric Policies for Linear Markov Decision Processes* — Max Qiushi Lin, Reza Asad, Kevin Tan, Haque Ishfaq, Csaba Szepesvári, and Sharan Vaswani (AISTATS 2026, `arXiv:2603.28595`). Local TeX: `/Users/kevin/.codex/.chatgpt-projects/g-p-69eaae8dcd6c8191b2061599e4c1f9a6/working/arxiv_sources/2603.28595/main.tex`.
5. **Chapter 5: Learning Continuous-Action Diffusion Policies** (`chapters/ch05-diffusion-policies.tex`)
   - *Learning Diffusion Policies with Sublinear Regret* — Kevin Tan, Zhihan Huang, and Yuting Wei (Nov 2026 clean manuscript). Local TeX: `/Users/kevin/.codex/.chatgpt-projects/g-p-6882989cbda881919061cabf18101c63/overleaf-github/main-clean.tex`.
6. **Chapter 6: Statistical Inference for Boosted Regression and Additive Models** (`chapters/ch06-boosting-inference.tex`)
   - *Statistical Inference for Gradient Boosting Regression* — Haimo Fang, Kevin Tan, and Giles Hooker (NeurIPS 2025, `arXiv:2509.23127`).
   - *Statistical Inference for Explainable Boosting Machines* — Haimo Fang, Kevin Tan, Jonathan Pipping, and Giles Hooker (AISTATS 2026, `arXiv:2601.18857`).
7. **Chapter 7: Parameter Estimation under Partial Observability** (`chapters/ch07-pomp-estimation.tex`)
   - *Automatic Differentiation to Improve Parameter Estimation for Partially Observed Markov Processes* — Kevin Tan, A. J. Abkemeier, Kunyang He, Giles Hooker, and Edward L. Ionides (JRSS-B R&R, `arXiv:2407.03085`). Local TeX: `/Users/kevin/Downloads/dmop-3/ms.tex` and `si.tex`.
8. **Chapter 8: Control under Partial Observability** (`chapters/ch08-pomdp-control.tex`)
   - *From POMDP Theory to Deep RL with Particle Filters* — Kevin Tan and Ziping Xu (NeurIPS 2026). Local PDF: `/Users/kevin/Downloads/control-main/Particle_Filtering_for_POMDP-8.pdf`; Linux repo: `kevtan-linux:/home/kevin/OneDrive/Documents/UMich/Research/pypomp/control`.
9. **Chapter 9: Conclusion** (`chapters/ch09-conclusion.tex`)

## Next Steps
1. Scaffold `main.tex`, `packages.tex`, `macros.tex`, and `references.bib`.
2. Pull the remaining 4 editable TeX sources (`2405.17324`, `2509.23127`, `2601.18857`, and the `pypomp/control` TeX source) into `sources/`.
3. Integrate Chapters 2–8 from the authoritative TeX sources with `Algorithm 1`, `Algorithm 2`, `Algorithm 3` numbering and draft Chapter 1 and Chapter 9.
