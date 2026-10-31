# Strategies to Improve Implementation of Cascade Testing in Hereditary Cancer Syndromes: A Systematic Review

**Citation:** Chiang, J.; Chua, Z.; Chan, J. Y.; Sule, A. A.; Loke, W. H.; Lum, E.; Ong, M. E. H.; Graves, N.; Ngeow, J. npj Genomic Medicine 9:26 (2024). DOI 10.1038/s41525-024-00412-0. Received 9 Nov 2023; accepted 13 Mar 2024. BibTeX key: `chiang2024cascade`.
**Source:** `Artigos/41525_2024_Article_412.pdf` (10 pages)
**Tier:** 1 (problem domain for the chosen theme). **Relevance:** colleague 5/5, optimization 2/5, chosen theme (cascade + DFL) 5/5.

Already cited in `docs/phase-2/2026-10-30-consolidacao.md` (as the `nature.com` link).

## Problem and motivation
About 10% of cancers come from hereditary cancer syndromes, which are underdiagnosed. Cascade testing tests at-risk relatives of a proband with a pathogenic or likely pathogenic variant. Uptake is poor, usually below 30%, and studies in Asian countries report rates as low as 13%. The review asks which intervention strategies improve cascade testing uptake, how well they are described, and which implementation outcomes are evaluated.

## Data (review protocol)
- Databases: PubMed, Embase, Web of Science, Cochrane Library, CINAHL, PsycINFO, Google Scholar. 2,606 records identified, 1,821 screened, 63 assessed in full text, **27 studies included** (PRISMA 2020 chart).
- Designs: 17 prospective, 5 cross-sectional, 5 retrospective. Publication dates 2013–2023, nine countries; 17 studies (63.0%) from the USA.
- Genes: 8 studies (29.6%) BRCA1/2 only; 3 (11.1%) Lynch genes (MLH1, MSH2, MSH6, PMS2, EPCAM); 11 (40.7%) broader panels; 5 (18.5%) did not specify. No study is described as Li-Fraumeni/TP53-specific in the parts read (TP53 appears only in the reference list).
- Frameworks: interventions classified with the **EPOC taxonomy**; intervention description quality with **TIDieR**; implementation outcomes with **Proctor's framework**.

## Key findings (verified in the extracted text)
- Mean uptake **41%** in intervention groups vs **33%** in control groups (studies that reported uptake).
- Uptake by EPOC category: **delivery arrangements 68%**, financial arrangements 37%, implementation strategies 24%. 20 of the 27 studies (74.1%) fall under delivery arrangements.
- Mean TIDieR score **7.3 / 12**. Least reported: modifications (18.5%), plans to assess fidelity (7.4%), actual fidelity assessment (7.4%).
- On average, **2.9 of 8** implementation outcomes were examined. **Cost, fidelity and sustainability were each reported by only 3.7% of studies** (one study out of 27).
- Direct contact of relatives by healthcare staff is acceptable to relatives, but it is **limited by privacy laws** that forbid disclosing genetic information to third parties without the proband's consent.

## Optimization lens
The review has no optimization model. It matters for the thesis because it defines the decision problem and its constraints:
- **Objective candidates:** uptake (relatives tested), carriers detected, cost per carrier detected.
- **Constraints:** consent and privacy (who may be contacted, and by whom), service capacity, communication channel (patient-mediated vs direct contact).
- **Evidence gap:** cost is almost never reported (3.7%). Any cost-aware optimization will need cost parameters from elsewhere (health-economics studies, the Genesis/Fleury operation) or a sensitivity analysis.
- The actions the review studies are **interventions on the communication and delivery process**, not choices of which relative to test. That is a different decision layer from the one the phase-2 theme proposes, and the thesis must say which layer it optimizes.

## Limitations (from the paper)
- EPOC categories overlap; the authors chose the best-fitting category per intervention.
- Most studies are from the USA, so findings may not generalize to Asian (or, by extension, Brazilian) settings, where testing and family disclosure rates differ.
- Heterogeneous outcomes and reporting quality.

## Relevance
- **To OncoGeneGraph:** high. Her P2 product (structuring cascade testing at Genesis/Fleury) is exactly the process this review studies. The low uptake numbers support the value of structuring and measuring the flow.
- **To the chosen theme:** very high as **problem motivation and constraint source**. It supports the phase-2 claim that cascade testing depends on communication, access and service organization, not only on genetic risk. It also warns that a "who to test" optimization may be second-order if uptake is limited by contact and consent.

## Ideas to borrow / open questions
- Model the decision with uptake as a probability that depends on the delivery arrangement (e.g., direct contact vs patient-mediated). Then "who to test" and "how to reach them" become one optimization problem.
- Cost parameters: look for the cost-utility study of targeted BRCA testing with cascade testing (Genet. Med. 2025, in the phase-1 snowballing log) and for Brazilian cost data.
- Privacy and consent rules are **hard constraints** in the formulation, consistent with LGPD in the colleague's project.

## Snowballing
- Backward: the 27 included studies (Table 1 of the paper), especially the delivery-arrangement interventions; the meta-analysis on direct contact of relatives that the discussion cites.
- Forward: cascade-testing implementation studies 2024–2026; any modeling or simulation of cascade testing strategies (none found yet, see the phase-1 snowballing log).
