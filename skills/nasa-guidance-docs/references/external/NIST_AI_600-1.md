# NIST AI 600-1 — Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | National Institute of Standards and Technology (NIST), U.S. Department of Commerce |
| **Kind** | guidance ("cross-sectoral profile of and companion resource for" the AI RMF [p.5]) |
| **Status** | NIST AI 600-1, issued July 2024 [p.2]; final; no later edition found |
| **Where to get it** | free public download, DOI https://doi.org/10.6028/NIST.AI.600-1 [p.1]; publication number NIST AI 600-1 |
| **Binds whom** | no one — it inherits the AI RMF's voluntary status; it is a profile ("cross-sectoral profiles can be used to govern, map, measure, and manage" risk, [p.5]) rather than a separate mandate |

**What it is good for, relative to NASA's documents.** It is the NIST AI RMF narrowed to generative
AI (GenAI) specifically, naming twelve risk categories unique to or exacerbated by GenAI and tying
each to suggested actions keyed to the RMF's GOVERN/MAP/MEASURE/MANAGE subcategories (our reading).
NASA's own documents (NASA-HDBK-2203, NPR 7150.2D) do not break out generative-AI-specific risks at
this granularity, so this profile is useful vocabulary for naming a candidate risk precisely before
checking what NASA text, if any, bears on it (our reading). It is not mission-assurance guidance and
carries no NASA safety-class or verification obligations.

**Key content for artificial intelligence / machine-learning assurance.**
- Twelve GenAI risk categories, each with its own numbered subsection (Sec. 2.1-2.12, pp.7-8 for the
  list, detailed through the chapter): CBRN Information or Capabilities; Confabulation; Dangerous,
  Violent, or Hateful Content; Data Privacy; Environmental Impacts; Harmful Bias or Homogenization;
  Human-AI Configuration; Information Integrity; Information Security; Intellectual Property;
  Obscene/Degrading/Abusive Content; Value Chain and Component Integration (Sec. 2, pp.7-8).
- "Confabulation" is NIST's term for an AI system confidently presenting erroneous or false content
  (Sec. 2.2, p.8) — the same phenomenon colloquially called hallucination.
- Actions are tagged with an Action ID mapping back to the parent AI RMF function/subcategory, e.g.
  "GV1.1-001" for the first suggested action under Govern 1.1 (p.17).
- Artificial intelligence / machine learning touchpoint: the whole document is a generative-AI risk
  profile; "artificial intelligence," "generative AI," "algorithm," and "automated" occur throughout —
  no isolated bullet needed.

**Nearest NASA counterpart.** Compares to `NASA-HDBK-2203` and `NPR_7150.2D` — those govern NASA
software assurance broadly, including AI-enabled software, but do not isolate generative-AI-specific
failure modes (confabulation, prompt-driven information extraction, value-chain integration risk) the
way this profile does (our reading).
