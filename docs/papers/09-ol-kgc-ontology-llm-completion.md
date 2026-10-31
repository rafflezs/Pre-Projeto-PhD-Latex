# Ontology-Enhanced Knowledge Graph Completion using Large Language Models (OL-KGC)

**Citation:** Guo, W.; Wang, X.; Chen, J.; Li, Z.; Tian, Z. arXiv:2507.20643 (2025). Tianjin University; University of Manchester. BibTeX key: `guo2025olkgc`.
**Source:** `Artigos/Ontology-Enhanced Knowledge Graph Completion using Large Language Models.pdf` (19 pages)
**Tier:** 2 (ontology constraints). **Relevance:** colleague 3/5, my optimization angle 2/5.

## Problem and motivation
LLM-based KG completion is a black box. It implicitly stores knowledge and can disseminate errors, so the output is hard to confirm. The paper combines neural structural information with **ontological knowledge** to make the reasoning more checkable.

## Data and graph
Standard KG completion benchmarks (names and numbers not extracted yet).

## Optimization lens
- No explicit optimization. The ontology enters as **knowledge retrieved by an automated extraction algorithm** and used to guide the LLM prompt or representation.
- Relevant point: ontology is used as a **constraint on the prediction space** (what is admissible), which is the same role the 01 draft gives it (feasible region).

## Method (short)
1. Neural-perceptual mechanism embeds structural information into text space.
2. Automated algorithm extracts ontological knowledge from the KG.
3. LLM reasons over the combined input.

## Evidence I have
Abstract only. Numbers pending the full-text pass.

## Limitations
- LLM-dependent; cost and reproducibility not discussed in what I read.
- Ontological knowledge is retrieved, not formally enforced (no hard constraints shown).

## Relevance
- **To OncoGeneGraph:** moderate. Her project already plans a GraphRAG layer; ontology-grounded retrieval and "confirmative" reasoning fit that layer.
- **To my optimization angle:** low-moderate. Useful as a contrast: ontology as soft guidance (here) vs. ontology as hard feasibility (what an optimization formulation can enforce).

## Ideas to borrow / open questions
- Compare soft ontology guidance (LLM prompt) with a hard **feasibility constraint** in a subgraph selection model.

## Snowballing
- Backward: LLM-based KGC (KG-BERT, etc.), ontology-aware reasoning.
- Forward: LLM + ontology reasoning in biomedical KGs (see `../phase-1/2026-10-15-snowballing.md`).
