# Large Scalable Cross-Domain Graph Neural Networks for Personalized Notification at LinkedIn

**Citation:** He, S.; Choi, J.; Li, T.; Ding, Z.; Du, P.; et al. (LinkedIn). arXiv:2506.12700v1 (15 Jun 2025). BibTeX key: `he2025linkedin`.
**Source:** `Artigos/Large Scalable Cross-Domain Graph Neural Networks for Personalized Notification at LinkedIn.pdf` (9 pages)
**Tier:** 3 (context, industrial). **Relevance:** colleague 1/5, my optimization angle 3/5.

## Problem and motivation
Personalized notification ranking on LinkedIn, balancing several competing engagement objectives across user, content and activity signals.

## Data and graph
A single large cross-domain graph unifying user, content and activity signals; temporal modeling.

## Optimization lens
- **Multi-task learning** over several engagement objectives (click-through rate and professional engagement), i.e., a **multi-objective** training problem handled by a multi-task architecture. The weighting between tasks is the trade-off.
- Deployed in production, so the objective trade-off is set by business needs (decision-maker needs, in the MOO taxonomy of note 05).

## Evidence
Abstract: outperforms single-domain baselines on CTR prediction and professional engagement; architectural innovations (temporal modeling, multi-task learning) add further gains. Numbers pending the full-text pass.

## Limitations
- Industrial scale and proprietary data; hard to reproduce at academic scale.
- Multi-task weighting details not reviewed yet.

## Relevance
- **To OncoGeneGraph:** low.
- **To my optimization angle:** moderate. A deployed example of **multi-objective weighting in production** and the decision-maker framing; useful as motivation, not as a method to adopt.

## Ideas to borrow / open questions
- How are the task weights chosen in production (fixed, tuned, or learned)? This is an optimization question worth answering from the full text.

## Snowballing
- Backward: multi-task learning (MMoE, PLE-style mixture-of-experts), cross-domain recommendation with GNNs.
- Forward: deployed multi-objective GNNs in recommendation (see `../phase-1/2026-10-15-snowballing.md`).
