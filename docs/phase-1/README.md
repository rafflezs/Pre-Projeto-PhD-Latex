# Literature studies: PhD pre-project (Phase 1)

> Current consolidated paper index: [`../papers/README.md`](../papers/README.md) (18 notes, updated 2026-10-30). This file is the 2026-10-15 snapshot.

Working notes on the 13 seed papers for the pre-project. Notes are in English; the pre-project itself is in PT-BR (`main.tex`, `tex/`).

Research direction (as stated): optimization applied to AI, supporting the colleague's OncoGeneGraph-BR work (knowledge graph + R-GCN for hereditary cancer, Li-Fraumeni). The optimization focus is not yet chosen; see `themes.md`.

## How to use this folder

| File | What it is |
|---|---|
| `papers/NN-slug.md` | One note per paper: citation, problem, graph/data, **optimization lens**, evidence, limitations, relevance, snowballing hooks. |
| `themes.md` | Candidate optimization themes (A–E) for Phase 2, with evidence level and risk. Cross-cutting observations from the 13 papers. |
| `snowballing.md` | Search protocol, OpenAlex queries, round-1 log, items to fetch, stop rule. |
| `refs.bib` | BibTeX drafts for the 13 seeds (not merged into `bib/ref.bib`). |

Relevance scores in each note: **colleague** = relevance to OncoGeneGraph-BR (1–5); **optimization** = relevance to the optimization angle (1–5).

## Index

| # | Note | Tier | Colleague | Optim. | Reading status |
|---|---|---|---|---|---|
| 01 | [RareNet: KG sparsification for rare disease diagnosis](../papers/01-rarenet-kg-sparsification-rare-disease.md) | 1 | 5 | 3 | full sections (method, loss, results) |
| 02 | [Efficient Subgraph GNNs via selection policies (Policy-Learn)](../papers/02-policy-learn-efficient-subgraph-gnns.md) | 1 | 2 | 5 | full sections (method, tables) |
| 03 | [One-shot-subgraph link prediction (PPR)](../papers/03-one-shot-subgraph-link-prediction.md) | 1 | 4 | 4 | method, ablation, BO; numbers pending |
| 04 | [KGTrimmer: KG pruning for recommendation](../papers/04-kgtrimmer-kg-pruning-recommendation.md) | 1 | 3 | 4 | method, datasets; ratio semantics to check |
| 05 | [Multi-objective DL: taxonomy and survey](../papers/05-multiobjective-deep-learning-survey.md) | 1 | 2 | 5 | taxonomy sections |
| 06 | [STAL: active learning + self-training for GNNs](../papers/06-stal-active-learning-self-training-gnn.md) | 1–2 | 4 | 4 | method, tables |
| 07 | [DynTKG: dynamic subgraph pruning, temporal KGs](../papers/07-dyntkg-dynamic-subgraph-pruning-tkg.md) | 2 | 2 | 3 | abstract; numbers pending |
| 08 | [KAT-GNN: ontology edges for EHR risk](../papers/08-kat-gnn-ehr-risk.md) | 2 | 4 | 2 | abstract + ablation summary |
| 09 | [OL-KGC: ontology + LLM completion](../papers/09-ol-kgc-ontology-llm-completion.md) | 2 | 3 | 2 | abstract; numbers pending |
| 10 | [GNNs for DTI in rare disease](../papers/10-gnn-drug-target-rare-disease.md) | 2 | 4 | 2 | method, limitations |
| 11 | [A Survey on GNNs (IEEE Access 2026)](../papers/11-survey-graph-neural-networks.md) | bg | 2 | 2 | abstract |
| 12 | [LinkedIn cross-domain GNN](../papers/12-linkedin-cross-domain-gnn.md) | 3 | 1 | 3 | abstract |
| 13 | [Graph-based MARL for ADN maintenance](../papers/13-adn-graph-marl-maintenance.md) | 3 | 1 | 4 | abstract |

"Numbers pending" means the results section has not been checked yet; do not quote those numbers until it has.

## Main takeaways (reading level, to confirm in full texts)

1. The optimization in most graph papers is **gradient-based and scalarized** (RareNet's two-loss coupling, STAL's grid search, LinkedIn's multi-task weights). Exact or budgeted discrete selection is rare in this set. This is the opening an OR-background thesis can use.
2. **Labeling is a fixed budget, not a cost** (STAL). A cost-aware, budgeted selection with guarantees is a gap in this set.
3. **Ontology is soft** in the clinical papers (KAT-GNN, OL-KGC). Hard ontological constraints as part of a subgraph optimization are not shown in any of the 13 papers.
4. The closest work to the colleague's domain is **RareNet** (01) and the rare-disease papers (10). The closest methodological work is **Policy-Learn** (02) and **One-shot** (03).
5. Cascade testing as an optimization problem did not appear in the first search round (see `themes.md`, theme B).

## Corrections to `docs/01-roteiro-pre-projeto.md` (not applied; for your decision)

Checked against the PDFs in the folder:

| Draft line | Draft says | What the PDF shows |
|---|---|---|
| 1 | Starts with chat text ("Sim — dá para transformar…") | Residue from a chat answer; remove before using the draft. |
| 47, 90, 154 (and other lines) | Links to a long presigned S3 URL (`X-Amz-Expires=600`) | Expires after 10 minutes; not a stable reference. |
| 54, 150 | `mlgworkshop` link for "A Survey on Graph Neural Networks" | The PDF is a 2026 IEEE Access survey (Zhang et al., DOI 10.1109/ACCESS.2026.3665657). Cite that. |
| 64, 144 | Dynamic subgraph pruning cited via an IEEE Xplore link | The PDF is J. King Saud Univ. Comput. Inf. Sci. 37:96 (2025), DOI 10.1007/s44443-025-00105-3. |
| 68 | Multi-objective DL survey via `link.springer` with DOI 10.1007/s44443-025-00105-3 | That DOI is the DynTKG paper's. The survey is arXiv:2412.01566 (Peitz & Hotegni). |
| 145 | KG pruning cited via ScienceDirect (S2666827025000830) | The PDF is ACM TOIS 44(1), DOI 10.1145/3769107 (KGTrimmer). |
| 146 | "Graph Policy Network for Transferable Active Learning on Graphs" with arXiv 2310.20082v2 | 2310.20082 is **Efficient Subgraph GNNs by Learning Effective Selection Policies** (ICLR 2024). The Graph Policy Network paper is not in the folder. |
| 147 | "Active Learning for Graphs with Noisy Structures" | Not in the folder; unverified. |
| 148 | STAL linked to DOI 10.1145/3769107 | Correct DOI: 10.1007/s10618-023-00959-z (Data Min. Knowl. Disc. 38, 2024). |
| 48 vs 36 | 48-month plan (lines 120–131) | The colleague's proposal (section 1) uses 36 months (3 years of doctorate). Decide the horizon. |

Round-1 OpenAlex queries also returned leads that the draft does not cite (see `snowballing.md`).

## Status and next steps

- Notes 01–06 read at section level; 07–13 partly or abstract-level. Full-text pass for 07–13 is the next task, and the "numbers pending" items above.
- Snowballing round 1 done; stop rule not yet met (see `snowballing.md`). Round 2: backward references of the new candidates; the planned queries; the colleague's reference list.
- Fetch the 9 items listed in `snowballing.md` (PDFs not downloaded by me).
- Choose the Phase 2 optimization theme (`themes.md`).
- Decide whether `docs/01-roteiro-pre-projeto.md` is rewritten and the corrections above applied, and whether `refs.bib` is merged into `bib/ref.bib`.

Nothing has been committed. `git status` should show only `docs/studies/` as new.
