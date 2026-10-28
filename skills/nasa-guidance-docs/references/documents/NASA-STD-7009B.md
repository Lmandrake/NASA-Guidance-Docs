# NASA-STD-7009B — Standard for Models and Simulations (companion: NASA-HDBK-7009B)

| | |
|---|---|
| **Owner office** | NASA-STD-7009B: approval signature "Joseph W. Pellicciotti NASA Chief Engineer" (Foreword, p.3) — no separate "Responsible Office" label appears in the cover text. NASA-HDBK-7009B: "Office of the NASA Chief Engineer" (cover, p.1). |
| **Kind and force** | NASA-STD-7009B is a NASA Technical Standard; NASA-HDBK-7009B is a NASA Technical Handbook (guidance that explains the Standard, carries no independent "shall"). See `../force.md` for what each kind binds generally. |
| **Revision and status** | STD-7009B: Revision B, approved 2024-03-05, superseding Revision A w/Change 1. No expiration date in the document. HDBK-7009B: Revision B. The cover (p.1) reads "Approved: 2026-02-03"; the Document History Log (p.2) gives Revision B an approval date of 2025-09-24 — the two disagree. 174 of its 175 pages carry a running header reading "DRAFT: NASA-HDBK-7009B" (boilerplate; the cover page is what governs). It is listed ACTIVE on standards.nasa.gov dated 2026-02-03, Change 0 (unverified independently here — check standards.nasa.gov directly before citing to NASA). |
| **Where to get it** | standards.nasa.gov, search by number (NASA-STD-7009B / NASA-HDBK-7009B). Neither is a NODIS document; NODIS carries zero NASA Technical Standards and zero NIDs, so absence from the NODIS master list proves nothing about either document's status. Public copy, confirmed anonymously off-network on 2026-10-26: `https://standards.nasa.gov/sites/default/files/standards/NASA/B/1/NASA-STD-7009B-Final-3-5-2024.pdf` |
| **Applies to** | STD-7009B §1.2.1 (p.8): "generally applicable (relevant and appropriate) to all M&S used by NASA, its contractors, and its partners" and "highly recommended for M&S used to support critical decisions". It reaches a Federally Funded Research and Development Center (FFRDC) such as JPL "only to the extent specified or referenced in the applicable contracts, grants, or agreements" (§1.2, p.9 — the paragraph immediately after the §1.2.1 list; sometimes cited as §1.2.2). HDBK-7009B §1.2.1 (p.9 of 175): for "M&S practitioners, technical reviewers, decision makers, and others ... implementing, reviewing, using, or receiving the results from an M&S-based analysis." |

## What it is for, plainly
The Standard is NASA's method for deciding how much to trust the output of a model or simulation (M&S) when a program or project uses that output to make a decision. Instead of proving a model is correct from first principles, it asks the people responsible to report, on a fixed scale, how much evidence backs the result — where the inputs came from, how the model was checked against something real, and how uncertain the answer is — and to hand that report to the decision-maker. The Handbook is a companion that walks through how to do each step, including, as of Revision B, how to apply the same approach to a model built by machine learning.

## What it obliges (or advises)
- Document what the model is for, how critical the decision it feeds is, and who is responsible (§4.1.1, p.20; tagged `[M&S 40]`, `[M&S 6]`, `[M&S 41]`).
- Validate the model by "testing a model or simulation and comparing its responses or results to the system the M&S is representing or an acceptable alternative" (§4.2.5, p.29).
- Score the work on named credibility factors — five about how the model was built, six about this particular use — and report the scores to the decision-maker (§4.3.6.1 area, p.34).
- For the uncertainty-characterization factor, a Level 4 score requires "a statistical analysis (e.g., ANOVA) of the output uncertainty ... for all output quantities after rigorous and validated propagation of all known sources of uncertainty," with results that "may include statistical moments, confidence intervals, sensitivity analysis, etc." Level 3 explicitly allows a "comprehensive (e.g., Monte Carlo sampling) approach" (Table 17, Level Definitions for the M&S Uncertainty Characterization Factor; §E.4.4 narrative immediately above it).
- Of the Standard's 43 numbered requirements (tagged `[M&S n]`), none has a person or organization as the grammatical subject — the great majority bind a record, plan, or report, and two bind the M&S itself (our reading, from a tag-by-tag read of the requirement set; not a verbatim quote).
- HDBK-7009B §4.5.3 (p.36): the governing sentence for applying the Standard to a learned model — "the use of AI-generated models should be approached with a similar scope and intent as all M&S applications governed by the standard, considering the AI credibility and other risk factors" (note the modal is "should": this is guidance, not a standard requirement).

