# KAT-GNN: A Knowledge-Augmented Temporal Graph Neural Network for Risk Prediction in Electronic Health Records

**Citation:** Lin, K.-W.; Kuo, Y.-C.; Wang, H.-Y.; Tseng, Y.-J. arXiv:2511.01249v1 (3 Nov 2025). Venue: not stated in the preprint (IEEE template). BibTeX key: `lin2025katgnn`.
**Source:** `Artigos/KAT-GNN: A Knowledge-Augmented Temporal Graph Neural Network for Risk Prediction in Electronic Health Records.pdf`
**Tier:** 2 (method + domain). **Relevance:** colleague 4/5, my optimization angle 2/5.

## Problem and motivation
Clinical risk prediction from EHRs is hard because data are heterogeneous and irregular over time. The paper injects clinical knowledge into patient graphs and models longitudinal dynamics.

## Data and graph
- Chang Gung Research Database (coronary artery disease prediction).
- MIMIC-III and MIMIC-IV (in-hospital mortality).
- Patient graphs built per modality, augmented with **ontology-driven edges from SNOMED CT** and **co-occurrence priors** from EHRs.

## Optimization lens
- No explicit optimization component. The "knowledge" enters as graph structure (edges); learning is standard supervised training of a time-aware transformer over graph-encoded patients.
- The optimization-relevant point is that **ontology-derived edges are a design choice**, not a constraint solved by an optimizer.

## Method (short)
1. Modality-specific patient graphs from EHR codes.
2. Augment with SNOMED CT ontology edges and co-occurrence priors.
3. Time-aware transformer over graph-encoded patient representations.

## Evaluation (as reported in the abstract)
- CAD prediction, AUROC **0.9269 ± 0.0029**.
- MIMIC-III mortality AUROC **0.9230 ± 0.0070**; MIMIC-IV **0.8849 ± 0.0089**.
- Baselines: GRASP and RETAIN. Ablations: knowledge augmentation and temporal modeling both contribute.

## Limitations
- Structure of the ontology edges is fixed by hand; no sensitivity analysis of which ontology relations matter (to verify in full text).
- EHR data, not germline/genetic; the ontology used (SNOMED CT) is clinical.

## Relevance
- **To OncoGeneGraph:** moderate-high as an example of **how an ontology enters a GNN** (the same question as the colleague's "ontology/schema" step). Her schema (Patient, FamilyMember, Variant, Gene, ACMG classes) could be augmented by ontology edges in the same way.
- **To my optimization angle:** low. No optimization method; useful as a baseline and as a source for which ontology edges to keep.

## Ideas to borrow / open questions
- Treat the choice of ontology edges as a **selection problem** (which SNOMED/ACMG relations to add under a size budget). That connects to theme C in `../phase-1/2026-10-15-themes.md`.

## Snowballing
- Backward: GRASP, RETAIN, SNOMED CT, time-aware transformers.
- Forward: ontology-augmented GNNs for clinical prediction (see `../phase-1/2026-10-15-snowballing.md`).
