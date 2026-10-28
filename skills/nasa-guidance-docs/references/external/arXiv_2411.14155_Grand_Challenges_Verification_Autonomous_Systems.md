# Leahy et al. (2024) — Grand Challenges in the Verification of Autonomous Systems

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Authors from universities, industry and government laboratories, writing as the Roadmap Working Group of the IEEE Robotics and Automation Society Technical Committee for Verification of Autonomous Systems (first author Leahy, with other authors; Introduction, p.1 to p.2) |
| **Kind** | Research / position paper (arXiv preprint, cs.RO) |
| **Status** | arXiv:2411.14155v1, 21 Nov 2024; headed as a journal-class manuscript (p.1). Described as a "consensus viewpoint" of the working group (p.1 to p.2). Preprint. |
| **Where to get it** | Public: `https://arxiv.org/abs/2411.14155`, confirmed anonymously off-network, 2026-10-26 |
| **Binds whom** | No one. |

**What it is good for, relative to NASA's documents.** A compact list of why verification methods built for conventional software strain under autonomy, with research directions. It is a source of vocabulary (operating envelope, unknown unknowns, self-reverification) for discussing where the verification evidence NASA standards expect may fall short (our reading). It deliberately limits itself to verification and sets validation, evidence collection and certification aside (Introduction, p.2).

**Key content for AI / machine-learning assurance.**
- Why testing is not enough: the wide variety of deployment situations "preclude exhaustive testing as the primary means" of verifying correctness (Introduction, p.1).
- Unknown unknowns: aspects of the environment that are unknown cannot be modeled, so recognizing unanticipated scenarios is "a key challenge" (Section III, p.2).
- Requirements: legal, ethical and social expectations must be turned from non-functional into functional requirements so verification can handle them (Section III b and IV.A, p.3).
- Operating envelopes (Section IV.C, p.4): runtime monitors and out-of-distribution detection are not designed to tell whether a model no longer reflects its environment. It cites the automotive Operational Design Domain concept and proposes systems that reason over their own verification, including "Dynamic Assurance Cases" and self-reverification.
- Opaque AI: verifying behavior of "quite opaque AI technologies" inside autonomous systems "remains an unsolved problem" (Section IV.D, p.5). Verification must extend to the models autonomy software relies on, not just the code (p.4).
- The paper says AI verification is "somewhat orthogonal" to its topic and cites IEEE 1012 as a verification and validation standard (Introduction, p.2).

**Nearest NASA counterpart.** `../documents/NASA-STD-8739.8B.md` (software assurance and safety) and `../documents/NPR_7150.2D.md` for the verification expectations the paper's challenges would stress (our reading, comparison only). No NASA page here addresses operating envelopes or self-reverification.
