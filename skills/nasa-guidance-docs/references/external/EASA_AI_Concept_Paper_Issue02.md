# EASA AI Concept Paper (Issue 02) — Concept Paper: First Usable Guidance for Level 1 & 2 Machine Learning Applications

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | European Union Aviation Safety Agency (EASA) |
| **Kind** | Concept paper (pre-regulatory guidance) |
| **Status** | Issue 02, dated 2024-03-06. Its own Foreword states it "does not constitute at this stage definitive or detailed guidance" and will feed EASA's AI Roadmap 2.0 Phase II ("AI/ML framework consolidation") once formal rulemaking begins (p.3). Concept/draft stage, not an adopted regulation. |
| **Where to get it** | Public, via EASA's AI Roadmap concept-paper series (easa.europa.eu); a public PDF was confirmed anonymously off-network on 2026-10-26 at `https://www.easa.europa.eu/en/downloads/139504/en`, but that download id was not individually confirmed to be Issue 02 |
| **Binds whom** | No one yet. A pre-regulatory concept paper meant to give applicants "early visibility" of EASA's expectations ahead of formal Means of Compliance (MOC) (p.4). |

**What it is good for, relative to NASA's documents.** This is the closest document among those mapped here to
an aviation safety regulator writing ML-specific lifecycle assurance objectives, the way
NASA-STD-8739.8B does for conventional software (our reading). It is explicitly scoped to "Level 1"
and "Level 2" AI, where a human retains decision authority or full oversight, and explicitly excludes
"Level 3" autonomous AI — so it does not reach the most autonomy-heavy end of the spectrum that NPR
8705.4B or ASTM F3269 address (our reading).

**Key content for AI / machine-learning assurance.**
- Three AI levels, defined by where decision authority sits: Level 1 "assistance to human" (human
  decides and acts), Level 2 "human-AI teaming" (system can act automatically, human retains full
  oversight/override), Level 3 "advanced automation" (not covered by this Issue) (p.4 footnote 4, p.10).
- Four "AI trustworthiness building blocks": trustworthiness analysis, AI assurance (renamed from
  "learning assurance"), human factors for AI (renamed from "AI explainability"), and AI safety risk
  mitigation (p.6).
- Criticality ceiling for this Issue: EASA states it will "initially accept only applications where
  AI/ML constituents do not include IDAL A or B / SWAL 1 or 2 / AL 1, 2 or 3 items" for supervised
  learning, and a lower ceiling still (IDAL D / SWAL 4 / AL 5 only) for unsupervised learning (p.10,
  paraphrase).
- 🔴 Verified quote: the document contains, verbatim, "The objectives contained in Sections C.3.1.1 to
  C.3.1.13 of this document fully apply to surrogate ML models," at the page marked as the
  start of page 84 (immediately before its page-85 marker). **Other citations give this
  claim as "p.86"; we could not resolve the discrepancy** — possibly a printed-page vs.
  PDF-page offset in this 258-page document. Flagging rather than silently reconciling.
- Names an in-progress industry standard, joint EUROCAE/SAE WG-114/G-34, as a track EASA is watching for
  future Means of Compliance (p.4).

**Nearest NASA counterpart.** No NASA document assigns AI-specific lifecycle objectives (data
management, learning management, model implementation, explainability) the way this concept paper
does; `../documents/NASA-STD-8739.8B.md` and `../documents/NASA-HDBK-2203.md` are the nearest NASA
counterparts for conventional software-assurance process structure (our reading, comparison only — not
a coverage claim).
