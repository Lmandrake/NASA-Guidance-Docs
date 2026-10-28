# Wronkiewicz et al. (2024) — Onboard Science Instrument Autonomy for the Detection of Microscopy Biosignatures on the Ocean Worlds Life Surveyor

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Authors from the Jet Propulsion Laboratory, Portland State University and the University of California, Berkeley (first author Wronkiewicz, with other authors) |
| **Kind** | Research paper (arXiv preprint, astro-ph.IM) |
| **Status** | arXiv:2304.13189v2, 19 Jan 2024; page header reads "Draft version January 22, 2024" (p.1). Preprint; review status not stated in the text. |
| **Where to get it** | Public: `https://arxiv.org/abs/2304.13189v2`, confirmed anonymously off-network, 2026-10-26 |
| **Binds whom** | No one. |

**What it is good for, relative to NASA's documents.** A concrete case of machine-learning classifiers running onboard an instrument suite to decide what data to return, with written requirements for transparency, uncertainty and operator override. It shows how a project might phrase assurance-relevant requirements for a learned component before any NASA document asks for them in so many words (our reading).

**Key content for AI / machine-learning assurance.**
- Problem: an instrument suite could generate 10,000x more raw data than can be transmitted (Abstract, p.1). Onboard Science Instrument Autonomy (OSIA) evaluates, summarizes and prioritizes data to maximize science return (Abstract, p.1).
- Six proposed requirements to "engender trust with mission stakeholders" (Section 1.6, p.5): overlapping extractions using unrelated algorithms; supporting raw data with summaries; prioritization that considers data already returned; reconfiguration information; honoring manual downlink requests at highest priority; and uncertainty estimates with extracted parameters.
- Interpretability drove model choice: computational and interpretability requirements led to classical ML (gradient boosted trees, random forests, support vector classifiers) rather than deep networks (Section 3.3.4, p.16).
- Operator control: priority bins and manual override of prioritization decisions during ground commanding (Section 3.3, p.18).
- Failure-cost reasoning: transmitting false positives has no intrinsic cost unless they "crowd out true positives" from a downlink opportunity (Section 3.4, p.19). Data-validation checks flag observations that violate expected data characteristics (Section 5.4).
- Evaluation used simulated and laboratory data and a field test at Mono Lake (Abstract, p.1). The paper integrates with the F Prime flight software framework (Section 5.5, p.30).

**Nearest NASA counterpart.** `../documents/NASA-STD-7009B.md` (models and simulations credibility) is the closest in spirit for how one would argue credibility of a learned model, and `../documents/NASA-HDBK-2203.md` is the guidance route for software engineering practice (our reading). Neither addresses onboard learned classifiers in these terms.
