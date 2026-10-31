# GPA: Graph Policy Network for Transferable Active Learning on Graphs

**Citation:** Hu, S.; Xiong, Z.; Qu, M.; Yuan, X.; Côté, M.-A.; Liu, Z.; Tang, J. NeurIPS 2020 (Advances in Neural Information Processing Systems 33, pp. 10174–10185, as cited by Policy-Learn's reference list). Tsinghua; Mila; Microsoft Research. Code: `github.com/ShengdingHu/GraphPolicyNetworkActiveLearning`. BibTeX key: `hu2020gpa`.
**Source:** `Artigos/NeurIPS-2020-graph-policy-network-for-transferable-active-learning-on-graphs-Paper.pdf` (12 pages)
**Tier:** 1 (sequential acquisition as an MDP). **Relevance:** colleague 3/5, optimization 5/5, chosen theme (cascade + DFL) 4/5.

**Correction:** the old draft cited this title with arXiv 2310.20082, which is Policy-Learn (note 02). This PDF is the actual paper.

## Problem and motivation
Labeling nodes for GNN training is expensive in domains such as chemistry and health care. Existing graph AL methods have two flaws, as the authors state:
1. **They ignore long-term performance.** They greedily optimize a short-term surrogate criterion at each step, while the real objective is the final GNN performance after the whole sequence of queries.
2. **They ignore node interactions.** A node with many labeled neighbors adds little information, but per-node criteria do not see that.

## Data and graph
- Same-domain transfer: train the policy on Reddit {1, 2}, evaluate on Reddit {3, 4, 5}.
- Cross-domain transfer: train on Cora and Citeseer; evaluate on Pubmed, Reddit 1–5, Coauthor-Physics, Coauthor-CS (10 graphs in total in this setting).

## Optimization lens
- **Formulation:** active learning as a **Markov decision process**.
  - State: current graph status (node features plus labeling and prediction information).
  - Action: select one unlabeled node to annotate at step t.
  - Reward: performance gain of the classification GNN trained with the selected nodes.
  - Budget: a query budget B; the labeled set starts empty; at each step the GNN trains one more epoch; after B queries, training continues to convergence.
- **Objective:** maximize the long-term return (final performance), not the per-step surrogate.
- **Solver:** policy gradient (reinforcement learning). The policy is itself a GNN, so it can model node interactions.
- **Transfer:** the policy is trained on fully labeled source graphs and applied **without retraining** to unlabeled target graphs.

## Evaluation
- Baselines: Random, Uncertainty, Centrality, Coreset, AGE, ANRMAB.
- Tables 1 (same domain) and 2 (cross domain) report Micro-F1 and Macro-F1. GPA is reported best on most columns. The table cells are garbled in text extraction, so read the values from the PDF before quoting.
- Budget efficiency (their Figure 2, left): random selection needs a budget of 100 to reach Micro-F1 90.0; GPA reaches it with 30. AGE needs 100 for Micro-F1 91.7; GPA needs 50.

## Limitations
- Uniform cost per query; the budget is a count.
- Needs fully labeled source graphs to train the policy; transfer quality depends on how similar source and target graphs are.
- RL training is costly and has high variance; no optimality certificate. The comparison is against heuristics, not against an exact or bounded solution.
- Homogeneous graphs; no typed relations.

## Relevance
- **To OncoGeneGraph:** moderate. Curating variants or acquiring labels in a small cohort is a budgeted query problem. Transfer from public graphs to the Genesis cohort is a question the colleague's few-shot fallback also raises.
- **To the chosen theme:** high. GPA states the argument the phase-2 theme needs: **greedy per-step criteria are myopic; the true objective is the outcome after the whole sequence**. Cascade testing is the same shape: each test result changes which relative to test next. GPA's MDP (state, action, reward, budget) is a direct template for sequential cascade decisions, and its weakness (no bound, uniform cost) is where an OR formulation can add value.

## Ideas to borrow / open questions
- Use the MDP template for sequential cascade testing: state = pedigree with known and unknown carrier status; action = test a relative or clarify a link; reward = carriers found minus cost.
- Compare the RL policy with exact dynamic programming on small pedigrees, to measure the optimality gap.
- Per-action costs (some relatives are harder to reach) break the uniform-budget assumption; formulate as a constrained MDP.

## Snowballing
- Backward: AGE (Cai et al. 2017), ANRMAB (Gao et al. 2018), Coreset (Sener & Savarese 2018), policy-gradient AL (Fang et al. 2017, "learning how to active learn").
- Forward: RL-based graph AL after 2020; Batch AL with GNNs via multi-agent RL (AAAI 2022), listed in the phase-1 snowballing log.
