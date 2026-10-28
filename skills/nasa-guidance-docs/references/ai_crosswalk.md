# How NASA's documents reach a flight system with an AI component

**What this is.** A walk through the path by which existing NASA requirements reach a flight system
that contains an AI or machine-learning component, and the point at which the *evidence methods*
those requirements name stop telling you anything about a learned component. Page numbers are PDF
pages of the source as extracted. Everything labelled "(our reading)" is interpretation, not NASA's.

**What it is not.** A determination that NASA covers or fails to cover AI. That call belongs to a
project's Technical Authorities and systems engineers.

## 1. The short version (our reading)

The *gates* transfer: NASA's existing classification and safety-criticality ladder is written about
systems and consequences, not about how the software was made, so it reaches an AI-enabled function
with no edit. The *evidence* does not fully transfer: the measures demanded at the top rungs (code
coverage, cyclomatic complexity, line-level design disclosure) measure code paths, and say little
about how a learned component behaves on inputs nobody tested.

## 2. The ladder, rung by rung

| Step | Clause | What it says | Reaches AI? (our reading) |
|---|---|---|---|
| Is this software? | NPR 7150.2D Appendix A, definition of software (p.50) | Includes auto-generated code and software NASA did not write (COTS, open source, reused, legacy) | Yes. A learned model executing on board is software in a system; nothing in the definition depends on how it was produced. |
| What class? | NPR 7150.2D §3.5, **SWE-020** (p.24), Appendix D | "The project manager shall classify each system and subsystem containing software in accordance with the highest applicable software classification definitions for Classes A, B, C, D, E, and F" | Yes. Classes are by consequence and use. Appendix D (p.69): "Class E software cannot be safety-critical software." A research prototype flown for an in-flight test should be upgraded to its operational class (Appendix D, Class E, p.69). |
| Is it safety-critical? | NPR 7150.2D Appendix A (p.49), definition, "(Source NPR 8715.3)"; **SWE-205** (§3.7, p.26) | "Safety Critical. A term describing any condition, event, operation, process, equipment, or system that could cause or lead to severe injury, major damage, or mission failure if performed or built improperly, or allowed to remain uncorrected." SWE-205: "The project manager, in conjunction with the SMA organization, shall determine if each software component is considered to be safety-critical per the criteria defined in NASA-STD-8739.8." | Yes. Written for "any condition, event, operation, process, equipment, or system". The criteria themselves are in NASA-STD-8739.8B; see that page. The definition is borrowed from NPR 8715.3; see `documents/NPR_8715.3.md` for what survives in the live revision. |
| What do safety-critical components get? | **SWE-023** (p.26) | Implement "the safety-critical software requirements contained in NASA-STD-8739.8" | Yes, as a gate. |
| | **SWE-134** (p.26) | For safety-critical or mission-critical software: known safe state at start and restart, safe transitions, operator overrides need "at least two independent actions by an operator", out-of-sequence command rejection, input/output integrity checks, "No single software event or action is allowed to initiate an identified hazard", timely off-nominal response, "The software can place the system into a safe state." | Mostly yes, and these are the strongest transfers: they are behaviour properties checkable around a component without reading its internals (our reading). |
| | **SWE-219** (p.27) | 100 percent code test coverage using Modified Condition/Decision Coverage (MC/DC) for safety-critical components | The rung applies; the measure says little. MC/DC over the code that runs a network says nothing about which weights decide an output (our reading). The Software Engineering Handbook's own retrofit (topic 7.25 §7.2) asks that "each node in a neural network must be shown to affect the solution and all paths evaluated", and topic 7.25 §5.1 says "there is not a provable means to evaluate the AI/ML system and show that they meet the safety requirements". Both are handbook guidance, not NPR text. |
| | **SWE-220** (p.27) | Cyclomatic complexity of 15 or lower for safety-critical components, exceedances "reviewed and waived with rationale" | Same as SWE-219: the rung applies; the metric measures branching in code, not learned behaviour (our reading). |
| Independent check? | **SWE-141** (p.25) | IV&V for Category 1 projects, Category 2 projects with Class A or B payload risk classification per NPR 8705.4, and projects the Mission Directorate selects | Yes, as a gate; the IV&V plan follows NASA-STD-8739.8 (SWE-131). Clauses aimed at the IV&V provider bind only where IV&V is assigned. |
| Tool-made code | **SWE-146** (§3.8.1, p.27), **SWE-206** (p.27–28) | Define the approach to auto-generated code, items (a)–(g); give NASA electronic access to "the models, simulations, and associated data used as inputs for auto-generation of software" | SWE-146 transfers: it obliges a plan, and its equal-standard clause attaches to the generated **code** in item (d), not to the generator. SWE-206's stated reason (reproducing generated code later) does not obviously hold for a trained generator: the inputs that decide the output are the model version, weights, instructions and sampling settings, which its closed list does not name (our reading). |

