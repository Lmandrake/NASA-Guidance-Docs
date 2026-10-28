# Nagarajan et al. (2021) — ASTM F3269 - An Industry Standard on Run Time Assurance for Aircraft Systems

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Nagarajan et al. (authors from a university, industry, the FAA and DLR); AIAA SciTech 2021 Forum |
| **Kind** | Research / conference paper about a standard (not the standard itself) |
| **Status** | AIAA SciTech 2021 Forum paper, DOI 10.2514/6.2021-0525. Open-access author submission (p.1). It describes the then-ongoing second revision of the standard, which was "undergoing the ASTM balloting process" (p.2), so details may differ from the published edition (p.11). |
| **Where to get it** | Public: `https://elib.dlr.de/144352/` (PDF: `https://elib.dlr.de/144352/1/latestsubmission_v1_ASTM%20F3269_SciTech_Control-ID_3453655.pdf`), confirmed anonymously off-network, 2026-10-26. The standard itself is paywalled; see `ASTM_F3269-21_RTA.md`. |
| **Binds whom** | No one. |

**What it is good for, relative to NASA's documents.** A free, readable account of the reasoning behind
the run time assurance (RTA) architecture standard, written by members of its working group. It does not
reproduce the standard; statements below are the paper's own and are attributed to it. For the
standard's page in this skill, see `ASTM_F3269-21_RTA.md`.

**Key content for AI / machine-learning assurance.**
- Defines run time assurance in one passage: detect misbehavior, switch to an alternate algorithm or
  bound outputs; "This is run time assurance." (§I, p.2). Positions RTA as a strategy for functions
  that may not be certifiable by traditional design assurance, and says it "will also play a role" for
  adaptive controllers and AI/ML functions (Abstract, p.1).
- Paper's description of the generic architecture: Input Manager, Safety Monitor, RTA Switch, Recovery
  Function and Complex Function, with term definitions in its Table 1 (§III.B, pp.4-5). Two variants:
  the monitor observes the Larger System, or observes the Complex Function directly (§III.B, p.5).
- The "Larger System" is the system for which assurance is argued, chosen by the applicant "in
  cooperation with the certification authority" (§III.A, p.4).
- Paper's account of assurance level and coverage: RTA components "must have the same assurance level"
  as the complex function's required level, and every operating point needs an available monitor and
  recovery function, otherwise operation there is disallowed or new ones are developed (§III.C, pp.6-7).
- Multi-monitor architectures were new in the second edition; arbitration is to be done within the
  Safety Monitor, with clear priority logic required but implementation not prescribed (§III.D, p.8).
- Worked appendix examples include a machine-learning adaptive autopilot with the pilot as a secondary
  recovery (§III.E, p.9). Certification benefits are listed in §III.F (p.11).

**Nearest NASA counterpart.** None in `../documents/` addresses RTA architecture directly (our reading).
The companion NASA-authored paper is on `Skoog_2020_ASTM_F3269-17_Autonomous_Aircraft.md`.
