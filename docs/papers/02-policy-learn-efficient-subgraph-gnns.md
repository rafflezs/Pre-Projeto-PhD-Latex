# Efficient Subgraph GNNs by Learning Effective Selection Policies

**Citation:** Bevilacqua, B.; Eliasof, M.; Ribeiro, B.; Meirom, E.; Maron, H. ICLR 2024 (arXiv:2310.20082v2). BibTeX key: `bevilacqua2024policylearn`.
**Source:** `Artigos/Efficient Subgraph GNNs by Learning Effective Selection Policies.pdf` (27 pages)
**Tier:** 1 (core). **Relevance:** colleague 2/5, my optimization angle 5/5.

## Problem and motivation
Subgraph GNNs are more expressive than message-passing GNNs, but they process a *bag* of subgraphs, which is expensive. The problem: learn to select a small subset of subgraphs that is nearly as informative as the full bag.

## Data and graph
- ZINC-12K (molecules), REDDIT-BINARY (large graphs, where full-bag Subgraph GNNs run out of memory), and other graph classification benchmarks.

## Optimization lens
- **Decision:** a subset of subgraphs from the bag, built **sequentially** by a selection policy.
- **Objective:** downstream task loss (MAE on ZINC, accuracy on REDDIT-BINARY), under a fixed **parameter budget** (500k on ZINC).
- **Theory:** they prove families of WL-indistinguishable graphs where small "efficient" subsets of subgraphs already distinguish all graphs in the family; random policies fail, learned policies succeed.
- **Solver:** the selection is *discrete*, made differentiable by a **Gumbel-softmax** relaxation (Jang et al., 2016; Maddison et al., 2017). The selection network is itself a Subgraph GNN.

## Method (short)
Iteratively pick subgraphs with a learned policy; each step conditions on what was already selected; train end-to-end through the Gumbel relaxation.

## Evaluation
- ZINC (Table 1): GCN 0.321, GIN 0.163, PNA 0.133, the best efficient baseline ~0.101 ± 0.010 for POLICY-LEARN (row label garbled in text extraction; verify in the PDF before quoting).
- REDDIT-BINARY (Table 2): Policy-Learn is the best among efficient baselines; full-bag Subgraph GNNs report OOM.

## Limitations
- Results are on graph-level tasks (molecules, social graphs), not on KG link prediction or node classification.
- Gumbel relaxation introduces training noise and temperature hyperparameters; the sensitivity analysis is not reviewed yet.
- Performance is compared mainly against efficient subgraph baselines; no comparison against exact or combinatorial selection.

## Relevance
- **To OncoGeneGraph:** low directly (graph-level tasks). Indirect: subgraph efficiency for R-GCN on a patient/family KG.
- **To my optimization angle:** high. It formalizes subgraph selection as **budgeted discrete optimization** and solves it with a relaxation. The natural question for you (OR background): what is the exact or certified alternative (ILP, greedy with guarantees)?

## Ideas to borrow / open questions
- Compare the Gumbel-policy selector to an **ILP** (max coverage under a size budget) on a small KG, to measure the optimality gap.
- The "efficient policy exists" theorem suggests a notion of **minimum sufficient subgraph** worth formalizing for KGs.

## Snowballing
- Backward: Subgraph GNN papers (Zhang & Li 2021; Cotta et al. 2021; Papp et al. 2021; Bevilacqua et al. 2022; Frasca et al. 2022), OSAN (Qian et al. 2022), Gumbel-softmax (Jang 2016; Maddison 2017).
- Forward: follow-up work on learned subgraph selection and expressive subgraph GNNs (see `../phase-1/2026-10-15-snowballing.md`).
