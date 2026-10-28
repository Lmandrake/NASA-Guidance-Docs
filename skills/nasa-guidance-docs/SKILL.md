---
name: nasa-guidance-docs
description: Map of NASA and JPL governance documents for flight missions, software and AI/ML/autonomy (owner, force, status, reach), plus EASA, FAA, NIST, DO-178C, ISO 42001, OMB. Use whenever a task cites NPR 7150.2, NASA-STD-8739.8, the SWEHB, NASA-STD-7009, NPR 7123.1, 7120.5, 8705.4, 8715.3, 8000.4, 2810.1, a NID or JPL Rules; asks "is this binding", "still in force", "which office owns this", or what NASA requires for safety-critical software, AI, software classes, IV&V, tailoring or waivers; before quoting a NASA requirement; or when mapping AI risks to NASA documents.
---

# NASA guidance documents: who owns what, how binding it is, where it stops

A map of NASA's software, safety and mission-assurance governance as it bears on flight systems,
including systems with an AI or machine-learning component, plus the outside frameworks people
compare it with. Facts carry locators; our interpretations are marked "(our reading)". It is **not**
the citation authority: before quoting anything into work another person will rely on, open the
source and check the clause at its location.

## How to navigate

| You need | Read |
|---|---|
| How binding a document type is, how standards become binding, how to check status | `references/force.md` |
| One NASA document: owner, force, status, where to get it, what it obliges, where it stops, AI touchpoints | `references/documents/<DOC>.md` — full list in `references/INDEX.md` |
| Which office owns what; how OCE, OSMA, OCIO, CDO, the Chief AI Officer, IV&V and the Technical Authorities interact | `references/offices.md` |
| How the documents reach an AI-enabled flight system, rung by rung, and where evidence methods stop transferring | `references/ai_crosswalk.md` |
| An outside framework (EASA, FAA, NIST, DoD, ASTM, RTCA, ISO, OWASP, CISA, OMB/EO) | `references/external/<NAME>.md` — **never** citable as NASA coverage |

**Headline pages, full treatment:** `NPR_7150.2D` · `NASA-HDBK-2203` (SWEHB) · `NASA-STD-8739.8B` ·
`NASA-STD-7009B` (with HDBK-7009B) · `NPR_7123.1D` · `NPR_7120.5F` · `NPR_7120.10B` · `NPR_8705.2C` ·
`NPR_8705.4B` · `NPR_8715.3` (3D and 3E) · `NPD_8700.1F` · `NPR_8000.4C` (with the Risk Management
Handbook) · `NID_1383.155` · `NID_2800.149` · `NPR_2810.1F` · `NPD_2540.1K` · `NASA-STD-1006A` ·
`NASA-SP-2010-580`. Every other document has a short page. Each page has the same sections,
so jump straight to "Where it stops" or the AI touchpoints.

## The traps that cause most wrong answers

