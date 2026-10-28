# NASA/SP-2016-6105-SUPPL — Expanded Guidance for NASA Systems Engineering, Volume 2

| | |
|---|---|
| **Owner office** | NASA Headquarters (no single named responsible office found in our text extraction) |
| **Kind and force** | NASA/SP (Special Publication) — guidance/reference supplement, not a requirements document; see ../force.md. Companion/supplement volume to the main NASA Systems Engineering Handbook, NASA/SP-2016-6105 |
| **Revision and status** | Published March 2016. No later edition found; whether a newer edition exists is unknown |
| **Where to get it** | NTRS (ntrs.nasa.gov), search by number — no document-specific URL found. Public copy, confirmed anonymously off-network on 2026-10-26: `https://ntrs.nasa.gov/api/citations/20170007239/downloads/20170007239.pdf` |

**Scope, plainly.** A 264-page supplement covering crosscutting systems-engineering topics (contracts, concurrent engineering, tool selection, environmental/nuclear/planetary-protection compliance, multi-level programs, fault management, technical margins, human systems integration) and two "special topics," §8.1 Statistical Engineering and §8.2 Model-Based Systems Engineering (MBSE), plus template/outline appendices. It contains no AI/ML-specific content; its closest vocabulary to "model-based" assurance is §8.2's own treatment of "model," aimed at engineering/architecture models rather than learned AI/ML models (our reading).

**AI and machine-learning touchpoints.** No "artificial intelligence" or "machine learning" found. "Autonom*" appears in §7.7 Fault Management: "Mitigation and recovery actions can be autonomous, automated, or human-controlled" (p.67); "decision functions can be autonomous, human interactive, or a combination of automation with human intervention" (p.68); and low-level recovery strategies may "autonomously adjust system parameters to mitigate the effects of faults" (p.69). These describe spacecraft fault-management autonomy generally, not AI/ML specifically (our reading).

**Connections and traps.**
- §8.1 Statistical Engineering (pp.62-64) is a NASA-sanctioned discipline for quantifying confidence in decisions under uncertainty, including probabilistic risk assessment — the closest existing NASA vocabulary to a confidence/calibration argument for a learned component (our reading).
- §8.2 Model-Based Systems Engineering (pp.64-70) quotes INCOSE 2007 on the shift from document-centric to model-centric SE and discusses MBSE implementation challenges (IT infrastructure, ontology, configuration management) — again, engineering models, not learned models (our reading).
- Only §7.1 and the openings of §8.1-8.2 were read in prose for this page; the remainder of Chapter 7 and the template appendices (C-T) were surveyed by header only.
