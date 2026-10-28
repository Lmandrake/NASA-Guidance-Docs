# Skoog et al. (2020) — Leveraging ASTM Industry Standard F3269-17 for Providing Safe Operations of a Highly Autonomous Aircraft

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | Skoog et al. (authors from NASA Armstrong Flight Research Center, a university, and the FAA); IEEE Aerospace Conference 2020, Big Sky, MT (NTRS record) |
| **Kind** | Research / conference paper (NTRS record 20200001756) plus companion presentation (NTRS record 20200001821); not NASA governance |
| **Status** | Paper: NTRS publication date 2020-01-08, distribution PUBLIC (NTRS record). Presentation: 2020-03-10, distribution PUBLIC (NTRS record). The IEEE version is DOI 10.1109/AERO47225.2020.9172434 and its IEEE copy is paywalled. The NTRS paper has the same title as the IEEE paper and is assumed to be the same work; the two texts were not compared. The NTRS copy's cover says "Submission due 18 Oct 2019" and "Revision due Jan 2020" (p.1). |
| **Where to get it** | Public: paper `https://ntrs.nasa.gov/citations/20200001756`; presentation `https://ntrs.nasa.gov/citations/20200001821`. Confirmed anonymously off-network, 2026-10-26. The standard itself is paywalled; see `ASTM_F3269-21_RTA.md`. |
| **Binds whom** | No one. |

**What it is good for, relative to NASA's documents.** A NASA-center-authored account of how the ASTM
F3269-17 run time assurance (RTA) architecture was extended for a highly autonomous aircraft. It is a
research paper by NASA authors, not NASA policy or requirements (our reading). For the standard, see
`ASTM_F3269-21_RTA.md`; for a later paper by members of the standard's revision group, see
`Nagarajan_2021_ASTM_F3269_RTA.md`.

**Key content for AI / machine-learning assurance.**
- NTRS abstract: the paper "expands upon the ASTM industry standard F3269-17 to outline a run-time
  assurance (RTA) network architecture" for safe flight operations of a highly autonomous aircraft
  (NTRS record 20200001756).
- Multiple separate monitors instead of a single "mother of all" monitor, each mapped to a pilot
  responsibility and easier to verify and validate (paper §"The Use of Multiple Separate Monitors", p.5).
  Each monitor must "declare the criticality" of the boundary breach it flags, reported to the RTA Switch
  (p.6). The paper says the weighting of rules of behavior should be set by "society and our legal
  system" rather than design engineers (p.6).
- The Input Manager is recast as an "Integrity Manager" with four categories of integrity monitor:
  self-health, derived data, dynamic consistency, outer-loop integrity verification (p.7-8).
- A second RTA switch for strategic recovery (re-plan, return to base, land, ditch) while tactical
  monitors stay available (pp.9-10); the Command Coupler isolating autopilot-specific interfaces (p.13).
- Presentation (NTRS 20200001821): slide deck of the same topics, including a slide on "Moral Compass &
  Rules of Behavior" (slides at PDF pp.7-9 and p.21) and a "Leveraging the ASTM Standard" comparison slide (p.14).
  It says the ASTM standard "was published October 2017" (p.9, slide text).

**Nearest NASA counterpart.** None in `../documents/` addresses RTA architecture directly (our reading).
