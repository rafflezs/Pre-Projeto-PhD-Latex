# Cost-effective Data Labelling for Graph Neural Networks (AIM)

**Citation:** Anonymous authors. 2023. Anonymized submission; the text names the track "Graph Algorithms and Modeling for the Web", which points to The Web Conference (WWW). The filename `153_Cost_effective_Data_Labell.pdf` looks like a submission ID. **Find the published version and its authors before citing.** BibTeX key (provisional): `anon2023aim`.
**Source:** `Artigos/153_Cost_effective_Data_Labell.pdf` (12 pages, with line numbers)
**Tier:** 1 (budgeted selection with an approximation guarantee). **Relevance:** colleague 3/5, optimization 5/5, chosen theme (cascade + DFL) 4/5.

## Problem and motivation
GNN-based active learning methods are usually:
1. **Supervised:** they need the GNN and the labels of newly selected nodes inside the loop, often with a "warm-up" labeled set.
2. **Model-specific:** the selection is tied to one GNN, so labels cannot be reused for other GNNs or tasks.
3. **Not scalable:** they retrain models or do expensive matrix operations.

The paper wants AL that is **unsupervised** (no warm-up, no labels during selection), **flexible** (works for any message-passing GNN) and **scalable**.

## Data and graph
Cora (2,708 nodes), CiteSeer (3,327), PubMed (19,717), Coauthor-Physics (34,493), Flickr (89,250), ogbn-arxiv (169,343) (their Table 6).

## Optimization lens (the core of this paper)
- **Reformulation:** AL becomes the **Aggregation Involvement Maximization (AIM)** problem. Select B seed nodes so that the aggregated features (the neighborhoods that message passing combines) of the selected seeds are as diverse and representative as possible. This uses only the shared structure of GNNs (multi-layer aggregation), not a specific model.
- **Decision:** a seed set S with |S| = B (cardinality budget).
- **Complexity:** AIM is proved **NP-hard**.
- **Structure:** the objective is **monotone and submodular**.
- **Algorithm:** greedy selection with **early termination** (called GreedyET in the tables), with the classical **(1 − 1/e) approximation ratio**.
- **Design choice backed by data:** their Tables 1 and 2 show that similar node pairs are mostly directly connected and that neighborhood size grows quickly with hops, so 1-hop neighborhoods are used.

## Evaluation (as stated in the contributions; verify against the result tables)
- Up to **19.4% higher accuracy** than prior methods; up to **five orders of magnitude** faster; up to **102.4× less memory**.
- Flexibility (Table 3, budget 20C, i.e., 20 nodes per class): GreedyET gets the best accuracy across GCN, APPNP, GraphSAGE and SGC on Cora and CiteSeer. Example: Cora with GCN, 84.0 vs 81.2 (AGE), 81.1 (MAB), 81.3 and 81.5 (GRAIN variants).

## Limitations
- The authors note that it does not support incremental computation on dynamic graphs.
- Uniform node cost (cardinality constraint), not a knapsack budget.
- The objective is a proxy (feature-aggregation coverage). It is not tied to the downstream decision or loss, so it is a "predict-agnostic" selection.
- Anonymous version; final numbers may differ in the published paper.

## Relevance
- **To OncoGeneGraph:** moderate. A model-agnostic selection fits a project where the GNN (R-GCN or alternatives) may change, and labels should be reusable.
- **To the chosen theme:** high, as a method template. It is the clearest example in the set of the OR pattern the thesis wants: reformulate an ML acquisition problem as a combinatorial problem, prove its hardness, find structure (submodularity), and give an algorithm with a guarantee.
- The contrast with GPA (note 15) is useful for the thesis: AIM is static, bounded and decision-agnostic; GPA is sequential, learned and has no bound. A cascade-testing formulation sits between them (sequential, with costs, ideally with bounds).

## Ideas to borrow / open questions
- Replace the cardinality constraint with a **knapsack constraint** (per-relative cost). Greedy for monotone submodular maximization under a knapsack constraint still has constant-factor guarantees, with modified rules.
- Is the expected number of carriers detected in a pedigree submodular in the set of tested relatives? If tests on related relatives give overlapping information, diminishing returns are plausible, but it needs a proof or a counterexample.
- Adaptive submodularity (Golovin & Krause 2011) covers the sequential case, where each test result is observed before the next choice. Check this line for cascade testing.

## Snowballing
- Backward: influence maximization and submodular optimization (Kempe et al. 2003; Nemhauser et al. 1978), GRAIN (feature-influence AL), AGE, ANRMAB.
- Forward: find the published version; follow its citing papers on scalable graph AL.
- Theory to add: adaptive submodularity (Golovin & Krause, JAIR 2011); submodular maximization under knapsack constraints.
