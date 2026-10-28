# Russino et al. (2024) — A Utility-Driven Approach to Onboard Scheduling and Execution for an Autonomous Europa Lander Mission

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Authors from the Jet Propulsion Laboratory, California Institute of Technology (first author Russino, with other authors); published in the Journal of Aerospace Information Systems (JAIS). Copyright notice: "Copyright © 2024. California Institute of Technology. Government sponsorship acknowledged." (p.1) |
| **Kind** | Research paper (journal article, author-posted version) |
| **Status** | Header reads "Appears in Journal of Aerospace Information Systems (JAIS), 2024", DOI 10.2514/1.I011323 (p.1). The file is named for 2023; the text itself says 2024. The posted copy may differ from the publisher's final version. |
| **Where to get it** | Public: `https://ai.jpl.nasa.gov/public/documents/papers/MEXEC-EL-Journal-Article-2023.pdf`, confirmed anonymously off-network, 2026-10-26. Publisher copyright applies; this page quotes sparingly. |
| **Binds whom** | No one. |

**What it is good for, relative to NASA's documents.** A worked design for system-level onboard autonomy on a concept mission with long communication blackouts, showing how an autonomy planner and executive are structured, tested in simulation, and reasoned about as a decision-theoretic system. It is a source of design and validation vocabulary for autonomy, not a statement of what NASA requires (our reading).

**Key content for AI / machine-learning assurance.**
- The abstract frames the approach as a utility-driven Hierarchical Task Network and says analysis shows it is "more consistently productive compared to traditional static approaches" (Abstract, p.1). The mission concept faces long blackouts: "over 42 hours out of every 84 hours" (Introduction, p.2).
- Design for flight: the planner and executive were designed for flight software with a cooperative design, and the executive does real-time constraint checking before a task runs (Section on MEXEC, p.15 to p.16). The planner validates uploaded task networks for memory fit and task assumptions before storing them (p.20).
- Verification and validation is named as a hard problem: "validation and verification of an autonomous systems is a tremendous challenge" (Discussion, p.31). It adds that past flights of significant autonomy relied on formal methods, informal methods and testing (p.31).
- Why flights are rare: system-level autonomy controls most mission activities and so "requires a very high degree of confidence" in the planner/scheduler (Related Work, p.32).
- Evidence offered here is empirical, from software simulation of realistic surface scenarios against static baselines (Abstract, p.1; Conclusion).

**Nearest NASA counterpart.** `../documents/NASA-STD-8739.8B.md`: its software assurance activities are what a team would apply to this kind of flight software, while the paper supplies the autonomy design context (our reading). No NASA page here covers onboard planning and execution specifically.
