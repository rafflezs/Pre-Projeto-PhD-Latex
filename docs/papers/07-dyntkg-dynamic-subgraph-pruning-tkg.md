# Dynamic Subgraph Pruning and Causal-Aware Knowledge Distillation for Temporal Knowledge Graphs (DynTKG)

**Citation:** Liu, Q.; Feng, S.; Huang, M. Journal of King Saud University – Computer and Information Sciences 37:96 (2025). DOI 10.1007/s44443-025-00105-3. Received 5 Apr 2025, accepted 7 Jun 2025. BibTeX key: `liu2025dyntkg`.
**Source:** `Artigos/Dynamic subgraph pruning and causal-aware knowledge distillation for temporal knowledge graphs.pdf`
**Tier:** 2 (pruning methodology, temporal). **Relevance:** colleague 2/5, my optimization angle 3/5.

**Note:** the draft `docs/phase-1/2026-10-15-roteiro-pre-projeto.md` (line 64) cites this paper with an IEEE Xplore link; the DOI printed on the paper is 10.1007/s44443-025-00105-3, which the draft attaches to the multi-objective survey (line 68). See note 05.

## Problem and motivation
Temporal KG reasoning (entity and relation prediction over time) is expensive and has trouble with redundant historical events and semantic conflicts.

## Data and graph
Temporal KGs; the abstract mentions healthcare event prediction and financial case studies (benchmarks not yet extracted).

## Optimization lens
- **Decision:** which historical events to keep, via a **time-decay Hawkes process** that filters events and reconstructs critical temporal subgraphs.
- **Attention:** a gradient-sensitive graph attention reweights nodes by gradient norms to reduce semantic conflicts.
- **Compression:** **rule-guided contrastive knowledge distillation** from a hybrid neural-symbolic teacher to a light student.
- **Objective:** entity prediction accuracy and inference speed (a two-objective trade-off, not formalized as Pareto in the abstract).
- **Solver:** gradient-based training; the pruning is rule/intensity-driven (Hawkes), not a combinatorial solve.

## Evidence I have
Abstract-level claims: "notable improvements in entity prediction accuracy and inference speed", "causal path visualizations enhance interpretability". Numbers pending the full-text pass.

## Limitations
- Temporal focus; a germline genetic KG is mostly static (though family and test dates have time).
- Compression is tuned by hand; no explicit Pareto analysis in the abstract.

## Relevance
- **To OncoGeneGraph:** low-moderate. Shows pruning that **preserves dependencies** (a point the 01 draft makes) and a distillation option for deployment.
- **To my optimization angle:** moderate. A two-objective trade-off (accuracy vs. speed) that could be formalized as a Pareto problem.

## Ideas to borrow / open questions
- Use the time-decay as a **prior on the selection budget**, and compare to an explicit budgeted selection.

## Snowballing
- Backward: TKG reasoning (e.g., RE-NET, TLogic-style rule methods), Hawkes processes, knowledge distillation (Hinton et al. 2015).
- Forward: temporal KG pruning and distillation work from 2025–2026 (see `../phase-1/2026-10-15-snowballing.md`).
