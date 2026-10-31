# Snowballing log

Protocol for building the literature base. Notes are in English.

## Seed set (round 0)
The 13 PDFs in `/home/rafflezs/Documentos/Doutorado/Artigos`. Notes in `papers/`.

## Tools
- **OpenAlex API** (`api.openalex.org`): `works/doi:...` for metadata; `filter=cites:W...` for citing works; `search=` with `filter=publication_year:2022-2026` for keyword discovery. Keyword search is loose, so read titles and check each candidate's abstract before counting it.
- **Semantic Scholar / Google Scholar / arXiv / ACM DL / IEEE Xplore / Springer**: to confirm venues and to access full texts through the USP/CAPES portal.

## Search strings (round 1)
- "active learning graph neural networks labeling budget"
- "subgraph selection graph neural networks learned policy"
- "knowledge graph sparsification graph neural network"
- "rare disease knowledge graph graph neural network"
- "Pareto multi-objective pruning graph neural network"
- "cascade testing germline variant relatives"

Planned but not yet run: "ontology constrained graph neural network knowledge graph" (first run gave off-topic results; rerun with different wording), "multi-objective hyperparameter optimization graph neural network", "integer programming active learning labels", "submodular active learning budget".

## Round 1 log (date: 2026-10-26)

### Backward / forward on Tier-1 seeds
- **RareNet (note 01)**: OpenAlex lists 0 citing works (too recent for index). Backward list still to pull (its references are not in OpenAlex yet).
- **Policy-Learn (note 02)**: 2 citing works in OpenAlex (2025: motif-driven molecular representation; graph self-supervised learning). Low relevance; logged as "later".
- **One-shot subgraph (note 03)**: 3 citing works (2025: multi-granularity KG reasoning, TKDE; SGKGE, TNNLS). Both KG-related. **Include for read**: "Learning Multi-Granularity and Adaptive Representation for Knowledge Graph Reasoning" (TKDE 2025, doi 10.1109/tkde.2025.3579774).
- **MOO survey (note 05)**: 14 citing works. Most are application papers. **Include for read**: "Pareto Set Learning for Multi-Objective Reinforcement Learning" (AAAI 2025, doi 10.1609/aaai.v39i18.34068) as a Pareto-set method reference; "Interactive Pareto Navigation for Deep Multi-task Learning" (2026, doi 10.1007/978-3-032-37667-1_37).

### Keyword discovery (round 1)
| Query | Candidates | Decision |
|---|---|---|
| active learning GNN labeling budget | Partition-Based Active Learning for GNNs (2022, arXiv 2201.09391); Structural-Clustering AL for GNNs (2024, doi 10.1007/978-3-031-58547-0_3); ScatterSample diversified label sampling (2022, arXiv 2206.04255); Batch AL with GNNs via multi-agent deep RL (AAAI 2022, doi 10.1609/aaai.v36i8.20897); Dissimilar Nodes Improve Graph AL (2022, arXiv 2212.01968); Contra2 one-step AL for imbalanced graphs (2025, doi 10.1016/j.artint.2025.104439) | **Include for read** (partition-based, batch AL, Contra2). Relevant to theme A (budgeted labeling). |
| subgraph selection GNN learned policy | Mostly off-topic (materials, transport, federated, GNN for subgraph transformation) | Discard. Refine query with "subgraph" + "explanation" or "sampling". |
| KG sparsification GNN | Towards Sparsification of GNNs (ICCD 2022, doi 10.1109/iccd56317.2022.00048); Graph Sparsification for Enhanced Conformal Prediction in GNNs (2024, arXiv 2410.21618); Inverse link prediction with GCNs for knowledge-preserving sparsification in chemistry (2025, doi 10.1186/s40537-025-01220-8) | **Include for read**: "Inverse link prediction ... knowledge-preserving sparsification" (knowledge-preserving sparsification is directly on theme C). Others later. |
| rare disease KG GNN | Application of KGs in rare disease research (2026, doi 10.3389/fpubh.2026.1757612); KGs and explainable AI for drug repurposing on rare diseases (2024, doi 10.1101/2024.10.17.618804; 2026 journal version doi 10.1177/29498732261443101); AI-driven drug repurposing with KGs for rare diseases (2025, doi 10.14293/idr.25.019ss); KGs meet GNNs: comprehensive survey (2026, doi 10.1145/3814608) | **Include for read**: "Application of knowledge graphs in rare disease research" (review, domain map); "Knowledge Graphs Meet GNNs: comprehensive survey" (2026). Drug-repurposing papers later. |
| Pareto pruning GNN | PrONe-RS: graph-isomorphic pruning with Pareto optimization (2026, doi 10.1109/jstars.2026.3686462); Hierarchical and dependency-aware multi-objective evolutionary pruning of DNNs (2026); Pareto optimization for multi-objective virtual screening (2024, doi 10.1039/d3dd00227f) | **Include for read**: PrONe-RS (Pareto + pruning, same structure as theme C; check whether the method is graph-based). Others later. |
| cascade testing germline | Cascade testing for hereditary cancer: multigene panels (JNCI 2023, doi 10.1093/jnci/djad203); cost-utility of targeted BRCA testing with cascade testing (2025, doi 10.1016/j.gim.2025.101463); Factors affecting implementation of cascade testing for BRCA (2025, doi 10.1002/jgc4.70055) | **Include for read** (clinical context for her workflow, and cost-utility as an optimization objective). **No optimization-formulated cascade-testing paper found in these results**: supports theme B as an open gap, but this is one search round, not an exhaustive check. |

## Stop rule and status
Stop rule: stop when two consecutive rounds bring no new Tier-1 candidate. **Round 1 found new candidates (partition-based AL, knowledge-preserving sparsification, PrONe-RS)**, so the rule is not yet satisfied. Next round: backward references of the new candidates, and the queries listed as "planned".

## Items to fetch (you download; I do not download PDFs)
1. Partition-Based Active Learning for GNNs (arXiv 2201.09391)
2. Batch Active Learning with GNNs via Multi-Agent Deep RL (AAAI 2022)
3. Contra2: one-step AL for imbalanced graphs (Artif. Intell. 2025)
4. Inverse link prediction for knowledge-preserving sparsification (2025)
5. Application of knowledge graphs in rare disease research (Front. Public Health 2026)
6. Knowledge Graphs Meet Graph Neural Networks: A Comprehensive Survey (2026)
7. PrONe-RS (JSTARS 2026)
8. Pareto Set Learning for Multi-Objective RL (AAAI 2025)
9. Cascade testing for hereditary cancer: multigene panels (JNCI 2023)

## Colleague's references
Ask Ana Carolina for her reference list or `.bib` (her proposal `99-OncoGeneGraph_BR_AMPLIA.docx` has in-text citations such as Schlichtkrull et al. 2018 and Gogoshin & Rodin 2023, and the Casali da Rocha et al. Chompret study). Add them to round 2 as seeds.

## Inclusion rule (applied so far)
Peer-reviewed or arXiv with a clear method and evaluation; graph-based or optimization-focused; domain relevance (biomedical KG, rare disease, cascade testing) counted as a plus. Excluded: surveys in unrelated domains unless they carry the optimization framing; industrial reports without method details.

## Round log (summary table)
| Round | Date | Seeds | New Tier-1 | Status |
|---|---|---|---|---|
| 0 | 2026-10-26 | 13 PDFs | — | done |
| 1 | 2026-10-26 | 13 + OpenAlex citing/keyword | 9 for read (items above) | open (rule not met) |