## 3. Verification does not require reading the internals

- NPR 7123.1D Appendix A: verification may be by test, analysis, demonstration, inspection, or a
  combination (see `documents/NPR_7123.1D.md` for the locator).
- NPR 7150.2D SWE-027 and SWE-211: off-the-shelf, open-source and reused components are verified and
  validated "to the same level required to accept a similar developed software component". That is
  a parity-of-outcome standard, black-box by construction (our reading).
- NASA-STD-7009B is the closest NASA method for a model you cannot verify from first principles:
  validation against a referent (§4.2.5), credibility levels including statistical evidence
  (Table 17), and "report your level" rather than a threshold (§4.3.6). It does not invoke itself
  (§1.2.1). See `documents/NASA-STD-7009B.md`.
- The handbook pulls the other way for safety-critical AI (topic 7.25, above). NASA's own material
  disagrees with itself here; carry both, and let the Technical Authority resolve it.

## 4. One test that sorts most cases (our reading)

Ask whether a check exists that is **cheaper than the function and runs on every one of its
outputs**. Where it does, an AI component is a harder instance of a problem NASA already handles: the
SWE-134 behaviours (safe state, independent override, integrity checks, no single event initiating a
hazard) are applied around it. Flown precedent: the AEGIS autonomous targeting software on the Mars
Science Laboratory rover checked properties of each chosen target at run time rather than verifying
how targets were picked (Francis et al., *Science Robotics* 2(7), 2017). Where no such check exists,
the existing evidence methods give little assurance and the question is genuinely new.

## 5. What a sweep of NASA's own stated reasons found (our analysis)

The Software Engineering Handbook publishes a Rationale for each NPR 7150.2D requirement. Method: read
NASA's own stated reason for each requirement, ask whether that reason still works when a machine does
the work, and follow with an adversarial re-read that tries to withdraw each flag. Figures removed
until the study's results are published (the study is active and ongoing). Any such result is our
analysis of NASA's text, not a NASA position.

## 6. Where AI is named at all

- **Requirements:** none of the documents mapped here contains an AI-specific requirement. NPR 7150.2D
  never uses "artificial intelligence", "machine learning", "autonomy" or "neural" (zero counts over
  the whole text).
- **Guidance:** Software Engineering Handbook topics 7.25 and 8.25; NASA Risk Management Handbook
  Part 1 §3.2.4 (names AI/ML as a source of uncertain risk and defers to NIST); NASA-HDBK-7009B §4.5.3
  (generative chatbots are a case where the M&S standard "may have less applicability").
- **Directive, not flight software:** NID 1383.155 governs generated media.
- **Already actor-neutral:** NPR 2810.1F's Least Privilege definition is about a "user or component";
  NID 2800.149 defines data access for "a human or Non-Person Entity (NPE)". So account and access
  rules may already reach a software agent as written (our reading; OCIO's call).
- **When nothing fits:** NPD 8700.1F §1(b)(4) p.2 already prescribes the response to a hazard with no
  accepted standard: "consulting with subject matter experts on strategies to ensure an acceptable
  level of risk."

## 7. Where outside text is stronger (comparison, not coverage)

A per-risk comparison asks, for each item on a list of AI risks, whether an outside document's text
is stronger than NASA's binding text, and again counting NASA guidance as well. Figures removed until the study's
results are published (the study is active and ongoing). These are findings about where NASA's own documents stop, never evidence that NASA requires what the outside
text says. Two outside points worth knowing:

- EASA's Concept Paper Issue 02 states that its learning-assurance objectives "fully apply to
  surrogate ML models", so a learned surrogate with no language model involved still gets the full
  set (see `external/EASA_AI_Concept_Paper_Issue02.md` for the page-number caveat).
- The FAA's AI safety roadmap names the three Overarching Properties (intent, correctness,
  innocuity) without defining them; the definitional source is NASA-TM-2019-220292 p.10, Figure 1
  (see `external/NASA-TM-2019-220292_Overarching_Properties.md`).

Pages for these and the other outside frameworks are in `external/`; `INDEX.md` lists them.