- Score the work on eleven separate factors, split across two groups: five "M&S capability" factors assessed during development — "M&S Data Pedigree, M&S Verification, M&S Validation, M&S Development Technical Review, and M&S Development Process/Product Management" (§E.3.1, p.61) — and six "M&S results" factors assessed during use — "M&S Use Assessment, M&S Input Pedigree, M&S Uncertainty Characterization, M&S Results Robustness, M&S Use/Analysis Technical Review, and M&S Use Process/Product Management" (§E.3.1, p.69).
- HDBK-7009B §4.5.3 (p.37) names four things to show about the training data behind a learned model, one of which cuts the opposite way from what intuition suggests: the training data being "too clean," leaving the AI model unable to address noisy real-world inputs (paraphrase, not verified verbatim at this exact wording).

## Where it stops
- §1.2.1 (p.8): "Any required application of this Standard is to be specified in program/project/organization/office directives and may be tailored" — the Standard does not invoke itself onto any program.
- §4.3.6 (p.34): "This Standard levies no requirements with respect to what levels to achieve (the sufficiency threshold levels), merely that the levels be determined and reported." Whether a reported level is good enough is the decision-maker's call, not the Standard's.
- The Standard forbids rolling its factors into one score: "Given that the factors are largely independent, comparison between or combining of factor assessments and thresholds is not intended and should be avoided in all labeling approaches" (§E.2, p.63; page not re-verified against every extraction's pagination — see Trap below).
- HDBK-7009B §4.5.3 (p.36): where an AI application is "not associated with predicting the RWS [real-world system] response," the Standard's processes "may have less applicability" — named cases include "generative AI (genAI) chatbots, and image, video, and audio generation systems, voice transcribers and notetakers" (p.37, continuation of the same discussion).

## AI and machine-learning touchpoints
- The word "AI" never appears in NASA-STD-7009B itself — the AI link is entirely carried by the companion Handbook (our reading from a full-text search of the Standard).
- HDBK-7009B §4.5.3 (p.36) names three places AI can sit in the M&S lifecycle: "AI can be the M&S, AI can produce inputs into the M&S, or AI can automate an M&S activity in the lifecycle."
- HDBK-7009B §4.5.3 (p.37) concedes the model may be unexaminable: "it may not be possible to examine the AI model in detail, or the training dataset that the model depends on. Even 'open' AI models are often only open weights... This may make evaluating the AI model difficult or impossible." (our reading: this is NASA's own guidance conceding the limit, not a requirement that resolves it.)
- A surrogate model's referent can itself be another, more expensive model rather than measured data: "In some instances, e.g., for the development of so-called 'surrogate models,' the referent can be the results obtained from a higher-fidelity (and typically computationally expensive) model" (validation discussion, p.65).
- The vocabulary gap is real: "black box" and "emergent" return zero hits across the Standard's full text (our count) — the concept the Standard is reaching for when it discusses an unexaminable model is there in the Handbook's §4.5.3 (above), but the Standard's own vocabulary has no name for it.

## How it connects to other documents
- NASA-STD-7009B and NASA-HDBK-7009B assert an identical 43-tag requirement set (by our set comparison); the Handbook adds no containment the Standard does not already carry — it explains, the Standard imposes.
- NPR 7120.5F has zero hits for "7009" or "models and simulations" in its own text (text search of its body); NPR 7150.2D and NPR 7123.1D mention 7009 only in reference appendices. So nothing in the programmatic or systems-engineering NPRs invokes this Standard automatically — invocation has to happen in a program, project, or contract document.
- §1.3 (p.9 area) ties tailoring to NPR 7120.5: "Tailoring of the requirements in this Standard ... is acceptable when formally approved by the delegated NASA Technical Authority in accordance with NPR 7120.5."
- The Standard's predecessor Handbook, NASA-HDBK-7009 (2013, superseded), has no section addressing AI at all; Revision B of the Handbook added §4.5.2–4.5.3 specifically for it.
- The Standard shares a historical root with NPR 7120.5F's Technical Authority structure: "This Standard was originally developed to respond to Action 4 from the 2004 report 'A Renewed Commitment to Excellence,' with consideration also given to related findings identified in the Columbia Accident Investigation Board (CAIB) Report" (Foreword, p.3) — the same CAIB finding that produced the Technical Authority and Formal Dissent process described on the NPR 7120.5F page.

## Traps
- **Pagination disagreement between extractions.** One reading, checked by hand against the PDF viewer, placed §E.4.4 at PDF page 76 and Table 17 at PDF page 77 (and separately found the document's own "List of Tables" index three pages wrong for 19 of 20 tables). A second text extraction's page markers used for the Table 17 / Monte Carlo quote above instead land that same content at pages 74–75. The two have not been reconciled here — hand-check the page number against your own PDF viewer before citing Table 17 or §E.4.4.
- The Standard is easy to read as mandatory because it is thorough and detailed; §1.2.1's "generally applicable" and "highly recommended" language is advisory until a directive or contract names it.
- "DRAFT" running headers on 174 of 175 pages of the Handbook are a stale posting artifact, not a status — the cover page and the standards.nasa.gov listing govern.
- Do not treat the Handbook's §4.5.3 concession as resolving the question of AI applicability — it both extends the Standard's approach to AI *and* names cases (generative AI, chatbots, in NASA's own wording) where that approach "may have less applicability." Both halves of that sentence matter.

## Verified quotes
> "Any required application of this Standard is to be specified in program/project/organization/ office directives and may be tailored (refer to section 1.3 in this Standard for tailoring requirements)."
— NASA-STD-7009B, §1.2.1, p.8

> "This language applies to the Jet Propulsion Laboratory (a Federally Funded Research and Development Center), other contractors, recipients of grants, cooperative agreements, or other agreements only to the extent specified or referenced in the applicable contracts, grants, or agreements."
— NASA-STD-7009B, §1.2 (paragraph after the §1.2.1 list), p.9

> "This Standard levies no requirements with respect to what levels to achieve (the sufficiency threshold levels), merely that the levels be determined and reported."
— NASA-STD-7009B, §4.3.6, p.34

> "the use of AI-generated models should be approached with a similar scope and intent as all M&S applications governed by the standard, considering the AI credibility and other risk factors."
— NASA-HDBK-7009B, §4.5.3, p.36

> "When the AI application in an M&S lifecycle is not associated with predicting the RWS response, the processes in the standard may have less applicability. Such cases may include AI applications, like generative AI (genAI) chatbots, and image, video, and audio generation systems, voice transcribers and notetakers (except in cases where the detailed accuracy of the notes is critical, e.g., during verification/validation testing)."
— NASA-HDBK-7009B, §4.5.3, pp.36–37

> "Artificial Intelligence: (1) Any artificial system that performs tasks under varying and unpredictable circumstances without significant human oversight, or that can learn from experience and improve performance when exposed to data sets. ... Note: NASA follows definitions defined in Section 238(g) of the National Defense Authorization Act of 2019."
— NASA-HDBK-7009B, §3.2 (Definitions), p.19

> "[M&S 15] The M&S shall be verified. [M&S 16] A record of the domain of verification of the verified M&S shall be maintained."
— NASA-STD-7009B, §4.2.3, p.28 (two of the 43 numbered requirements; both bind the M&S or a record of it, not a person)

> "When computational or empirical surrogate models are based on ML approaches, they may be considered a sub-set of artificial intelligence (AI) models with respect to M&S use and results credibility. Although a sub-set of AI ... the ML surrogates used for (M&S supported) critical decisions are subject to the same M&S credibility evaluation and risk evaluations as other non-AI M&S approaches."
— NASA-HDBK-7009B, §4.5.2 (Note), p.36
