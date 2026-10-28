# Chien et al. (2006) — Lessons Learned from the Autonomous Sciencecraft on Earth Observing One

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Authors from the Jet Propulsion Laboratory, NASA Goddard Space Flight Center and Interface & Control Systems (first author Chien, with other authors); workshop paper (title block, p.1) |
| **Kind** | Research paper / experience report (workshop paper) |
| **Status** | 2006 workshop paper; the venue (IWPSS 2006) is taken from the host URL, as the paper's first page does not name it. No version or revision statement in the text. |
| **Where to get it** | Public: `https://www.stsci.edu/largefiles/iwpss/2006620252chien-s-iwpss2006.pdf` (hosted by the IWPSS 2006 workshop host), confirmed anonymously off-network, 2026-10-26 |
| **Binds whom** | No one. |

**What it is good for, relative to NASA's documents.** A flown example, from a spacecraft that ran AI software as its primary operations system, of what reliability and validation practice looked like for onboard planning and learned event detectors. NASA's governance documents say what must be assured; this paper shows one concrete way a team got there and what it found hard (our reading).

**Key content for AI / machine-learning assurance.**
- Scope: the software combined model-based planning and scheduling, procedural execution, and event detection "learned by support vector machine (SVM) techniques" (Abstract, p.1). It was in experimental use from 2003 and the primary operations system from November 2004 (Abstract, p.1).
- Architecture for reliability: the first lesson is that autonomy software must "exist in an architecture designed for reliability" within a rigorous systems-engineering and validation framework (Lessons Learned, p.3). The three layers were a planner, an execution layer and the original flight software (Introduction, p.1).
- Validation burden: "All of the AI technologies had to operate extremely reliably for the integrated system to function reliably" (p.4). Reliability came from a redundant layered architecture, a requirements-engineering process, multi-level testing and spiral deployment, and even so the engineering challenges "were arduous" (p.4).
- Risk posture: the authors note that deploying in an extended mission allowed greater risk than for a launching spacecraft in its prime mission, and that a JPL and MIT program on model-based monitoring and diagnosis of the autonomy software itself was begun in anticipation of more risk-averse future missions (p.4).
- Predictability by design: a simpler optimization scheme was flown to reduce computation and "increase the predictability of the system" (p.3). Operator-commanded changes appear to the planner as unexplained state changes, so suppressing autonomous responses to them is discussed (p.3).
- Reported benefits: a 100x increase in science return per megabyte downlinked and over $1M/year lower operations cost (Abstract, p.1; Impact, p.2).

**Nearest NASA counterpart.** `../documents/NASA-STD-8739.8B.md` (software assurance and software safety) for the assurance activities, and `../documents/NPR_7150.2D.md` for software engineering requirements. This paper predates both and addresses no requirement in them directly; it is background on practice (our reading).
