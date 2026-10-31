# Paper notes: consolidated index

One note per paper in `/home/rafflezs/Documentos/Doutorado/Artigos` (18 PDFs as of 2026-10-30). Notes are in English; the pre-project is in PT-BR.

This folder is the single place for paper breakdowns. Phase documents link here:
- `../phase-1/`: preparation (2026-10-15 roteiro draft, themes A–E, snowballing round 1).
- `../phase-2/`: theme refinement. The current theme is **decision-focused learning and optimization on family knowledge graphs to prioritize cascade genetic testing** (`../phase-2/2026-10-30-consolidacao.md`, `../phase-2/2026-10-30-cascade-testing-tema.md`).
- BibTeX drafts: `../../refs.bib` (repo root; not merged into `bib/ref.bib`).

## Note template

Each note has: citation and BibTeX key, problem, data/graph, **optimization lens** (decision variables, objective, constraints, solver), evaluation with numbers checked against the PDF text, limitations, relevance, ideas to borrow, snowballing hooks.

Scores (1–5):
- **Colleague:** relevance to OncoGeneGraph-BR (germline KG, R-GCN, GraphRAG, cascade testing).
- **Optim.:** relevance to the optimization-for-AI angle.
- **Theme:** relevance to the current phase-2 theme (cascade testing + decision-focused learning). Notes 01–13 were written before the theme was chosen, so their Theme score appears only in this index.

## Index

| # | Note | Topic | Tier | Colleague | Optim. | Theme | Reading depth |
|---|---|---|---|---|---|---|---|
| 01 | [RareNet](01-rarenet-kg-sparsification-rare-disease.md) | KG sparsification, rare disease diagnosis | 1 | 5 | 3 | 3 | method, loss, results |
| 02 | [Policy-Learn](02-policy-learn-efficient-subgraph-gnns.md) | learned subgraph selection (Gumbel) | 1 | 2 | 5 | 3 | method, tables |
| 03 | [One-shot subgraph](03-one-shot-subgraph-link-prediction.md) | PPR subgraph link prediction, BO tuning | 1 | 4 | 4 | 2 | method, ablation; numbers pending |
| 04 | [KGTrimmer](04-kgtrimmer-kg-pruning-recommendation.md) | KG pruning for recommendation | 1 | 3 | 4 | 1 | method, datasets |
| 05 | [Multi-objective DL survey](05-multiobjective-deep-learning-survey.md) | MOO taxonomy (scalarization, Pareto, MGDA) | 1 | 2 | 5 | 3 | taxonomy sections |
| 06 | [STAL](06-stal-active-learning-self-training-gnn.md) | active learning + self-training | 1–2 | 4 | 4 | 3 | method, tables |
| 07 | [DynTKG](07-dyntkg-dynamic-subgraph-pruning-tkg.md) | temporal KG pruning, distillation | 2 | 2 | 3 | 1 | abstract; numbers pending |
| 08 | [KAT-GNN](08-kat-gnn-ehr-risk.md) | ontology edges, EHR risk | 2 | 4 | 2 | 2 | abstract, ablation summary |
| 09 | [OL-KGC](09-ol-kgc-ontology-llm-completion.md) | ontology + LLM KG completion | 2 | 3 | 2 | 1 | abstract; numbers pending |
| 10 | [GNN DTI rare disease](10-gnn-drug-target-rare-disease.md) | sparse-data GNN, edge reweighting | 2 | 4 | 2 | 2 | method, limitations |
| 11 | [GNN survey (IEEE Access 2026)](11-survey-graph-neural-networks.md) | background | bg | 2 | 2 | 1 | abstract |
| 12 | [LinkedIn cross-domain GNN](12-linkedin-cross-domain-gnn.md) | deployed multi-task GNN | 3 | 1 | 3 | 1 | abstract |
| 13 | [ADN graph MARL](13-adn-graph-marl-maintenance.md) | risk-aware sequential decisions on a graph | 3 | 1 | 4 | 3 | abstract |
| 14 | [GALClean](14-galclean-active-learning-noisy-graphs.md) | active learning on noisy graphs, EM | 2 | 3 | 3 | 3 | method, ablation tables |
| 15 | [GPA](15-gpa-graph-policy-network-active-learning.md) | active learning as an MDP, RL policy | 1 | 3 | 5 | 4 | formulation, tables, budget curve |
| 16 | [AIM (cost-effective labelling)](16-aim-cost-effective-data-labelling-gnn.md) | NP-hard, submodular, greedy 1 − 1/e | 1 | 3 | 5 | 4 | formulation, contributions, Table 3 |
| 17 | [OWGAL](17-owgal-open-world-graph-active-learning.md) | open-world graph active learning | 2 | 2 | 3 | 2 | formulation, method, Table 2 notes |
| 18 | [Cascade testing review (npj Genom. Med. 2024)](18-cascade-testing-implementation-systematic-review.md) | interventions for cascade testing uptake | 1 | 5 | 2 | 5 | full results and limitations |

"Numbers pending": results not checked yet. Do not quote those numbers until they are.

## Reading paths

