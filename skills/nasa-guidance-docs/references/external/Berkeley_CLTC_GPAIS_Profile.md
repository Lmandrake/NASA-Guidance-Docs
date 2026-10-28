# Berkeley CLTC GPAIS Profile — AI Risk-Management Standards Profile for General-Purpose AI Systems (GPAIS) and Foundation Models

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | UC Berkeley Center for Long-Term Cybersecurity (CLTC), AI Security Initiative; authors Anthony M. Barrett, Jessica Newman, Brandie Nonnecke, Dan Hendrycks, Evan R. Murphy, and Krystal Jackson [p.3] |
| **Kind** | Guidance / risk-management profile (academic / think-tank; voluntary) |
| **Status** | Version 1.0, November 2023 [p.1] |
| **Where to get it** | Public, CC BY 4.0 license, at cltc.berkeley.edu/publication/ai-risk-management-standards-profile [p.1–p.2]. Note: excerpts from NIST's AI Risk Management Framework (AI RMF) Playbook reproduced in Section 3 are under NIST's own fair-use license terms, not CC BY [p.1]. The open license means fuller quoting of the Berkeley-authored text is fine, but locators are kept below regardless. Public copy, confirmed anonymously off-network on 2026-10-26: `https://cltc.berkeley.edu/wp-content/uploads/2023/11/Berkeley-GPAIS-Foundation-Model-Risk-Management-Standards-Profile-v1.0.pdf` |
| **Binds whom** | No one (voluntary) — "We intend this Profile document primarily for use by developers of large-scale, state-of-the-art GPAIS" (paraphrase) [p.9]; it is a supplementary profile to the voluntary NIST AI RMF, not a standalone mandate. |

**What it is good for, relative to NASA's documents.** NASA's own documents have no profile
tailored specifically to general-purpose or foundation models (GPAIS) the way this 118-page document
tailors the NIST AI RMF to that case (our reading). It is unusually concrete for a voluntary framework: an
appendix retrospectively tests the Profile's own draft guidance against four real 2023 foundation
models (GPT-4, Claude 2, PaLM 2, Llama 2), rating how far public documentation for each model
fulfilled the Profile's high-priority subcategories [p.7–p.8 Contents; p.83]. That self-test is a rare example
of a framework checking itself against real systems rather than staying purely prescriptive (our reading).

**Key content for artificial intelligence / machine-learning assurance.**
- Organized around the NIST AI RMF's four "core functions": Govern (policies/roles), Map (context and
  risk identification), Measure (AI trustworthiness characteristics), Manage (prioritize/respond)
  (paraphrase) [p.9–p.10; p.5–p.7 Contents]
- Section 4 cross-maps its own guidance: §4.1 "Mapping to ISO/IEC 23894," §4.2 "Preliminary Mapping
  to ISO/IEC FDIS 42001," §4.3 "Mapping to White House AI Commitments" [p.7 Contents]
- Names technical practices for frontier/foundation models (Manage 1.2–1.3): incremental compute
  scale-up (roughly ≤3x per step) to catch emergent capabilities early, protecting model weights,
  disallowing open-ended live web access during training, excluding canary-tagged (BIG-bench) data
  [p.64–p.65]
- Appendix 4 retrospectively rated the Profile's draft guidance against GPT-4, Claude 2, PaLM 2, and
  Llama 2 using each model's public documentation, with a per-model subcategory rating table [p.83]
  and a GPT-4 rationale appendix starting at [p.86]
- AI/machine-learning touchpoint: the entire document is a risk-management profile for general-
  purpose AI systems and foundation models; found throughout, not in one isolated passage

**Nearest NASA counterpart.** `NASA-HDBK-2203` (the Software Engineering Handbook), whose topics
7.25 and 8.25 address artificial intelligence directly, and `NASA-STD-7009B` / its companion
`NASA-HDBK-7009B` (Standard for Models and Simulations), whose Revision B extends its
credibility-reporting approach to "a model built by machine learning" (paraphrase, per that document's
own page). The difference (our reading): NASA's documents set a credibility-reporting process keyed
to a specific decision and its criticality, while this Profile sets detailed, named technical practices
(compute-scaling increments, weight protection, canary-string exclusion) aimed specifically at the
developers of large-scale foundation models — a narrower and more model-development-centric
scope than NASA's decision-focused credibility framework.

