# Less is More: One-shot-subgraph Link Prediction on Large-scale Knowledge Graphs

**Citation:** Zhou, Z.; Zhang, Y.; Yao, J.; Yao, Q.; Han, B. ICLR 2024 (arXiv:2403.10231v1). BibTeX key: `zhou2024oneshot`.
**Source:** `Artigos/Less is More: One-shot-subgraph Link Prediction on Large-scale Knowledge Graphs .pdf` (32 pages; text extracted, figure text partly garbled)
**Tier:** 1 (core). **Relevance:** colleague 4/5, my optimization angle 4/5.

## Problem and motivation
Structural link predictors score every entity in the whole KG for each query, which does not scale. The paper decouples prediction into (i) extracting **one query-dependent subgraph** and (ii) predicting on that subgraph only.

## Data and graph
Five large-scale KG benchmarks (names to confirm in the experimental section; full-text pass pending).

## Optimization lens
- **Decision:** the subgraph for a query (u, r, ?), built by sampling from a **Personalized PageRank** (PPR) distribution around the query entity u. Subgraph size is a controlled ratio (r_V, the fraction of entities kept).
- **Objective:** joint training of sampler and predictor so that the subgraph keeps the answer and the supporting evidence; the paper emphasizes avoiding trivial solutions.
- **Automated configuration search:** the data-space and model-space hyperparameters (subgraph scale, number of layers, etc.) are tuned with **Bayesian optimization using a random-forest surrogate** (Bergstra et al., 2013; Hutter et al., 2011), because the search space is discrete and mixed.
- **Solver:** PPR is a non-parametric heuristic; the predictor is trained by gradient descent; hyperparameters by BO.

## Method (short)
1. For a query, compute PPR from the source entity; keep the top subgraph.
2. Run a GNN predictor on that single subgraph.
3. Use BO with an RF surrogate to pick subgraph scale and predictor depth.

## Evaluation and evidence I have
- Ablation (training with varying scales and layers): using all entities (rVq = 1.0) "degenerates" prediction, since too many irrelevant entities are covered; deeper predictors with a larger L consistently do better, which motivates learning a deeper predictor on small subgraphs.
- Efficiency and performance claims on five benchmarks; numbers not yet extracted (full-text pass pending).

## Limitations
- The sampler is heuristic (PPR), so optimality of the subgraph is not guaranteed.
- BO over the configuration space is expensive; the cost is not reported in the parts I read.
- Link prediction on KGs with a fixed query template; no temporal or ontological constraints.

## Relevance
- **To OncoGeneGraph:** high. Link prediction (patient–family, patient–variant) is one of her two tasks. The subgraph-per-query idea fits a patient-centred retrieval for R-GCN or GraphRAG.
- **To my optimization angle:** high. It is the best example in the folder of an **explicit configuration optimization** (BO with RF surrogate) and of a **sampling-as-optimization** choice (PPR as a heuristic that could be replaced by a budgeted selection).

## Ideas to borrow / open questions
- Replace PPR top-k with a **budgeted coverage problem** (max expected evidence coverage subject to subgraph size) and measure the gain.
- Use BO (already in the paper) as the baseline for tuning my own selection budgets.

## Snowballing
- Backward: PPR (Page et al. 1999; Jeh & Widom 2003), BO (Bergstra 2013; Hutter 2011), path-based KG reasoning (Das et al. 2017; Sadeghian et al. 2019).
- Forward: subgraph-based KG completion and efficient link prediction papers from 2024–2026 (see `../phase-1/2026-10-15-snowballing.md`).
