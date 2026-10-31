# Improving Graph Neural Networks by Combining Active Learning with Self-Training (STAL)

**Citation:** Katsimpras, G.; Paliouras, G. Data Mining and Knowledge Discovery 38, 110–127 (2024), published online Aug 2023. DOI 10.1007/s10618-023-00959-z. BibTeX key: `katsimpras2024stal`.
**Source:** `Artigos/Improving Graph Neural Networks by combining active learning with self-training.pdf`
**Tier:** 1 (core for label budgets). **Relevance:** colleague 4/5, my optimization angle 4/5.

**Correction to `docs/phase-1/2026-10-15-roteiro-pre-projeto.md` (line 148):** the draft links STAL to DOI `10.1145/3769107`. That DOI is for KGTrimmer (note 04). The correct DOI is `10.1007/s10618-023-00959-z`.

## Problem and motivation
GNNs need labels; labels are scarce and expensive, especially in health. Active learning (AL) picks uncertain nodes to label; self-training (ST) adds confident pseudo-labels. The paper combines them and checks whether the combination helps.

## Data and graph
- Cora (2,708 nodes; 10,556 edges; 7 classes), CiteSeer (3,327; 9,104; 6), PubMed (19,717; 88,648; 3), ogbn-arxiv (169,343; 1,166,243; 40).

## Optimization lens
- **Decision:** at each round, which unlabeled nodes to query (the most uncertain, under a budget); which pseudo-labels to add (the most confident).
- **Objective:** classification accuracy after a fixed number of queries, i.e. **accuracy per labeling budget**; implicitly, label cost is a fixed budget per round, not optimized.
- **Hyperparameters:** grid search (Table 2): learning rate {1e-2, 1e-3, 1e-4}; dropout {0, 0.3, 0.5, 0.8}; layers {2, 4, 6}; heads {2, 4}; hidden dimension {16, 32, 64, 128}.
- **Solver:** greedy selection by uncertainty; GNN trained with gradient descent.

## Method (short)
1. Train GNN on labeled set.
2. AL step: pick the most uncertain unlabeled nodes (variants in Table 3 labeled AL-ε, AL-QbC, AL-AGE; the meaning of ε to check in the method section).
3. ST step: add high-confidence pseudo-labels.
4. Repeat.

## Evaluation (Table 3, accuracy %, mean ± std, excerpt)
- GCN baseline: Cora 77.7, CiteSeer 63.3, PubMed 75.0, ogbn-arxiv 61.6.
- STAL-ε: Cora 78.9, CiteSeer **67.9**, PubMed 76.0, ogbn-arxiv 62.5.
- Several gains are within one standard deviation (e.g., Cora). Read the whole table before claiming significance.

## Limitations
- Benchmarks are citation networks, not clinical or heterogeneous KGs.
- Budget is a fixed number of queries; there is no cost-aware or budgeted optimization (e.g., per-node labeling cost).
- Greedy uncertainty selection has no optimality guarantee; gains are modest and noisy on several datasets.

## Relevance
- **To OncoGeneGraph:** moderate-high. The variant-classification or VUS-reclassification problem is a labeling-budget problem; STAL is a baseline for "which variant to curate next".
- **To my optimization angle:** high. It frames label acquisition as a sequential decision with a budget but does not optimize it as one. The gap: **budgeted, cost-aware selection with guarantees** (ILP or submodular maximization, where each label has a different cost).

## Ideas to borrow / open questions
- Replace greedy uncertainty with **submodular coverage under a budget** (greedy has a (1-1/e) guarantee) and compare on the same benchmarks.
- Add a per-node cost to the formulation (curation time, expert cost) and optimize for accuracy per cost.

## Snowballing
- Backward (names as cited in the paper's related work; confirm in its reference list before citing): active learning on graphs, self-training with pseudo-labels (Li et al. 2018; Wang et al. 2021; Dai et al. 2021), GCN (Kipf & Welling 2017).
- Forward: active learning for GNNs with noisy structures (now note 14, GALClean), graph policy networks for AL (now note 15, GPA), budgeted AL with guarantees (note 16, AIM), and budgeted AL in clinical graphs (see `../phase-1/2026-10-15-snowballing.md`).
