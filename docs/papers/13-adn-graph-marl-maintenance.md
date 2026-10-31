# Adaptive Risk-Aware Maintenance Strategy for Active Distribution Networks via Graph-Based Multi-Agent Reinforcement Learning

**Citation:** Huang, Y.; Zheng, X.; Liu, X.; Su, Z.; Lin, F. (Guangzhou Power Supply Bureau, Guangdong Grid). ICCSMT 2025 (short, 5 pages). BibTeX key: `huang2025adn`.
**Source:** `Artigos/Adaptive Risk-Aware Maintenance Strategy for Active Distribution Networks via Graph-Based Multi-Agent Reinforcement Learning.pdf`
**Tier:** 3 (context; sequential decision-making with graphs). **Relevance:** colleague 1/5, my optimization angle 4/5.

## Problem and motivation
Maintenance planning for active distribution networks, where distributed energy resources make the grid stochastic and bidirectional. Time-based and condition-based maintenance are too static.

## Data and graph
The grid as a graph (spatial dependencies and topological state).

## Optimization lens
- **Method:** GR-MAPPO = Graph neural network (state representation) + multi-agent reinforcement learning (decentralized coordination) + Proximal Policy Optimization (training), with a **risk-aware** component.
- **Decision:** maintenance actions per agent/area over time.
- **Objective:** cost and risk trade-off through the reward design (details not reviewed).
- **Solver:** policy-gradient RL; not an exact optimizer.

## Evidence
Abstract only; the short paper's experiments were not reviewed.

## Limitations
- Short conference paper; the risk-aware reward and the evaluation protocol are likely thin (to check).
- Engineering domain; the connection to clinical KGs is conceptual.

## Relevance
- **To OncoGeneGraph:** low.
- **To my optimization angle:** moderate. Shows **graph-based sequential decision-making under risk**, a different optimization paradigm (RL) from the subgraph selection and MOO papers. Useful for contrast with exact methods.

## Ideas to borrow / open questions
- Risk-aware objectives (e.g., CVaR) as an alternative to expected-cost in the label or test budget problem.

## Snowballing
- Backward: MAPPO (Yu et al. 2022), graph-based MARL in power systems.
- Forward: risk-aware graph RL in engineering systems (see `../phase-1/2026-10-15-snowballing.md`).
