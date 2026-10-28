# Department of Defense Cyber Developmental Test and Evaluation Guidebook, Version 3.0

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Office of the Director, Developmental Test, Evaluation, and Assessments (DTEA); Office of the Under Secretary of Defense for Research and Engineering |
| **Kind** | Guidebook (DoD T&E community guidance) |
| **Status** | Version 3.0, June 2025. |
| **Where to get it** | Public: cto.mil/dtea; Distribution Statement A, approved for public release, distribution unlimited. Public copy, confirmed anonymously off-network on 2026-10-26: `https://www.cto.mil/wp-content/uploads/2025/08/Cyber-DTE-Guidebook-V3-June2025_Final_87e72e.pdf` |
| **Binds whom** | DoD government cyber DT&E test teams — guidance under the companion DoW Manual 5000.103 policy, not a binding requirement in its own right. |

**What it is good for, relative to NASA's documents.** General cyber-DT&E guidance; its treatment of AI
is secondary (as an attack surface and a test tool), not the guidebook's main subject, unlike the
companion AI-Enabled Systems guidebook (our reading).

**Key content for AI / machine-learning assurance.**
- Lists "AI (e.g., Machine Learning, Deep Learning, Natural Language Processing, Robotics) and Big Data
  Applications" as a named cyber-attack-surface category, with guidance to "consider training and model
  parameter data poisoning," "susceptibility of altered analytics and other attacks," and "model
  extraction attacks" (threat-surface table, verbatim bullets).
- Discusses AI from two directions for test teams: "AI as the SUT [system under test]" and "AI as a
  test tool," warning that if AI is used to generate or evaluate test results, those results must be
  "explainable and repeatable," or risk being "irrelevant" due to possible AI "hallucinations or
  mistakes" (§ on AI, paraphrase/partial quote).
- Names a planned, not-yet-released "Digital Appendix M: Cyber DT&E for artificial intelligence-enabled
  systems," described as a "prototype under development" at time of writing (table entry, paraphrase).
- Points to the external MITRE ATLAS™ matrix (atlas.mitre.org) for AI-specific adversarial-ML attack
  techniques (paraphrase).

**Nearest NASA counterpart.** No NASA document addresses cyber DT&E specifically; compares to
`../documents/NID_1383.155.md`-adjacent cybersecurity material and general NASA IT-security NIDs (our
reading, comparison only).
