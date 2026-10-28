# NASA-STD-8739.8B — Software Assurance and Software Safety Standard

| | |
|---|---|
| **Owner office** | "This standard was developed by the NASA Office of Safety and Mission Assurance (OSMA)." — NASA-STD-8739.8B, Foreword, p.3 |
| **Kind and force** | NASA-STD (NASA Technical Standard) — not self-imposing by itself; binding only where a directive, contract or project document invokes it. NPR 7150.2D §3.6 invokes it directly for every project ("[the project manager] shall plan and implement software assurance, software safety, and IV&V (if required) per NASA-STD-8739.8" — SWE-022). See `../force.md`. |
| **Revision and status** | Revision B, "Approved: 2022-09-08," cover page states "Superseding NASA-STD-8739.8A" (p.1). No expiration date or next-review date is stated anywhere in the document's 65 pages. Marked "APPROVED FOR PUBLIC RELEASE – DISTRIBUTION IS UNLIMITED" (p.1). Current as of this writing; check standards.nasa.gov for a later revision. |
| **Where to get it** | standards.nasa.gov, search by number (NASA-STD documents are not carried in the NODIS directive register). Public copy, confirmed anonymously off-network on 2026-10-26: `https://standards.nasa.gov/system/files/tmp/NASA-STD-87398%20REV%20B.pdf` |
| **Applies to** | "This NASA Technical Standard applies to the assurance of software created by or for NASA projects, programs, facilities, and activities" (§1.2, p.6). Reaches the Jet Propulsion Laboratory (JPL) and other contractors, grant recipients, or parties to agreements "only to the extent specified or referenced in their contracts, grants, or agreements" (§1.2, p.6). |

## What it is for, plainly

This standard tells a NASA project how to assure its software and, where applicable, how to run Independent Verification and Validation (IV&V) on it. Its own purpose statement: "to define the requirements to implement a systematic approach to Software Assurance (SA), software safety, and Independent Verification and Validation (IV&V) for software created, acquired, provided, or maintained by or for NASA" (§1.1, p.5). It is keyed one-to-one to NPR 7150.2D's software engineering requirements (SWE tags) rather than standing on its own list: Table 1 pairs each applicable SWE requirement with the assurance task that goes with it.

## What it obliges (or advises)

- Carry out the Table 1 assurance and safety tasks "per the requirements marked applicable in the software engineering requirements mapping matrix for the software component" — the applying project's tailoring record governs which rows apply (§4.3, SASS-01, p.16).
- Decide whether software is safety-critical against five named criteria and trace the decision to the system hazard analysis (§4.2, pp.15–16; see "Safety-criticality determination criteria" below).
- Where safety-critical, implement the safety-critical software requirements the standard sets, under the chain NPR 7150.2D sets up (SWE-023, SWE-134, SWE-219, SWE-220 — see `NPR_7150.2D.md`).
- Where IV&V applies, keep it independent on three named counts: "technical independence, managerial independence, and financial independence" (§4.4.1.2, p.48).
- Where IV&V applies, verify and validate the source code "through the use of analysis tools (including but not limited to static, dynamic, composition, and formal analysis tools)" (Table 1, IV&V requirements, p.54).
- Build an IV&V Project Execution Plan (IPEP) documenting the scope, methods and rigor of IV&V analysis, reviewed and concurred by the NASA SMA Technical Authority (p.50).
- Give the Safety and Mission Assurance (SMA) organization signature authority on software plans and documentation (§1.3, p.6).
- Where tailoring is needed, document it as part of program/project requirements and get it approved by the responsible Center Technical Authority in accordance with NPR 8715.3 (§1.4, p.6).
- Balance IV&V effort against resources under the standard's "appropriate assurance" principle: "it is not possible to provide IV&V on all aspects of a project's software, the IV&V Provider and project should balance risks against available resources to define an IV&Vprogram for each project" (§4.4.1.6.b, p.49).

## Where it stops

- **IV&V's "shall" clauses bind only an IV&V effort that already exists.** The standard's own words: "The IV&Vrequirements are applicable to all IV&Vefforts performed on a software development project, as tailored by the IV&V Project Execution Plan... IV&V as a risk mitigation activity, and as such, the application of IV&Vanalysis and the rigor of that analysis is driven by the IV&V Provider's assessment of software risk" (p.50). This standard does not itself decide which projects get an IV&V Provider — see Trap below.
- **Hazard-analysis-gated.** Software counts as safety-critical only where the hazard analysis makes it so: "Software is classified as safety-critical if the software is determined by and traceable to hazard analysis" (§4.2 Note, p.16).
- **Independence is defined about people and organizations, never about the instrument used.** All three independence parameters (technical, managerial, financial, §4.4.1.2, p.48) are properties of the reviewing organization, not of any tool or method it uses (our reading).

## AI and machine-learning touchpoints

