# GALClean: Active Learning for Graphs with Noisy Structures

**Citation:** Chi, H.; Qi, C.; Wang, S.; Ma, Y. (NJIT; Penn State). Workshop paper at MLG @ KDD 2023 (venue inferred from the filename `MLG__KDD_2023_paper_9.pdf`; the PDF itself uses the ACM "Conference'17" template, so confirm the venue and any later full version). BibTeX key: `chi2023galclean`.
**Source:** `Artigos/MLG__KDD_2023_paper_9.pdf` (10 pages)
**Tier:** 2 (active learning under structural uncertainty). **Relevance:** colleague 3/5, optimization 3/5, chosen theme (cascade + DFL) 3/5.

**Correction to the old draft (`docs/phase-1/2026-10-15-roteiro-pre-projeto.md`):** the draft's `mlgworkshop.org/2023/papers/MLG__KDD_2023_paper_9.pdf` link was cited as "A Survey on Graph Neural Networks". That URL is this paper (GALClean), not a GNN survey. The draft also cited "Active Learning for Graphs with Noisy Structures" with a NeurIPS 2020 link; that NeurIPS link is the Graph Policy Network paper (note 15). The two links are swapped or misattributed.

## Problem and motivation
Graph active learning (AL) methods pick nodes to label using the graph topology (degree, GNN embeddings). Real graphs have noisy edges (here: heterophilous edges that connect nodes of different labels, from random noise or adversarial attacks). Selecting good nodes needs a clean graph, and cleaning the graph needs labels. The two tasks depend on each other.

## Data and graph
- Cora, Citeseer, Pubmed and other benchmarks (6 datasets in the main results), with random edge noise and unsupervised adversarial attacks at several perturbation ratios (5–20% in the figures).

## Optimization lens
- **Decision:** which B nodes to label (a fixed labeling budget), and which edges to keep (graph purification).
- **Objective:** node classification accuracy after spending the budget.
- **Procedure:** alternates (i) node selection with a noise-robust score that includes a **cleanliness score (C-Score)** and (ii) training an edge predictor on latent representations to purify the graph. The cleaned graph feeds the next selection round.
- **Theory:** the iteration is interpreted as **stochastic Expectation-Maximization (EM)**. GALClean+ runs a few extra EM iterations after the budget is spent.
- **Solver:** heuristic selection scores with gradient-trained GNN and edge predictor. No optimality guarantee for the selection.

## Evaluation (numbers verified in the extracted text)
- Table 1 (motivation): standard graph-AL methods (AGE, LSCALE, GRAIN, ALG) drop sharply from noise-free to perturbed graphs. For example, AGE goes from 77.07% (noise-free) to 52.74% on one perturbed Cora setting. Column alignment is garbled in extraction, so check the PDF before quoting a specific cell.
- Table 2 (C-Score ablation): with/without C-Score, Cora 70.40 ± 1.35% vs 69.21 ± 1.47%, Citeseer 67.65 ± 1.52% vs 64.37 ± 2.68%, Pubmed 75.76 ± 2.32% vs 73.31 ± 3.91%.
- Table 3: GALClean+ vs GALClean, Cora 70.40 vs 69.81, Citeseer 67.65 vs 65.99, Pubmed 75.76 vs 75.08. The authors themselves call the gain from the extra EM iterations "rather marginal".
- Main results are in figures (Figures 3–4); GALClean+ is reported to beat AGE, GRAIN, ALG and Random across noise ratios.

## Limitations
- Noise model = heterophilous edges. Missing edges (unknown relationships), which matter for pedigrees, are not the focus.
- Fixed uniform budget; no per-node cost.
- Benchmarks only (citation networks); main results shown as figures, so exact numbers are hard to cite.

## Relevance
- **To OncoGeneGraph:** moderate. Family links and variant–patient links in a real-world registry are noisy or uncertain. The colleague's link prediction for missing relationships is the "clean the graph" half of this loop.
- **To the chosen theme:** moderate. The paper's core insight, that **information acquisition and structure estimation are interdependent**, matches the phase-2 framing (separate what is observed from what is inferred; a predicted kinship link is not a confirmed one). The EM view is a useful formal baseline for "acquire labels and refine the graph" loops.

## Ideas to borrow / open questions
- Treat uncertain kinship edges as latent variables, and acquisition (testing a relative, clarifying a link) as the label query. Does EM-style alternation beat predict-then-optimize?
- Extend the noise model to **missing** edges, not only spurious ones.

## Snowballing
- Backward: AGE, LSCALE, GRAIN, ALG (graph-AL baselines); graph structure learning (Jin et al. KDD 2020, Pro-GNN); stochastic EM references.
- Forward: robust graph active learning 2024–2026; check for a full-length version of this paper.
