# Multi-objective Deep Learning: Taxonomy and Survey of the State of the Art

**Citation:** Peitz, S.; Hotegni, S. S. arXiv:2412.01566v2 (3 Dec 2024). Venue: not stated in the preprint I read (check the published version). BibTeX key: `peitz2024multiobjective`.
**Source:** `Artigos/Multi-objective Deep Learning: Taxonomy and Survey of the State of the Art.pdf` (18 pages)
**Tier:** 1 (core, optimization framing). **Relevance:** colleague 2/5, my optimization angle 5/5.

**Correction to `docs/phase-1/2026-10-15-roteiro-pre-projeto.md` (line 68):** the draft cites this survey with DOI `10.1007/s44443-025-00105-3`. That DOI belongs to the DynTKG paper (see note 07). The correct identifier for this survey is arXiv:2412.01566.

## Problem and motivation
Machine learning routinely has conflicting criteria (accuracy vs. sparsity vs. cost, multi-task losses, multi-criteria hyperparameter tuning). Multi-objective optimization is costlier than single-objective, and deep learning (huge parameter counts, non-linearities, stochastic gradients) makes it harder. The survey gives a taxonomy and a state of the art across supervised, unsupervised, reinforcement and generative learning.

## Data and graph
Not applicable (survey).

## Optimization lens (the core of this paper for you)
- **Formulation:** multi-objective problem (MOP) over parameters θ with losses L(θ) = (L_1(θ), …, L_K(θ)). The Pareto set P and the Pareto front PF = L(P) are defined in the standard way (non-dominated points).
- **Taxonomy of training procedures (their Figure 6):**
  - *Scalarization*: parameter-dependent (actively chosen weights) vs. accepting any Pareto-optimal point. Scalarizing turns the problem into a single-objective problem (weighted sum or other scalarizations); this is the most common approach.
  - *Gradient-based multi-objective methods*: multiple-gradient descent algorithms (MGDA) find a common descent direction; used for high-dimensional problems.
  - *Set-based / front-based methods*: approximate the whole Pareto front, e.g. via **hypervolume maximization**; decision-maker preferences guide which region of the front to target.
- **Decision-maker needs** are an explicit axis of the taxonomy (a point, a front, or a preference region).
- **Solver:** mostly gradient-based or evolutionary/search-based, depending on the category.

## Evaluation
Survey: no experiments of its own. It lists applications across paradigms.

## Limitations (of the survey, and for my use)
- Deep-learning focus; the discussion of exact or combinatorial methods is limited (most MOO for DL is gradient-based or evolutionary). This is the **gap** an OR-background project could address.
- Hypervolume and front-quality metrics are described but not benchmarked on the KG/graph tasks in question.

## Relevance
- **To OncoGeneGraph:** low to moderate. Useful to justify a multi-objective formulation (e.g., AUC vs. calibration vs. graph size in her R-GCN).
- **To my optimization angle:** very high. It is the best reference in the folder for the vocabulary (scalarization, Pareto, hypervolume, MGDA, decision-maker preferences) and for positioning the thesis against deep-learning-specific MOO.

## Ideas to borrow / open questions
- Use the taxonomy to classify each paper in `../phase-1/2026-10-15-themes.md` (which MOO family does each approach use?).
- Propose a **constrained** formulation (ε-constraint) as an alternative to scalarization where clinical constraints are hard.
- Check whether any surveyed method solves **exact** discrete selection problems (subgraphs, label budgets). If not, that is a gap.

## Snowballing
- Backward: MGDA (Désidéri 2012), hypervolume references, multi-task learning surveys (cited in the paper).
- Forward: multi-objective methods for GNNs, multi-objective hyperparameter optimization for deep learning, Pareto-based model selection in healthcare (see `../phase-1/2026-10-15-snowballing.md`).
