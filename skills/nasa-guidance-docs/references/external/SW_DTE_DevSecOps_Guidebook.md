# Software Developmental Test and Evaluation in DevSecOps Guidebook

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Office of the Director, Developmental Test Evaluation and Assessments (DTE&A); Office of the Under Secretary of Defense for Research and Engineering |
| **Kind** | Guidebook (DoD T&E community guidance) |
| **Status** | January 2025 edition. |
| **Where to get it** | Public: cto.mil/dtea; Distribution Statement A, approved for public release, distribution unlimited. Public copy, confirmed anonymously off-network on 2026-10-26: `https://www.cto.mil/wp-content/uploads/2025/08/SW-DT_E-in-DevSecOps-Guidebook-Jan-2025-1.pdf` |
| **Binds whom** | DoD software DT&E teams working within Agile/DevSecOps pipelines — guidance, not a binding directive. |

**What it is good for, relative to NASA's documents.** A DevSecOps-pipeline-specific companion to the
AI-Enabled Systems guidebook, useful for how ML components are expected to be tested inside a
continuous-integration software pipeline specifically — a context NASA's own software-assurance
documents do not address in these terms (our reading).

**Key content for AI / machine-learning assurance.**
- Has a dedicated section, "4.8 Testing Systems that Incorporate Artificial Intelligence and Machine
  Learning" (table of contents and body heading, verbatim).
- States that an ML-based system's lifecycle "necessarily differs from a traditional system in that an
  ML-based system requires training data and cannot be properly tested until it has been trained," with
  training-data volume potentially "orders of magnitude larger" than the trained system itself (§4.8,
  paraphrase/partial quote).
- Lists DevSecOps-specific ML test issues (§4.8, verbatim bullets, partial): "Verifying and validating
  training data," "Testing the software environment used to conduct training."
- A text search of the public PDF finds roughly 4 occurrences each of "Machine Learning" and "Artificial
  Intelligence," concentrated in §4.8, plus 2 occurrences of "neural" — AI/ML is one dedicated section
  within a broader DevSecOps T&E guidebook, not its central topic.

**Nearest NASA counterpart.** No NASA document addresses software T&E inside a DevSecOps/Agile pipeline
specifically; compares to `../documents/NPR_7150.2D.md` (software engineering requirements) and
`../documents/NASA-STD-8739.8B.md` (software assurance) (our reading, comparison only).
