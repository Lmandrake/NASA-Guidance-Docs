# How binding is it? Document types, force, and where status lives

Page numbers below are the PDF page of the source as extracted.

## The ladder, plainly

| Type | What it is | Force |
|---|---|---|
| **NPD** (NASA Policy Directive) | Agency policy and who is responsible for it | Policy. States duties as "is responsible and accountable for"; typically carries no `shall`. A policy statement with no modal verb can still set scope (see `documents/NPD_8700.1F.md`). |
| **NPR** (NASA Procedural Requirements) | Agency requirements, numbered, with `shall` | Binding on NASA employees ("COMPLIANCE IS MANDATORY FOR NASA EMPLOYEES" on the cover). Reaches JPL and contractors through the contract. |
| **NID** (NASA Interim Directive) | Temporary requirement pending an NPD/NPR revision | Binding while in force. Has an expiration that NASA extends in a register without reissuing the PDF. |
| **NASA-STD / NASA-SPEC** (technical standard) | Engineering requirements, numbered `shall` statements | **Not self-imposing.** Binding only when law, a directive, a contract or a project document invokes it (NPR 7120.10B §1.2.1). |
| **NASA-HDBK** (handbook) | Guidance, lessons learned, techniques | Guidance, even where it contains `shall` sentences (NPR 7120.10B Appendix A). Becomes binding only where a contract or Agency document cites it. |
| **NASA/SP**, technical memoranda | Special publications, reports | Guidance or reference. Can be replaced by a Technical Authority's choice. |
| **JPL Rules** | JPL institutional requirements and guidance | JPL's own documents; not public, so not covered here. |

## The three clauses that settle most force questions

All from NPR 7120.10B, *Technical Standards for NASA Programs and Projects*, "Responsible Office:
Office of the Chief Engineer", effective June 01, 2022, expiring June 01, 2027 (p.1).

> "1.2.1 A technical standard is not “self-imposing,” i.e., it is not mandatory for use by a performing
> entity unless:
> a. Required by U.S. law or NASA directive, or
> b. Invoked by other NASA requirements documents (e.g., contracts, including but not limited to, the
> JPL FFRDC contract, program and project documents, grants, and agreements)."

— NPR 7120.10B §1.2.1, p.5

> "Although NASA handbooks may contain “shall” statements, they are not intended to be requirements
> documents. Handbooks, or portions thereof, containing procedural or process requirements may be
> cited in contract, program, and other Agency documents."

— NPR 7120.10B Appendix A, definition of Handbook, p.14

> "In this directive, all mandatory actions (i.e., requirements) are denoted by statements containing
> the term "shall." The terms "may" denotes a discretionary privilege or permission, "can" denotes
> statements of possibility or capability, "should" denotes a good practice and is recommended, but
> not required, "will" denotes expected outcome, and "are/is" denotes descriptive material."

— NPR 7120.10B Preface P.2(c), p.3. Most NPRs carry a conventions paragraph of this shape; read the
document's own one before deciding what a sentence binds (NPR 8000.4C has the same "are/is"
convention, which makes its definition of Risk descriptive).

**Who picks standards for a project:** NPR 7120.10B §3.1.1 (p.9) has program and project
managers, with delegated Technical Authority concurrence, select technical standards in priority
order: those mandated by law, those designated mandatory by NPDs and NPRs, then those needed for
mission success. Tailoring needs approval by the delegated Technical Authority (§3.2.1, p.10).

## Force-reading traps

- **Force can live in the stem.** A colon-terminated `shall` stem binds lettered children that carry
  no modal verb (NPR 7150.2D §3.8.1, p.27). Filtering on `shall` loses them.
- **Force can be carried in by quotation.** The Software Engineering Handbook reproduces NPR 7150.2D
  `shall` sentences verbatim. The NPR binds; the handbook copy does not.
- **Notes and Rationale blocks are non-normative.** In NODIS HTML they are the only indented
  paragraphs, which is a marker for annotation, not for depth.
- **Some standards say outright they are not mandatory.** NASA-STD-7009B §1.2.1 p.8: required
  application "is to be specified in program/project/organization/office directives."

## Where status lives (check the right register)

| Type | Register | Trap |
|---|---|---|
| NPD, NPR | NODIS current directives, `https://nodis3.gsfc.nasa.gov/Rpt_current_directives.cfm`; per directive `https://nodis3.gsfc.nasa.gov/displayDir.cfm?t=<NPR\|NPD>&c=<number>&s=<revision>` | A cover can show an expiry the register has extended (NPD 1000.0C cover 2025-12-30, NODIS 2027-06-30). This list carries no standards and no NIDs, so absence from it proves nothing for those. |
| NID | NODIS "Other NASA-Level Documents", `https://nodis3.gsfc.nasa.gov/OPD/OPD_list.cfm` | The extension is prose at the front of the Subject cell, not a column, in several spellings. NASA does not reissue the PDF when it extends a NID. |
| NASA-STD, NASA-HDBK | standards.nasa.gov (search by number) | The site root can bounce anonymous users to sign-on while deep document pages load fine. An approved document can keep DRAFT running headers (NASA-HDBK-7009B). |
| SWEHB (NASA-HDBK-2203) | swehb.nasa.gov, a living wiki | Retirement of a page is recorded on its container page, not on the attachment. |

**Context, not a rule:** as retrieved on 2026-09-25, the NODIS front page said that directive updates were
paused during an Agency-wide review and that "Previously issued directives remain in effect during
this period." Do not read that as automatically extending every printed
expiry; check each directive's own record.

**A page count is not a completeness check.** Two renderings of NPR 8715.3D differed (54 vs 47
pages) and the shorter was the later state, because a cancelled appendix was removed. Use the
change log.
