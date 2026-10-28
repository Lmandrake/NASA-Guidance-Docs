# NCSC-CISA — Guidelines for Secure AI System Development

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | UK National Cyber Security Centre (NCSC) and US Cybersecurity and Infrastructure Security Agency (CISA), jointly with ~21 international partner agencies (NSA, FBI, Australia's ACSC, Canada's CCCS, New Zealand's NCSC-NZ, Chile's Government CSIRT, Czech NUKIB, Estonia's RIA and NCSC-EE, France's ANSSI, Germany's BSI, Israel's INCD, Italy's ACN, Japan's NISC and Cabinet Office, Nigeria's NITDA, Norway's NCSC-NO, Poland's Ministry of Digital Affairs and NASK, South Korea's NIS, and Singapore's CSA) [p.3] |
| **Kind** | Guidance (secure-by-design lifecycle guidelines, not a standard) |
| **Status** | Published November 2023; the document states no revision number and carries no expiration date — marked for release on a TLP:CLEAR basis [p.3] |
| **Where to get it** | Public, published by NCSC (ncsc.gov.uk) and CISA (cisa.gov); text content is licensed for re-use under the UK Open Government Licence v3.0, "© Crown copyright 2023" [p.20]. Public copy, confirmed anonymously off-network on 2026-10-26: `https://www.ncsc.gov.uk/files/Guidelines-for-secure-AI-system-development.pdf` |
| **Binds whom** | No one (voluntary) — it "recommends guidelines for providers of any systems that use artificial intelligence" (paraphrase) [p.5] |

**What it is good for, relative to NASA's documents.** NASA has no agency-wide, security-focused
lifecycle checklist aimed specifically at AI/machine-learning systems the way this document is (our
reading). It was developed with input from major AI developers (Anthropic, OpenAI, Google, Google
DeepMind, Microsoft, Hugging Face, IBM and others are listed as contributing organizations) [p.3], so
its vocabulary — "secure by design," adversarial machine learning (AML), model/data provenance,
model cards — reflects fairly broad 2023 industry usage rather than any one vendor's framing (our
reading). It is useful as an outside structure for comparison, not as evidence of what NASA requires.

**Key content for artificial intelligence / machine-learning assurance.**
- Four lifecycle phases: secure design, secure development, secure deployment, secure operation and
  maintenance [p.4 Contents; p.8]
- Secure design: threat-model AI-specific risks, assess supply-chain security for trained/fine-tuned/
  API-based models, weigh model complexity against interpretability [p.9–p.11]
- Secure development: secure the AI supply chain, document models/data/prompts via model cards,
  data cards and SBOMs, manage AI-specific technical debt [p.12–p.13]
- Secure deployment: protect model weights/training data from extraction or tampering, build
  AI-specific incident response, release only after red-teaming/benchmarking [p.14–p.15]
- Secure operation and maintenance: monitor behavior and inputs for drift/adversarial activity,
  update via secure versioned release, share vulnerability information [p.16]
- Defines "AI" specifically as machine-learning applications and introduces "adversarial machine
  learning" (AML) — prompt injection, data poisoning — as its own threat class [p.6]
- AI/machine-learning touchpoint: the entire document is about securing AI/ML systems across their
  development lifecycle; found throughout, not in one isolated passage

**Nearest NASA counterpart.** `NASA-HDBK-2203` (the Software Engineering Handbook), whose topics
7.25 ("Artificial Intelligence And Software Engineering", since retitled "Super Intelligence And Software Engineering") and 8.25 address AI engineering and
assurance guidance directly, and `NASA-STD-8739.8B` (Software Assurance and Software Safety
Standard), which ties assurance tasks to the software lifecycle generally. The difference (our
reading): NASA's documents key assurance tasks to binding, numbered SWE requirements switched on
by a project's software class, while this guidance is voluntary, security-specific, and organized around
AI-particular controls (model/data provenance, red-teaming, supply-chain attestation) that NASA's
software lifecycle documents do not name in these terms.

