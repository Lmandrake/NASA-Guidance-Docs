# OWASP Top 10 LLM 2025 — OWASP Top 10 for LLM Applications 2025

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | OWASP (Open Worldwide Application Security Project), GenAI Security Project — a community-driven, non-profit project [p.1, p.5] |
| **Kind** | guidance / vulnerability taxonomy, industry community project, voluntary |
| **Status** | "Version 2025," released 2024-11-18; supersedes the 2023 v1.0 (2023-08-01) and v1.1 (2023-10-16) [p.2] |
| **Where to get it** | Free public document, no login/paywall: genai.owasp.org (OWASP GenAI Security Project). Licensed under Creative Commons CC BY-SA 4.0 — redistribution and adaptation permitted with attribution and share-alike [p.2]. Public copy, confirmed anonymously off-network on 2026-10-26: `https://genai.owasp.org/download/43299/?tmstv=1731900559` |
| **Binds whom** | No one (voluntary) — a community-authored industry reference, not a regulation |

**What it is good for, relative to NASA's documents.** This is an industry-community vulnerability
taxonomy for large language model (LLM) applications, built by security practitioners through
"brainstorming sessions, voting, and real-world feedback" (paraphrase of [p.5]) — not a government or
standards-body document. Its value here is a detailed, widely used vocabulary of ten concrete LLM
attack/failure classes (e.g., prompt injection, excessive agency) with example attack scenarios and
mitigations, at a level of specificity NASA's own guidance does not reach for this exact technology
(our reading).

**Key content for AI-related assurance.**
- Ten numbered risk categories for 2025, each with description, common vulnerability examples,
  mitigations, and attack scenarios: LLM01 Prompt Injection [p.7]; LLM02 Sensitive Information
  Disclosure [p.11]; LLM03 Supply Chain [p.15]; LLM04 Data and Model Poisoning [p.20]; LLM05 Improper
  Output Handling [p.23]; LLM06 Excessive Agency [p.26]; LLM07 System Prompt Leakage [p.30]; LLM08
  Vector and Embedding Weaknesses [p.33]; LLM09 Misinformation [p.36]; LLM10 Unbounded Consumption
  [p.39].
- LLM06 Excessive Agency names three root causes — "excessive functionality," "excessive
  permissions," "excessive autonomy" — and recommends human-in-the-loop approval for high-impact
  actions (paraphrase of [p.26-28]); this maps closely to autonomous-agent oversight concerns.
- LLM09 Misinformation treats "hallucination" as a named cause of misinformation and cites a real
  incident (Air Canada chatbot) and overreliance as a related, distinct failure mode [p.36-37].
- AI touchpoint check (artificial intelligence|machine learning|automat|algorithm|software, etc.): the
  whole document is about LLM/AI application security; essentially every page references "LLM,"
  "model," or "AI" directly.

**Nearest NASA counterpart.** Closest to `../documents/NASA-STD-8739.8B.md` (software assurance and
software safety) and `../documents/NASA-STD-7009B.md` (models and simulations standard) for the
model-behavior risks (LLM04, LLM09), though neither NASA document names LLM-specific attack classes
such as prompt injection or system prompt leakage (our reading).
