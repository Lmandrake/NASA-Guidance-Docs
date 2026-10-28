# Dutle et al. — Verification of Autonomous Systems (NASA Langley presentation, NTRS 20250003529)

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Dutle et al., NASA Langley Research Center (NTRS record 20250003529) |
| **Kind** | Research presentation (slides), 49 PDF pages |
| **Status** | NTRS record: STI type PRESENTATION, Distribution PUBLIC, no publication date listed. Presented at "NASA SWS Assurance of Autonomy Technical Challenge Closeout" (NTRS record). The abstract field is empty |
| **Where to get it** | `https://ntrs.nasa.gov/citations/20250003529` (confirmed anonymously off-network, 2026-10-26) |
| **Binds whom** | No one. A research briefing, not a requirement |

**What it is good for, relative to NASA's documents.** Shows what formal-methods verification of autonomy-related algorithms looked like in one NASA research group: what can be proved about path planning, runtime assurance and small neural networks, and where those methods stop scaling. It is evidence of research practice, not of what any NASA document requires (our reading).

**Key content for AI / machine-learning assurance.**
- Scope: "Formal Verification: The use of mathematically rigorous tools and techniques to verify the correctness of a digital design" (slide 1, p.2). Three strands: verification of autonomous path planning, of runtime assurance (RTA) frameworks, and numerical verification of AI/ML components (p.2).
- Runtime assurance: "a runtime monitor is used in a simplex architecture, where an untrusted component is allowed to operate, but is monitored" (p.12). The framework is verified with a NASA-developed tool, Plaidypvs, an embedding of differential dynamic logic in the PVS prover (pp.18-19).
- Neural networks: the stated problem is "Unpredictable behavior" and "Round-off error in embedded systems" (p.41). Activation functions were formalized in PVS (p.43), and small examples show a single input can change class as numeric precision is lowered (p.45).
- Path planning: formal analysis of one rerouting algorithm "discovered some issues" in the algorithm as described (p.5).
- Future-work slides note limits, for example "Investigate novel abstraction techniques to scale up analysis" (p.49).

**Nearest NASA counterpart.** None directly. For software assurance and verification requirements see `../documents/NPR_7150.2D.md` and `../documents/NASA-STD-8739.8B.md`; compare as research methods versus requirements (our reading).
