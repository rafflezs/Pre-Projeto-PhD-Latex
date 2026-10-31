# Knowledge Graph Pruning for Recommendation (KGTrimmer)

**Citation:** Lin, F.; Zhu, X.; Zhao, Z.; Huang, D.; Yu, Y.; Li, X.; Zheng, Z.; Xu, T.; Chen, E. ACM Transactions on Information Systems 44(1), Art. 20, Nov 2025. DOI 10.1145/3769107. BibTeX key: `lin2025kgtrimmer`.
**Source:** `Artigos/Knowledge Graph Pruning for Recommendation.pdf` (28 pages)
**Tier:** 1 (core). **Relevance:** colleague 3/5, my optimization angle 4/5.

## Problem and motivation
Knowledge-graph-based recommender systems are slow to train because of "knowledge explosion". Earlier pruning and summarization either look only at KG structure, ignoring the recommendation task, or merge real nodes into virtual ones that lose collaborative signal.

## Data and graph
- Amazon-Book (70,679 users; 24,915 items; KG with 88,572 entities, 39 relations, 2,557,746 triplets).
- Last-FM (23,566 users; KG 58,266 entities, 9 relations).
- Alibaba-Fashion (114,737 users; KG 59,156 entities, 51 relations).

## Optimization lens
- **Decision:** which KG nodes to remove, via a **learned global mask** (holistic view) and a **collective importance score** from user attention (collective view). Pruning is soft and learned end-to-end.
- **Objective:** the recommendation loss on the pruned KG, with the expectation that accuracy is maintained while training cost falls. The paper frames this as "remove unessential nodes while minimizing performance degradation".
- **Constraints:** none explicit; the pruning level is an experimental variable.
- **Solver:** end-to-end gradient training of an "importance-aware graph neural network".

## Method (short)
1. Dual-view importance evaluator: collective (community consensus from collaborative signals) + holistic (learned global mask from node properties and popularity).
2. Aggregate both into an importance score per entity.
3. Build an importance-aware GNN that injects the filtered knowledge into the recommender.

## Evaluation
- Baselines include KG-only pruning and noise-robust KG recommenders (e.g., KRDN).
- The text reports that when pruning is light (90% on Amazon-Book, 30% on Last-FM and Alibaba-Fashion, as written in the results discussion — check the exact meaning of the ratio in the table), baselines remain comparable; with heavier pruning, KGTrimmer clearly wins because the collaborative signal is kept.
- Statistical significance is reported at p < 0.01 (t-test).

## Limitations (from text and my reading)
- Recommender domain; the "importance" depends on collaborative signals that a clinical KG does not have.
- Relies on user–item interaction data; the equivalent for a germline/phenotype KG is unclear.
- Pruning ratio semantics and the cost of the global mask need checking in the full text.

## Relevance
- **To OncoGeneGraph:** moderate. Shows importance-driven KG pruning with measurable training speed-up. The task signal (collaborative) must be replaced by a clinical one (e.g., variant–patient links, cascade results).
- **To my optimization angle:** high. The paper frames pruning as a **trade-off between efficiency and accuracy** with no explicit Pareto analysis. A natural extension is to make that trade-off explicit (Pareto over accuracy and graph size).

## Ideas to borrow / open questions
- Replace the learned global mask with an explicit **knapsack or budgeted selection** over node importance scores.
- Test the "keep the collaborative signal" idea with a clinical analogue: keep nodes that support family-level evidence.

## Snowballing
- Backward: graph sparsification references in the paper (their refs 8, 22, 49, 51); KG-based recommenders; knowledge explosion literature.
- Forward: KG pruning and sparsification for recommenders and clinical KGs from 2025–2026 (see `../phase-1/2026-10-15-snowballing.md`).
