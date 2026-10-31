# RareNet: Knowledge Graph Sparsification for GNN-based Rare Disease Diagnosis

**Citation:** Cara, P.; Zaripova, K.; Bani-Harouni, D.; Navab, N.; Farshad, A. arXiv:2510.08655 (v1, 9 Oct 2025). TUM / MCML. BibTeX key: `cara2025rarenet`.
**Source:** `Artigos/Knowledge Graph Sparsification for GNN-based Rare Disease Diagnosis.pdf` (11 pages)
**Tier:** 1 (core). **Relevance:** colleague 5/5, my optimization angle 3/5.

## Problem and motivation
Rare genetic disease diagnosis with phenotype-only input. Full genome sequencing is not always available, and the candidate-gene space is huge. The goal is to identify the most likely causal gene and return a patient-specific subgraph for clinical follow-up.

## Data and graph
- Knowledge graph from prior work (105,220 nodes, 1,095,469 edges; node types include phenotypes, diseases, genes).
- Datasets: MyGene2 (real, 146 patients) and a simulated set (42K patients: 36K train, 6.4K test, designed to exclude many training diseases/genes).

## Optimization lens
- **Decision:** which edges/genes to keep. A learned **edge score** is computed per edge (attention-based, from a GAT over an m-hop subgraph sampled around the patient's phenotypes), and a **gene scorer** ranks candidates.
- **Objective:** joint training of two losses:
  - *subgraph loss*: contrasts positive edges (phenotype → causal gene) against negative edges sampled from the m-hop neighborhood; it encourages concise, enriched subgraphs;
  - *gene loss*: ranks the true causal gene among all candidates.
  The two are coupled in a teacher–student setup, where the edge scorer penalizes the gene scorer.
- **Constraints:** none explicit. Subgraph size is controlled through the scoring and the sampling radius m, not by a constrained optimizer.
- **Solver:** gradient-based (deep learning). Subgraph selection is *soft*, learned through scores, not a combinatorial solve.

## Method (short)
1. Sample an m-hop subgraph around the patient's phenotype nodes.
2. GAT layers produce node embeddings and attention coefficients.
3. Patient representation = attention-pooled phenotype embeddings.
4. Edge scores and gene scores are computed; the final patient subgraph keeps high-scoring edges.
5. Also usable as a **pre-processing** filter (restrict candidate genes) or **post-processing** re-ranker (boost genes in the subgraph by δ after min–max normalization of an external method's scores).

## Evaluation
- Metrics: Hits@1/5/10, MRR. Baselines: Shepherd, PhenoApt (and Amelie, as an add-on).
- Simulated Patients (Table III): RareNet Hits@1 **27.2 ± 1.0** vs Shepherd 13.0 and PhenoApt 8.8; Hits@10 **60.6 ± 2.2** vs 35.7 and 23.3.
- Simulated Patients, mixed setting (Table V area): Hits@1 **57.4 ± 1.0** (text extraction; verify table label).
- MyGene2 (Table IV): used as add-on to Shepherd, Amelie and PhenoApt (+RN); gains reported per method.

## Key claims (verify before citing)
- "First knowledge-graph method that jointly extracts a patient-specific subgraph, generates candidate genes and prioritizes causal genes from phenotypes only."
- The authors explicitly question current evaluation protocols and dataset limitations (abstract, last sentence).

## Limitations
- Evaluated on two datasets; simulated patients may not reflect real clinical distributions.
- Interpretability is claimed through subgraphs; no clinical validation reported in the text I read.
- Sampling radius and loss weighting are design choices with limited sensitivity analysis in the sections I skimmed (full-text pass pending).

## Relevance
- **To OncoGeneGraph:** very close. Same clinical question family (rare/hereditary disease, phenotype/variant KG, subgraph explanation). Shows the KG-sparsification-for-diagnosis pattern in the same domain.
- **To my optimization angle:** the subgraph selection is *learned via scores*, not solved as a combinatorial problem; the two-loss coupling is an implicit multi-objective trade-off with fixed weighting. Good target for "make it explicit" (Pareto or budgeted selection).

## Ideas to borrow / open questions
- Replace the implicit size control with an explicit **budget/size constraint** and compare to a fixed-size top-k baseline.
- Use the subgraph as a **candidate filter** for cascade testing (see `../phase-1/2026-10-15-themes.md`, theme B).
- How sensitive are Hits@k to the radius m and to the subgraph-loss weight?

## Snowballing
- Backward: rare-disease KG GNN references; Shepherd and PhenoApt papers.
- Forward: citing papers from 2025–2026 (see `../phase-1/2026-10-15-snowballing.md`).
