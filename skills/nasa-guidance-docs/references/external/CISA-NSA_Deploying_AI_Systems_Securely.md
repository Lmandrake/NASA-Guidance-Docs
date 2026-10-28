# CISA-NSA Deploying AI Securely — Deploying AI Systems Securely: Best Practices for Deploying Secure and Resilient AI Systems

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | U.S. National Security Agency (NSA) Artificial Intelligence Security Center, with CISA, FBI, and international partners (Australian Signals Directorate/ACSC, Canadian Centre for Cyber Security, New Zealand NCSC, UK NCSC) [p.1] |
| **Kind** | guidance / joint cybersecurity information (best practices), voluntary |
| **Status** | Ver. 1.0, April 2024; document id U/OO/143395-24, PP-24-1538; marked TLP:CLEAR (shareable without restriction) [p.1] |
| **Where to get it** | Public (U.S. government joint guidance); originally media.defense.gov / cisa.gov, which block some direct fetches — mirrored via web.archive.org. Public copy, confirmed anonymously off-network on 2026-10-26: `https://www.ic3.gov/CSA/2024/240415.pdf` |
| **Binds whom** | No one (voluntary) — "best practices," addressed to organizations that deploy and operate AI systems developed by another entity [p.1-2] |

**What it is good for, relative to NASA's documents.** This is operational, deployment-and-maintenance
security guidance — explicitly scoped to organizations deploying and operating AI systems "designed
and developed by another entity," and explicitly *not* applicable to design/development itself (which
its companion document, the UK NCSC's "Guidelines for secure AI system development," covers) (our
reading of [p.1-2]). Its value here is a concrete, government-coordinated checklist for securing the
deployment environment, protecting model weights, and operating/monitoring a fielded AI system — a
late-lifecycle layer that is thinner in NASA's own documents (our reading).

**Key content for AI-related assurance.**
- Structured in three phases: "Secure the deployment environment," "Continuously protect the AI
  system," and "Secure AI operation and maintenance" [p.3, p.5, p.7].
- Calls for requiring the AI system's primary developer to supply a threat model, which the
  deployment team then uses to plan mitigations (paraphrase of [p.3-4]).
- Names model weights as "a particularly critical component to protect," recommending hardware
  protection, isolated storage (e.g., a hardware security module or restricted enclave), and
  two-person control/integrity for privileged access [p.4, p.7, p.9] (paraphrase).
- Recommends human-in-the-loop as a failsafe for automated rollbacks and for other AI-assisted
  automation, and recommends continuous monitoring of model behavior for drift or anomalous inputs
  [p.6, p.8] (paraphrase).
- AI touchpoint check (artificial intelligence|machine learning|automat|algorithm|software, etc.): the
  document is entirely about securing "AI systems" and "ML-based" systems; "artificial intelligence,"
  "AI system," and "machine learning" recur throughout, including the explicit scope statement that
  "AI systems" here "refers to machine learning (ML) based artificial intelligence (AI) systems" [p.2].

**Nearest NASA counterpart.** Closest to `../documents/NPR_8705.4B.md` (risk classification for NASA
payloads/missions, operations-phase concerns) and `../documents/NASA-STD-8739.8B.md` (software
assurance), for its operate-and-maintain-phase controls (monitoring, access control, patching); none
of NASA's documents reviewed here separate deployment/operations security guidance for an
externally-developed AI system this explicitly (our reading).