1. **Force depends on the document type, not on the word "shall".** An NPR binds NASA employees and
   reaches JPL and contractors through the contract. A NASA technical standard "is not
   'self-imposing'" (NPR 7120.10B §1.2.1, p.5): it binds only where law, a directive, a contract or a
   project document invokes it. A handbook is guidance even when it reproduces an NPR's `shall`
   sentence word for word (NPR 7120.10B Appendix A, p.14). An NPD assigns duties ("is responsible and
   accountable for") and typically has no `shall`.
2. **A requirement's force often lives in its stem.** NPR 7150.2D §3.8.1 binds items (a)–(g) through
   one `shall` in the stem; item (d) has no modal verb. Filtering on `shall` loses these.
3. **Some standards say outright they are not mandatory.** NASA-STD-7009B §1.2.1 p.8: required
   application "is to be specified in program/project/organization/office directives".
4. **A definition can be borrowed from a document that has since moved.** NPR 7150.2D's "Safety
   Critical" definition (Appendix A, p.49) is marked "(Source NPR 8715.3)"; the definition sits in
   cancelled NPR 8715.3D text and is absent from live 8715.3E. See `documents/NPR_8715.3.md`.
5. **Status lives in a register, not on the cover.** NODIS's current-directives list covers NPDs and
   NPRs only. NIDs have a second NODIS register, and NASA extends a NID without reissuing its PDF.
   Standards are on standards.nasa.gov. An approved document can still carry DRAFT running headers.
6. **IV&V clauses bind only where IV&V is assigned.** NPR 7150.2D SWE-141 (p.25) sets which projects
   get independent verification and validation; clauses addressed to the IV&V provider in
   NASA-STD-8739.8B §4.4 apply only on those projects.
7. **Gates come before content.** A software requirement reaches a component only if its software
   class is marked for it (NPR 7150.2D Appendix C; classes in Appendix D), and the safety-critical
   ones only after the safety-criticality determination (SWE-205, p.26).
8. **"No NASA document mentions AI" is false; "no NASA requirement is AI-specific" is the defensible
   claim** for the documents mapped here. NPR 7150.2D never uses the words; the SWEHB (topics 7.25,
   8.25), the Risk Management Handbook and NASA-HDBK-7009B do, as guidance. NID 1383.155 is about
   generated media, not flight software.
9. **Outside text is comparison, not coverage.** An EASA objective or a NIST practice can be stronger
   than any NASA clause on a topic; that is a finding about NASA's documents, never evidence that
   NASA requires it.
10. **Never write "NASA covers X" or "NASA has a gap in X" from this skill.** Say what a clause says,
    where it stops, and whose call the determination is (usually the project's Technical Authorities).

## How this has been used (worked patterns)

These are methods for using this material. Figures removed until the study's results are published
(the study is active and ongoing).

**1. Does a requirement's own reason survive when AI does the work?** The Software Engineering
Handbook publishes a Rationale for each NPR 7150.2D requirement. Read NASA's stated reason for every
one and ask whether it still holds when a learned model writes, decides or generates. Figures removed until the study's results are published (the study is active and ongoing).
Method lesson: follow the first pass with an adversarial re-read that tries to withdraw each flag, and
report that a reason survives, not that the evidence method still works. See `references/ai_crosswalk.md` §5.

**2. Which documents reach a risk, and how binding is that text?** For each item on a risk list,
find the NASA clauses that bear on it, quote each verbatim with its locator, record the document's
force (NPR, standard, handbook) and whether something invokes it, and argue for and against the fit
with no verdict. Then roll up per document (figures removed until the study's results are published). A roll-up can
be turned into per-document edit packages: the existing clause verbatim, the proposed edit beside
it, and whose obligation the edit touches. Check every quote at its cited page; models fabricate
citations and are more confident when they do.

**3. A consequence tier for AI controls, built from determinations projects already make.** Key the
tier to NPR 7150.2D software class (SWE-020, Appendix D) and the safety-critical determination
(SWE-205 per NASA-STD-8739.8B §4.2 criteria), which then trigger SWE-023, SWE-134, SWE-219 (100%
MC/DC) and SWE-220 (cyclomatic complexity ≤15). The ladder transfers; its top-rung evidence does not,
because coverage and complexity measure code paths, not learned behaviour. Walk-through:
`references/ai_crosswalk.md` §2.

**4. A requirement can be met in full and deliver nothing.** NASA-STD-8739.8B §4.4.1.2 (p.48)
defines IV&V independence by three organizational parameters: technical (not involved in
development), managerial (not in the same organization) and financial (budget controlled
independently). Two reviews by different contractors, on different budgets and reporting lines, both
using the same underlying model, satisfy all three while sharing one failure mode (our reading). Ask
of every requirement: what is it for, and does the proxy still deliver that?

**5. Routing a question between offices without taking anyone's authority.** OCIO decides whether an
AI tool is authorized for NASA use; whether its output is fit to inform a mission or safety decision
is an assurance question for the Technical Authorities. A workable interface (our reading): assurance assessment runs in parallel with OCIO authorization and stays provisional until
authorization lands; a mission that needs a tool class outside the authorized set sends OCIO a
documented capability need; and in the same breath, an assurance result grants no exemption from
OCIO controls. See `references/offices.md` for the offices.

**6. Is this document in force?** NASA-STD-8739.9: standards.nasa.gov's CSV says INACTIVE with a
cancellation notice while its HTML page shows a later revalidation date (04/09/2018). NID 1383.155:
the cover says expired 2026-09-15, the NODIS register says extended to 2027-09-15. NPD 1000.0C: cover
2025-12-30, NODIS 2027-06-30. Check the register for that document class; raise conflicts with a
subject-matter expert rather than resolving them in code.

**7. Is this handbook text binding?** No, unless something cites it as a requirement (NPR 7120.10B
Appendix A). The SWEHB quotes NPR `shall` text verbatim, and its AI topic 7.25 asks that "each node in
a neural network must be shown to affect the solution and all paths evaluated" while NPR 7150.2D
never mentions neural networks. NASA's own material disagrees with itself there; carry both.

**8. Is a policy any good?** NPR 8705.6 (p.17) separates auditing compliance with a standard from
assessing effectiveness against principles. Score draft requirements on the four words NPR 8621.1D uses for
mishap recommendations (p.32: clarity, verifiability, achievability, traceability) and ask whether
following each one would change a decision.

## When writing for someone else

- Every claim about a document gets a locator: document, clause or SWE tag, page (say printed or PDF).
  Quote only text checked against the source at that location.
- Mark interpretation as interpretation.
- Spell out acronyms on first use and use NASA's own terms.
- JPL's institutional rules are not public and are not covered here; cite the public NASA document
  (usually NPR 7150.2D) instead.

## Keeping this current

Pages record the revision they were written against. When NASA issues a new revision, update that
page's status row and re-check its quotes rather than appending a correction beside the old text.
Provenance and scope: `docs/DESIGN.md` at the repo root.
