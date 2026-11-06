# A fast Quasi-Bayes recursive procedure for Hierarchical Dirichlet processes

MSc thesis in Economic and Social Sciences, Bocconi University, A.Y. 2024/2025.
Advisor: Prof. Sonia Petrone. Author: Matteo Almici.

**Read the thesis:** [Almici_MSc_Thesis_Quasi-Bayes_HDP.pdf](Almici_MSc_Thesis_Quasi-Bayes_HDP.pdf) (94 pages)

## TL;DR

Newton's recursive algorithm gives fast, online density estimation for Dirichlet process mixtures, but it has no obvious extension to grouped data. This thesis builds one: **Newton-HDP**, a recursive procedure for Hierarchical Dirichlet process (HDP) mixtures, where groups borrow strength from each other through a shared global estimate.

## Questions addressed

1. Can we build a recursive algorithm for HDP mixtures that keeps the simplicity of Newton's recursion while allowing borrowing of strength across groups?
2. Does it admit a quasi-Bayesian interpretation, i.e. is the model it implies asymptotically partially exchangeable?
3. How does its one-step predictive rule compare to exact HDP inference, and where does the approximation come from?

## Main contributions

- **Newton-HDP algorithm.** Group-level estimates and a global estimate are coupled through a feedback loop that mirrors the HDP hierarchy. Cost is O(NJK), versus O(N^2 * C_MCMC) for exact inference (N observations, J groups, K components).
- **Information loss analysis** of the algorithm relative to exact HDP inference, using the exact one-step predictive of the Chinese Restaurant Franchise as a benchmark.
- **Empirical evaluation** against independent Newton recursions and a collapsed Gibbs sampler, in balanced, unbalanced and heterogeneous settings.
- **Theory.** Under some assumptions, almost sure convergence of the group and global estimates (Theorem 7.2) and asymptotic partial exchangeability of the implied array (Theorem 7.3).
- **Two empirical additions for Newton's algorithm:** a clustering procedure based on the modal structure of the density estimate, and a warm start with a preliminary Gibbs step to reduce sensitivity to the data ordering.

## Structure

| Chapter | Content |
|---|---|
| 1 | Exchangeability, de Finetti, Bayesian predictive approach, Dirichlet process |
| 2 | Newton's recursions as a quasi-Bayes procedure |
| 3 | Warm start and clustering performance of Newton's algorithm |
| 4 | Partial exchangeability and the Hierarchical Dirichlet process |
| 5 | Newton-HDP: algorithm and information losses |
| 6 | Empirical evaluation |
| 7 | Quasi-Bayes properties of Newton-HDP |

## Keywords

Bayesian nonparametrics, quasi-Bayes, predictive approach, Hierarchical Dirichlet process, partial exchangeability, recursive estimation, density estimation.

## Notes

The simulation code is not included in this repository yet. In the thesis, I declare the use of Claude as an assistant for language, LaTeX transcription, checking computations and debugging code; I reviewed everything and take full responsibility for the final text.

## Contact

[LinkedIn](https://www.linkedin.com/in/matteo-almici-matt2001/)
