# OWGAL: Open-World Graph Active Learning for Node Classification

**Citation:** Xu, H.; Xiang, L.; Ou, J.; Weng, Y.; Wang, X.; Zhou, C. ACM Transactions on Knowledge Discovery from Data 18(2), Article 43, Nov 2023. DOI 10.1145/3607144. Received 20 Nov 2022; accepted 19 Jun 2023. BibTeX key: `xu2023owgal`.
**Source:** `Artigos/3607144.pdf` (20 pages)
**Tier:** 2 (active learning with emerging classes). **Relevance:** colleague 2/5, optimization 3/5, chosen theme (cascade + DFL) 2/5.

## Problem and motivation
Graph AL methods assume a fixed set of classes. On evolving graphs, new classes appear, and AL methods that prefer known classes miss them. The paper calls this **Open-World Graph Active Learning (OWGAL)**: label nodes that are informative and also detect novel-class nodes.

## Data and graph
The setup section lists Amazon-Computer, Amazon-Photo, Coauthor-CS, Coauthor-Physics, Arxiv, Reddit and Products (seven names). The abstract and conclusion say "four large-scale datasets", and the setup sentence says "six datasets". **Check which datasets the main tables actually use.**

## Optimization lens
- **Formulation (their Eq. 1):** given graph G, known classes, an initial training set and a labeling budget B, select V_l with |V_l| = B that minimizes the expected loss on the remaining nodes. Standard cardinality-budget AL.
- **Method:**
  - prototype learning: each known class is a prototype vector, and known classes are pushed apart, so nodes far from all prototypes get high uncertainty (novel-class candidates);
  - unparameterized **label propagation** to score nodes far from labeled nodes in the topology;
  - **weighted sampling** over node importance and class importance, to suppress unimportant classes.
- **Solver:** heuristic scores plus weighted sampling. No optimality guarantee.

## Evaluation
- Macro-F1 improvement of **5.97% to 16.57%** over state-of-the-art baselines (abstract).
- Observation from their Table 2: **random sampling beats most graph-AL baselines** in this open-world setting, because the baselines prefer known classes while random sampling follows the data distribution and so hits novel classes more often. This is a useful warning about AL baselines.

## Limitations
- Inconsistent dataset count in the text (see above).
- Cardinality budget, uniform cost.
- The setting assumes rounds of AL at graph-evolution stages; how often rounds happen is not optimized.

## Relevance
- **To OncoGeneGraph:** low-moderate. A real-world registry grows over time (new families, new variants, VUS reclassifications), which is an open-world setting. New variant classes or phenotypes may appear.
- **To the chosen theme:** low-moderate. Two points matter: (1) a reminder to include **random and simple baselines**, since sophisticated AL can lose to them; (2) open-world shifts (new families, new genes) threaten any policy trained on past cases, which connects to the phase-2 point about validating on new families vs. known families.

## Ideas to borrow / open questions
- Weighted sampling over "class importance" maps to giving more weight to rare but clinically important variants (e.g., TP53 p.R337H as the priority subgroup).

## Snowballing
- Backward: open-world / open-set learning (OpenWGL, Proser, OW-DETR), prototype networks, label propagation (Zhu & Ghahramani 2002), AGE, GPN.
- Forward: graph AL under distribution shift and class imbalance (Contra2, 2025, in the phase-1 snowballing log).
