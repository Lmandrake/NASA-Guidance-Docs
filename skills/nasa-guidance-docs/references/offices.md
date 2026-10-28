# Offices: who owns what, and how they hand off

Page numbers are the source's page anchors as extracted. Interpretation is marked "(our reading)".

## Who owns which documents

The owner is the "Responsible Office" on the document's cover, or the approving official where a
standard has no such line.

| Office | Head reports to | Owns (in this skill) |
|---|---|---|
| **Office of the Chief Engineer (OCE)** | "The Chief Engineer reports to the NASA Associate Administrator." (NPD 1000.3F §4.11.2, p.47) | NPR 7150.2D, NPR 7123.1D, NPR 7120.10B, NASA-STD-7009B and NASA-HDBK-7009B, NASA-STD-1006A (approved by the Chief Engineer). The Software Engineering Handbook publishes no owner line on its pages |
| **Office of Safety and Mission Assurance (OSMA)** | "The Chief, Safety and Mission Assurance reports to the NASA Associate Administrator" (NPD 1000.3F §4.13.2, p.51) | NASA-STD-8739.8B, NPD 8700.1F, NPR 8715.3E, NPR 8705.2C, NPR 8705.4B, NPR 8000.4C, NPR 8705.6 (owner per the document), the System Safety and Risk Management Handbooks |
| **Office of the Chief Information Officer (OCIO)** | "The CIO reports to the NASA Administrator." (NPD 1000.3F §4.9.2, p.44) | NPR 2810.1F, NPD 2810.1F, NPD 2540.1K, NPD 2800.1F, NID 2800.149 |
| **Associate Administrator** | — | NPR 7120.5F (space flight program and project management), NPD 1000.3F (the NASA organization) |
| **Office of the Chief Health and Medical Officer (OCHMO)** | — | NPR 7120.11A (Health and Medical Technical Authority) |
| **Office of Communications** | — | NID 1383.155 (AI-generated media) |

Each document page in `documents/` quotes its own owner line.

## What each office is for, in its own charter

All from NPD 1000.3F, *The NASA Organization* (Responsible Office: Associate Administrator;
effective January 20, 2025, expiring January 20, 2029).

- **OCE:** "provides policy direction, oversight, and assessment for NASA engineering … Also, it is
  responsible for Agency-level standards and policies as applied to engineering and program
  management" (§4.11.1, p.47). The Chief Engineer "Serves as the lead Technical Authority for
  engineering" (§4.11.2.1c, p.47) and "Coordinates with OCIO and OSMA in the leadership of enterprise
  protection" (§4.11.3.4, p.49).
- **OSMA:** "provides policy direction, functional oversight, and assessment for all Agency safety,
  reliability, maintainability, quality engineering and assurance, software assurance, risk
  management, orbital debris mitigation, nuclear flight safety, aviation safety, and planetary
  protection activities" (§4.13.1, p.51). The Chief SMA "Serves as the lead Technical Authority for
  safety and mission assurance, providing independent oversight of programs and projects" (§4.13.2,
  p.51).
- **OCIO:** "The Chief Information Officer (CIO) is the principal advisor to the Administrator and
  other senior officials on matters pertaining to IT, the NASA Enterprise Architecture (EA),
  cybersecurity, records management, and privacy." (§4.9.1, p.44)

## AI-specific roles

- **Chief Data Officer (CDO)** sits within OCIO: "The CDO serves as the OCIO designated official for
  the use, protection, dissemination, and generation of data. In that capacity, the CDO works closely
  with the NASA Chief Artificial Intelligence (CAIO) Officer, leads and coordinates OCIO support to the
  CAIO" (NPD 2800.1F §5, p.5; NPD 2800.1F: Responsible Office OCIO, effective January 11, 2025,
  expiring January 11, 2030).
- **Chief AI Officer (CAIO):** named in NPD 2800.1F (p.5; the NASA CIO delegates IT Authority to,
  among others, the "CDO, CAIO, SAISO", p.7) and in NID 1383.155 §3.a (p.3). The CAIO role also
  follows from federal policy; see `external/` for the OMB memoranda. NASA's public AI page has been renamed: `https://www.nasa.gov/ai/` now redirects to `https://www.nasa.gov/super-intelligence/`, titled "Super Intelligence - NASA" (checked 2026-10-26), so search for either name.
- **Senior Agency Information Security Officer (SAISO), Center CISOs, Information System Owners:**
  roles defined in NPR 2810.1F §1.2.3 (pp.12–14); see `documents/NPR_2810.1F.md`.

## The Technical Authorities: the main hand-off mechanism for flight work

Defined in NPR 7120.5F §3 (quoted in full in `documents/NPR_7120.5F.md`):

> "TA originates with the Administrator and is formally delegated to the NASA AA and then to the NASA
> Chief Engineer for Engineering TA; the Chief, Safety and Mission Assurance for SMA TA; and then to
> the Center Directors. The Administrator delegates Health and Medical Technical Authority (HMTA) to
> the NASA CHMO. Subsequent TA delegations are made to selected individuals who are funded
> independent of the Programmatic Authority."

— NPR 7120.5F §3.3.2, p.46

- **Engineering TA (ETA)** owns engineering design processes and rules (§3.3.7, p.47); **SMA TA**
  owns SMA processes (§3.3.9, p.48); **HMTA** owns health and medical policy (§3.3.10, p.49; NPR
  7120.11A).
- The program or project manager stays "ultimately responsible for the safe conduct and successful
  outcome" (§3.3.1, p.45).
- **Disagreement goes up, not around.** A Formal Dissent is raised "at a minimum of two levels of
  management above the original program or project decision" (§3.4.2, p.49) and can go "even to the
  NASA Administrator, if necessary" (§3.4.5, p.49).
- **Standards and tailoring run through the TAs.** Program and project managers select technical
  standards "with delegated Technical Authority concurrence" (NPR 7120.10B §3.1.1, p.9); tailoring a
  Technical Authority requirement needs formal approval by the delegated TA (NPR 7120.10B §3.2.1,
  p.10); relief from mission-assurance requirements follows NPR 8715.3E.
- **Software:** NPR 7150.2D has the project manager determine safety-criticality "in conjunction with
  the SMA organization" (SWE-205, p.26), and its Requirements Mapping Matrix tailoring needs
  Technical Authority approval (Chapter 2; see `documents/NPR_7150.2D.md`).

## IV&V

- NASA's Independent Verification and Validation (IV&V) program is assigned by project category, not
  chosen by the project: Category 1, Category 2 with Class A or B payloads (NPR 8705.4), and projects
  the Mission Directorate selects (NPR 7150.2D SWE-141, p.25). The plan follows NASA-STD-8739.8B
  (SWE-131).
- Independence is defined in NASA-STD-8739.8B §4.4.1.2 (p.48) as technical, managerial and
  financial independence: all three are about people and organizations (our reading: none of them
  speaks to two reviewers sharing one tool or model).
- What IV&V is for, in its own words: see `documents/NASA_IVV_Capabilities_Handout_FY25.md`.

## JPL

JPL is a Federally Funded Research and Development Center (FFRDC). NASA requirements reach it through
the contract: a technical standard is mandatory only where invoked, including by "the JPL FFRDC
contract" (NPR 7120.10B §1.2.1b, p.5), and NASA-STD-7009B reaches an FFRDC "only to the extent
specified or referenced in the applicable contracts" (§1.2.2). JPL implements them through institutional rules, which are not public and not covered here.
