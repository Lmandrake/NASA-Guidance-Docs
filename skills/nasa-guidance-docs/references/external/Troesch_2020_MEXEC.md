# Troesch et al. (2020) — MEXEC: An Onboard Integrated Planning and Execution Approach for Spacecraft Commanding

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Authors from the Jet Propulsion Laboratory, California Institute of Technology (first author Troesch, with other authors) |
| **Kind** | Research paper (workshop paper) |
| **Status** | 2020 paper; copyright line reads "Copyright c 2020, California Institute of Technology. Government sponsorship acknowledged." (p.1). The venue (IntEx 2020 workshop) is taken from the host URL, as the first page of the text does not name it. |
| **Where to get it** | Public: `https://ai.jpl.nasa.gov/public/papers/IntEx-2020-MEXEC.pdf`, confirmed anonymously off-network, 2026-10-26 |
| **Binds whom** | No one. |

**What it is good for, relative to NASA's documents.** A compact description of a goal-based onboard planner and executive built as flight software, with two experiments on a CubeSat and its testbed. Useful as an example of incremental infusion and of the assurance work that autonomy flight software involved (our reading).

**Key content for AI / machine-learning assurance.**
- The paper says autonomy increases require that one "methodically prove out autonomous capabilities" and let users build confidence (Introduction, p.1), and that MEXEC was developed in a systematic way "to be flight-ready" with incremental flight and testbed experiments (p.1).
- Interaction with fault protection: shutting down the planner from the ground or by fault protection raised timing risks that "required some verification and validation work, as well as careful design" (p.5).
- Resource limits: MEXEC was held to 2 MB of memory, which limited task networks to 100 tasks or fewer (p.5). Before first flight, the team did testing, input validation, static analysis and optimizations, and points to a separate source for the assurance techniques used (p.5).
- Results: the flight experiment reproduced standard sequence behavior; the testbed experiment showed a momentum constraint being monitored and a dump response dispatched without tripping fault protection (Results and Conclusion, pp.6 to 8). The paper's claim that this could have avoided safe mode is a hypothetical about a flight situation, not a flight result (p.8).

**Nearest NASA counterpart.** `../documents/NASA-STD-8739.8B.md` for assurance of flight software (our reading); this paper describes practice on a small mission and does not map to a specific requirement.
