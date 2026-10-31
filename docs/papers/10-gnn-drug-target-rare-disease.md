# Graph Neural Networks for Predicting Drug-Target Interactions in Rare Disease

**Citation:** Zangana, H. M.; Saeed, D. S.; Rasheed, H. H.; Mohammed, D.; Jones, R. K. International Journal of Artificial Intelligence & Robotics (IJAIR) 8(1), 2026, pp. 50–63. Received Jun 2026, accepted 27 Jul 2026, published 31 Jul 2026 (per article history). BibTeX key: `zangana2026dti`.
**Source:** `Artigos/ Graph Neural Networks for Predicting Drug-Target Interactions in Rare Disease .pdf` (14 pages; the filename has leading and trailing spaces)
**Tier:** 2 (domain match: rare disease, sparse data). **Relevance:** colleague 4/5, my optimization angle 2/5.

## Problem and motivation
Rare diseases have little biological data and sparse drug–target interaction (DTI) information, so standard GNNs degrade. The paper proposes a GNN for DTI prediction robust to sparsity.

## Data and graph
- Heterogeneous biomedical knowledge graphs from DrugBank, Orphanet and UniProt, at three sparsity levels (moderate, high, extreme).

## Optimization lens
- **Components:** self-supervised **graph contrastive learning** (node dropping and edge masking as augmentations) and a **rare-disease-aware edge-reweighting** mechanism that increases the influence of disease-specific edges during message passing.
- **Objective:** contrastive loss plus the prediction loss (binary cross-entropy style, MLP decoder). The weighting between them is a training hyperparameter (temperature 0.5 for the contrastive term).
- **Solver:** gradient-based. Edge reweighting is a learned or heuristic weight, not a constrained selection.

## Evaluation (abstract)
- AUROC **0.932 / 0.904 / 0.859** and AUPRC **0.871 / 0.835 / 0.748** under moderate, high and extreme sparsity, outperforming baseline methods.

## Limitations (from the paper)
- Evaluation on computational benchmarks and public databases; predicted interactions need experimental validation.
- No clinical validation.

## Relevance
- **To OncoGeneGraph:** moderate-high. The sparsity regime (few positives, rare disease) is close to her cohort concerns (she already plans few-shot or graph-transfer fallbacks if the cohort is small).
- **To my optimization angle:** low-moderate. The reweighting is a hand-designed weight, a candidate to replace with an **optimized** weighting (bilevel or constrained).

## Ideas to borrow / open questions
- Treat the rare-disease edge weights as **decision variables** under a sparsity budget, and compare to the fixed heuristic.
- Contrastive augmentations as a source of data for the sparse regime (could complement active learning, theme A).

## Snowballing
- Backward: graph contrastive learning (GraphCL, GRACE), edge reweighting, DTI benchmarks (DrugBank, Orphanet).
- Forward: GNNs for rare-disease KGs (see `../phase-1/2026-10-15-snowballing.md`).
