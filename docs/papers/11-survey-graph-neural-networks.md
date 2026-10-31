# A Survey on Graph Neural Networks

**Citation:** Zhang, X.; Li, S.; Li, H.; Gong, P.; Shi, J.; et al. IEEE Access (2026), DOI 10.1109/ACCESS.2026.3665657 (published 17 Feb 2026). BibTeX key: `zhang2026gnnsurvey`.
**Source:** `Artigos/A_Survey_on_Graph_Neural_Networks.pdf`
**Tier:** Background. **Relevance:** colleague 2/5, my optimization angle 2/5.

**Note on the draft:** `docs/phase-1/2026-10-15-roteiro-pre-projeto.md` (lines 54, 150) cites "A Survey on Graph Neural Networks" through `mlgworkshop.org/2023/papers/MLG__KDD_2023_paper_9.pdf`. That URL is GALClean, "Active Learning for Graphs with Noisy Structures" (note 14), not a survey. The survey PDF in the folder is this 2026 IEEE Access paper. Cite it by its DOI.

## Problem and motivation
Panorama of GNNs since 2022: architecture, optimization strategies, structural adaptations, applications, and open challenges (scalability, dynamic graphs, interpretability, integration with other AI paradigms).

## Optimization lens
Covers "optimization strategies" as a category; the section details were not read (full-text pass pending).

## Evidence
Survey. No experiments of its own.

## Limitations
- Broad coverage means shallow treatment of subgraph selection and pruning, which is the focus of this project.

## Relevance
- **To OncoGeneGraph:** background for the R-GCN and the scalability and interpretability challenges.
- **To my optimization angle:** background. Use it to frame where optimization enters GNN pipelines (training, architecture search, sampling).

## Ideas to borrow / open questions
- Use its challenge list (scalability, dynamic graphs, interpretability) to motivate the chosen theme in Phase 2.

## Snowballing
- The survey's own reference list is a good backward source for the GNN backbone papers (GCN, GAT, R-GCN, GraphSAGE).