- **For the current theme (cascade testing + decision-focused learning):** 18 (problem, constraints, evidence gaps), then 15 (sequential acquisition as an MDP), 16 (budgeted selection with a guarantee), 14 (acquisition and structure estimation are interdependent), 06 and 17 (active-learning baselines and their pitfalls), 01 (rare-disease KG subgraphs), 13 (sequential decisions under risk), 05 (multi-objective vocabulary).
- **For the colleague's KG and GNN work:** 01, 10, 08, 03, 09, 18.
- **For subgraph and KG pruning (former theme C):** 02, 03, 04, 07, 01.

## Synthesis across the 18 papers

1. **Active learning on graphs spans three optimization styles in this set.** Greedy heuristics with uniform budgets (STAL 06, OWGAL 17, GALClean 14); learned sequential policies without bounds (GPA 15); and a combinatorial reformulation with an approximation guarantee (AIM 16). None of them has per-item costs (all use |S| = B), and none ties the selection to a downstream decision. Cost-aware, decision-aware acquisition with bounds is the open space, as far as this set shows.
2. **GPA's argument fits cascade testing.** Greedy per-step criteria are myopic; the real objective is the outcome after the whole sequence. In cascade testing, each result changes the next best action. GPA solves the sequential problem with RL; small pedigrees allow exact dynamic programming as an optimality reference.
3. **AIM shows the OR pattern the thesis can follow:** reformulate the acquisition problem, prove hardness, find submodularity, give a greedy algorithm with a guarantee. Open questions for cascade testing: is the objective (expected carriers detected) submodular in the set of tested relatives, and does adaptive submodularity cover the sequential version?
4. **Structural uncertainty matters.** GALClean (14) shows that choosing what to acquire and estimating the graph depend on each other. Pedigrees and kinship links are partly observed. This supports the phase-2 rule that inferred links must be kept apart from confirmed ones.
5. **The clinical evidence does not give cost parameters.** The cascade review (18) reports cost in only 3.7% of included studies (1 of 27). Uptake is highest with delivery-arrangement interventions (68%), compared with financial arrangements (37%) and implementation strategies (24%). Privacy law limits direct contact of relatives. A "who to test" model must therefore include uptake probability, consent constraints and cost assumptions with sensitivity analysis.
6. **Simple baselines can win.** In OWGAL's open-world setting, random sampling beats most graph-AL baselines (17). GPA and AIM compare only against heuristics, never against exact solutions. The evaluation plan should include random, risk-ranked and Mendelian-probability baselines, and exact solutions on small instances.
7. **Earlier findings still hold.** Subgraph selection is learned or heuristic (01–04). Trade-offs are mostly scalarized (05, 06, 12). Ontology is used as soft guidance, not as hard constraints (08, 09).

## Citation errors in the old draft (`docs/phase-1/2026-10-15-roteiro-pre-projeto.md`)

All checked against the PDFs. The NeurIPS link was also checked against its proceedings page title. Three active-learning citations are rotated:

| Draft line(s) | Draft attributes the link to | The link is actually | Fix |
|---|---|---|---|
| 17, 66, 111, 146 | Graph Policy Network / active learning on graphs (`arxiv.org/html/2310.20082v2`) | Policy-Learn, subgraph selection (note 02) | Cite GPA, NeurIPS 2020 (note 15) |
| 147 | "Active Learning for Graphs with Noisy Structures" (`proceedings.neurips.cc/.../73740ea85c4ec25f00f9acbd859f861d`) | GPA (note 15); the page title confirms it | Cite GALClean (note 14), MLG @ KDD 2023 |
| 54, 150 | "A Survey on Graph Neural Networks" (`mlgworkshop.org/2023/papers/MLG__KDD_2023_paper_9.pdf`) | GALClean (note 14) | Cite the IEEE Access 2026 survey, DOI 10.1109/ACCESS.2026.3665657 (note 11) |
| 68 | Multi-objective DL survey with DOI 10.1007/s44443-025-00105-3 | DynTKG (note 07) | arXiv:2412.01566 (note 05) |
| 148 | STAL with DOI 10.1145/3769107 | KGTrimmer (note 04) | DOI 10.1007/s10618-023-00959-z (note 06) |
| 64, 144 | DynTKG via an IEEE Xplore link | — | DOI 10.1007/s44443-025-00105-3 (note 07) |
| 145 | KG pruning via ScienceDirect (S2666827025000830) | — | ACM TOIS, DOI 10.1145/3769107 (note 04) |
| 1, 47, 90, 154 | chat residue and presigned S3 links that expire | — | remove |

## Open items

- Notes 07, 09, 11–13: full-text pass; fill the "numbers pending" items. Note 03: result numbers.
- Note 16 (AIM): find the published version and its authors; the PDF is an anonymous 2023 submission.
- Note 14 (GALClean): confirm the venue and whether a full-length version exists.
- Note 17 (OWGAL): resolve the dataset count (abstract says four, setup says six, seven names listed).
- Snowballing round 2 (the stop rule in `../phase-1/2026-10-15-snowballing.md` is not met): adaptive submodularity (Golovin & Krause 2011); submodular maximization under knapsack constraints; decision-focused / predict-then-optimize learning; cascade testing modeling and simulation; the 27 studies included in note 18.
