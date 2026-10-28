# NASA-STD-1006A — Space System Protection Standard

| | |
|---|---|
| **Owner office** | No "Responsible Office" line of the kind an NPD/NPR carries. Approved by signature: "Original Signed by Adam West for... Ralph R. Roe, Jr. ... NASA Chief Engineer," July 15, 2022 (Foreword, p.3). Exemptions from the standard's requirements need approval "by the Office of the NASA Chief Engineer" (§2.4 Order of Precedence, p.8) |
| **Kind and force** | NASA-STD (Technical Standard) — not self-imposing; binding only when invoked by law, directive, contract, or project document; see ../force.md |
| **Revision and status** | Revision A, approved July 15, 2022 (Foreword, p.3). Confirmed ACTIVE, Version A, Change 0, approval date 07/15/2022 per `standards.nasa.gov/standard/nasa/nasa-std-1006` (checked live, 2026-10-14). The Document History Log (p.2) extracted with no readable content in our text extraction; change history beyond Change 0 is unknown from it |
| **Where to get it** | standards.nasa.gov — search "NASA-STD-1006". Public copy, confirmed anonymously off-network on 2026-10-26: `https://standards.nasa.gov/sites/default/files/standards/NASA/A/0/2022-07-15-NASA-STD-1006A-Approved.pdf` |
| **Applies to** | "This NASA Technical Standard is applicable to all NASA programs and projects... It will apply to the Jet Propulsion Laboratory (a Federally Funded Research and Development Center [FFRDC]), other contractors, recipients of grants and cooperative agreements, and parties to other agreements... to the extent specified or referenced in applicable contracts, grants, or agreements" (§1.2, p.6) |

## What it is for, plainly
Six mandatory requirements that protect NASA spacecraft against deliberate, adversary interference — not against accidental hazards. It covers command-link encryption, backup command-link protection, protecting sensitive command information, resilience to loss of outside positioning/navigation/timing (PNT) services, and reporting unexplained interference.

## What it obliges
- [SSPR 1] "Programs/projects shall protect the command stack with encryption that meets or exceeds the Federal Information Processing Standard (FIPS) 140... Level 1" (§4.1.1, p.9); tailorable for hosted instruments, deep-space missions, and certain mission classes; does not apply to balloon or sounding rocket projects (§4.1.1.b, pp.9-10).
- [SSPR 2] "If a project uses an encrypted primary command link, any backup command link shall, at a minimum, use authentication" (§4.1.2, p.10).
- [SSPR 3] "The program/project shall protect the confidentiality of command link [Critical Project Information] as controlled unclassified information (CUI)" (§4.1.3, p.10).
- [SSPR 4] "If project-external PNT services are required, projects shall ensure that systems are resilient to the complete loss of, or temporary interference with, external PNT services" (§4.2.1, p.11).
- [SSPR 5] "Projects/Spectrum Managers/Operations Centers shall report unexplained interference to [the Mission Resilience and Protection Program (MRPP)] or to other designated notifying organizations" (§4.3.1, p.12).
- [SSPR 6] "Projects/Spectrum Managers/Operations Centers shall conduct proficiency training for reporting unexplained interference" (§4.3.2, p.13).
- All six are collected in a Requirements Compliance Matrix (Appendix A, p.14) that programs/projects use to mark each one Applicable or Not Applicable.
- Definitions (§3.2, pp.8-9) include Command Link, Command Stack, Critical Project Information, Deep Space ("beyond 2 million kilometers from the Earth"), and Hardware Commands — spacecraft commands "routed to a specific location and... executed on receipt, without any flight software interaction," also called backup or firecode commands.

## Where it stops
- All six requirements are tag-verified with zero children — no sub-clause anywhere in the standard carries its own "shall" (our reading, consistent with this standard's structure elsewhere).
- Not self-imposing: per NPR 7120.10B §1.2.1 (see ../force.md), a technical standard binds only when a law, directive, contract, or program/project document invokes it; nothing in NASA-STD-1006A's own text makes it mandatory on its own authority.
- Scope is purposeful, adversarial threats only — every "Objective" statement under §4.1-4.3 names "unauthorized access," "adversary," or "interference," never accidental or random hardware failure (pp.9-13).
- Several requirements carry explicit tailoring or exclusion language (SSPR 1's hosted-instrument and deep-space carve-outs, and the balloon/sounding-rocket exclusion, p.10).

## AI and machine-learning touchpoints
- No clause names AI, machine learning, or autonomy; the standard protects the command and navigation channel, not any onboard decision-making function (our reading).
- SSPR 4's PNT-resilience requirement is the closest point of contact: an AI-enabled onboard navigation or state-estimation function that depends on external PNT would need to satisfy the same resilience requirement as any other navigation design — the standard reaches the requirement placed on the system, not how the system is implemented inside (our reading).
- SSPR 1-3's command-stack and command-link-CPI protections would also bound any AI-based onboard autonomy capable of issuing or altering commands, since they protect the uplink channel itself regardless of what decides what to send (our reading).

## How it connects to other documents
- Implements NPR 1058.1 (NASA Enterprise Protection Program), NPR 7120.5 (NASA Space Flight Program and Project Management), and NPR 7120.8 (NASA Research and Technology Program and Project Management Requirements) (§1.1, p.6).
- Points to NASA/TP-2018-219822 (Navigation Filter Best Practices) and GPS interface specification IS-GPS-200 for SSPR 4 implementation guidance (§4.2.1.b, pp.11-12).
- Non-use of a specifically designated reference-document version, and conflicts between this standard and other requirements documents, are both resolved "by the delegated Technical Authority" (§2.1 and §2.4, pp.7-8).

## Traps
- Looking for a "Responsible Office" line the way an NPD or NPR carries one: this standard has none. The nearest equivalent is the Chief Engineer's approval signature and the Chief Engineer's exemption authority under the Order of Precedence clause.
- Reading six requirements with no sub-clauses as a sign of incomplete extraction: it is a confirmed structural property of this document, not a parsing miss.
- Assuming NASA-STD-1006A binds a project because it is written with "shall": per the standard-class rule in ../force.md, a technical standard still needs a law, directive, contract, or project document to invoke it before it binds anyone.

## Verified quotes
> "[SSPR 1] Programs/projects shall protect the command stack with encryption that meets or exceeds the Federal Information Processing Standard (FIPS) 140, Security Requirements for Cryptographic Modules, Level 1."
— NASA-STD-1006A, §4.1.1, p.9

> "[SSPR 4] If project-external PNT services are required, projects shall ensure that systems are resilient to the complete loss of, or temporary interference with, external PNT services."
— NASA-STD-1006A, §4.2.1, p.11

> "The requirements and standard practices established in this NASA Technical Standard do not supersede or waive existing requirements and standard practices found in other Agency documentation or in applicable laws and regulations unless a specific exemption has been obtained by the Office of the NASA Chief Engineer."
— NASA-STD-1006A, §2.4, p.8

> "Hardware Commands: Spacecraft commands that, once extracted by the spacecraft hardware from the uplink command channel, are routed to a specific location and are executed on receipt, without any flight software interaction. These commands may also be known as backup or firecode commands."
— NASA-STD-1006A, §3.2, p.9
