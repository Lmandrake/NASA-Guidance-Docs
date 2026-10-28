# NIST SP 800-218A — Secure Software Development Practices for Generative AI and Dual-Use Foundation Models: An SSDF Community Profile

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | National Institute of Standards and Technology (NIST), with CISA (Cybersecurity and Infrastructure Security Agency) contribution (one co-author, Martin Stanley, is CISA) [p.1-2] |
| **Kind** | guidance — an SSDF (Secure Software Development Framework) Community Profile augmenting NIST SP 800-218 [p.5] |
| **Status** | July 2024, approved by the NIST Editorial Review Board 2024-07-25 [p.2, p.8] |
| **Where to get it** | Free public document, no login/paywall: https://doi.org/10.6028/NIST.SP.800-218A, also csrc.nist.gov/pubs/sp/800/218/a/final [p.1, p.4] |
| **Binds whom** | No one (voluntary) — it is "not subject to copyright in the United States" and "may be used by nongovernmental organizations on a voluntary basis"; applies to AI model producers, AI system producers, and AI system acquirers who elect to use it [p.3, p.6] |

**What it is good for, relative to NASA's documents.** This document is an augmentation/profile of
the base SSDF (NIST SP 800-218), not a standalone standard — it supplements SSDF practices and
tasks with AI-specific recommendations, considerations, and notes, and "should not be used without
SP 800-218" (our reading of [p.5]). Its value here is as a detailed, publicly vetted vocabulary for
secure AI model development practices (data provenance, model-weight protection, training-data
integrity) that NASA's own documents do not spell out at this granularity (our reading).

**Key content for AI-related assurance.**
- Scope is explicitly AI model *development* (data sourcing, design, training, fine-tuning,
  evaluation); "practices for the deployment and operation of AI systems with AI models are out of
  scope" (paraphrase of [p.10]).
- Table 1 (SSDF Community Profile for AI Model Development) adds AI-specific recommendations under
  existing SSDF practice groups PO (Prepare the Organization), PS (Protect Software), PW (Produce
  Well-Secured Software), and RV (Respond to Vulnerabilities) [p.14-27].
- Notable AI-specific additions: confirming training/testing/fine-tuning/aligning data integrity
  before use (task PW.3, "Not part of SSDF 1.1") [p.22-23]; protecting model weights and
  configuration parameters from unauthorized access (PS.1.3) [p.20]; and tracking provenance of a
  model and its components (PS.3.2) [p.21].
- AI touchpoint check (artificial intelligence|machine learning|automat|algorithm|software, etc.):
  the document is saturated with "artificial intelligence," "generative AI," "AI model," and
  "machine learning" throughout — it is written specifically for AI/ML software development, not an
  incidental hit.
- A limitation the document states about itself: it "only address[es] cybersecurity risk
  management," not the fuller set of AI risks (data privacy, intellectual property, bias) (paraphrase
  of [p.13]).

**Nearest NASA counterpart.** Closest in subject matter to `../documents/NASA-STD-8739.8B.md`
(NASA's software assurance and software safety standard) and `../documents/NPR_7150.2D.md` (NASA's
software engineering requirements) — both address secure, reliable software development process
requirements, but neither names AI-specific development-time risks (training data integrity, model
weight protection) the way this Profile's PW.3/PS.1.3/PS.3.2 additions do (our reading).