- The standard names zero AI/ML/autonomy-specific clauses: the words "artificial intelligence," "machine learning," "autonomy," and "neural" occur zero times across its 65 pages, against 1,029 occurrences of "software" and 11 of "auto-generat" (our count).
- SWE-205 of NPR 7150.2D sends every project's safety-criticality call to this standard's five criteria (§4.2, pp.15–16) before any AI-enabled component could occupy a safety-critical role at all (our reading).
- The source-code analysis-tool clause (Table 1, p.54) names the *method* (static/dynamic/composition/formal analysis tools) but not what runs it; nothing in the text excludes an AI-assisted analysis tool from satisfying this clause, which is a gap in specificity rather than a stated allowance (our reading).
- The three independence parameters (§4.4.1.2, p.48) are written entirely about personnel and organizations. If a developer's analyst and an "independent" IV&V reviewer both query the same trained model, all three organizational parameters can be satisfied while the two reviews still share an error source — the standard's text does not reach that case (our reading).

## How it connects to other documents

- Invoked by NPR 7150.2D §3.6 (SWE-022) for every project's software assurance/safety/IV&V planning, and by SWE-205/SWE-023 for the safety-critical determination and its downstream requirements — see `NPR_7150.2D.md`.
- NPR 7150.2D §3.6 (SWE-141) sets which projects must run software IV&V at all (NPR 7120.5 Category 1 projects; Category 2 projects with Class A or B payload risk classification per NPR 8705.4; or projects the Mission Directorate Associate Administrator selects) — see `NPR_7150.2D.md` and `NPR_8705.4B.md`.
- Superseded and cancelled NASA-STD-8719.13 (Software Safety): the document history log records the reason for the prior revision as bringing software safety requirements into this one standard and cancelling 8719.13 (Document History Log, p.2; paraphrase, not verified verbatim — the history-log table did not survive text extraction cleanly).
- Disagrees with NPR 7150.2D's own Appendix C on the section references given for two shared requirements, SWE-032 and SWE-086 (our cross-document check; the specific conflicting section numbers were not re-verified in this pass — flagged as a NASA-vs-NASA inconsistency, not a defect in either document alone).

## Traps

- **Tailoring runs through the Center Technical Authority, not through the Chief, SMA, directly.** §1.4 (p.6) names the responsible Center TA as the approver for a program/project's tailoring request, under NPR 8715.3's process — do not assume relief from this standard is granted at the Agency SMA level by default.
- **Check that a copy is the released standard.** Verify any copy, and any citation to a later revision, against standards.nasa.gov; a draft carries a not-approved notice on its cover page, so read the whole cover, not just the header line.
- **IV&V clauses read as universal "shall" statements but are not.** Every "The IV&V Provider shall..." sentence in Table 1 presupposes a project that already has an IV&V Provider assigned. Whether that is true for a given project is decided elsewhere, by NPR 7150.2D's SWE-141 (category and payload-class gate) — not by anything in this standard's own text.
- Reading the five safety-critical criteria (§4.2) as requiring all five: the standard's own wording is "if it meets **at least one**" (p.15) — any single criterion is sufficient.

## Verified quotes

> "The purpose of the Software Assurance and Software Safety Standard is to define the requirements to implement a systematic approach to Software Assurance (SA), software safety, and Independent Verification and Validation (IV&V) for software created, acquired, provided, or maintained by or for NASA."
— NASA-STD-8739.8B, §1.1, p.5

> "Software is classified as safety-critical if it meets at least one of the following criteria: Causes or contributes to a system hazardous condition/event, Provides control or mitigation for a system hazardous condition/event, Controls safety-critical functions, Mitigates damage if a hazardous condition/event occurs, Detects, reports, and takes corrective action if the system reaches a potentially hazardous state."
— NASA-STD-8739.8B, §4.2, pp.15–16

> "Three parameters define the independence of IV&V: technical independence, managerial independence, and financial independence."
— NASA-STD-8739.8B, §4.4.1.2, p.48

> "The IV&V Provider shall verify and validate the source code through the use of analysis tools (including but not limited to static, dynamic, composition, and formal analysis tools)."
— NASA-STD-8739.8B, Table 1 (IV&V requirements), p.54

> "The IV&V requirements are applicable to all IV&V efforts performed on a software development project, as tailored by the IV&V Project Execution Plan."
— NASA-STD-8739.8B, IV&V Requirements overview, p.50

> "The responsible project manager shall perform the software assurance and software safety activities defined in Table 1 per the requirements marked applicable in the software engineering requirements mapping matrix for the software component. (SASS-01)"
— NASA-STD-8739.8B, §4.3, p.16

> "Tailoring of this standard for application to a specific program or project is documented as part of program or project requirements and approved by the responsible Center Technical Authority (TA) in accordance with NPR 8715.3, NASA General Safety Program Requirements."
— NASA-STD-8739.8B, §1.4, p.6
