# Design: a reusable skill for NASA governance documents

**Decision: build it.** Knowledge about NASA's governance documents (who owns each,
how binding it is, where the live copy is, what it reaches and where it stops) is needed by
any proposal, review, mission or AI-assurance task, so it should live in one place that any session
can load and anyone can read.

**Why a skill and not a document.** The value is in being loaded at the moment someone is about to
cite a requirement, ask whether a document is in force, or route a question to an office. A skill
description fires on those moments; a document in a repo is read only by someone who already knows
it exists.

**Layout.** `skills/nasa-guidance-docs/SKILL.md` stays short: navigation and the nine traps that
cause most wrong answers. Detail is in `references/`, read on demand:
- `force.md` — what each document type binds, and how to check status per register.
- `documents/<DOC>.md` — one page per NASA document. About twenty headline documents get the full
  template (owner, force, status, where to get it, obligations, where it stops, AI touchpoints,
  connections, traps, verified quotes); every other document mapped gets a short page.
- `external/<NAME>.md` — outside frameworks (EASA, FAA, NIST, DoD, ASTM, RTCA, ISO, OWASP, CISA,
  OMB and executive orders). Each carries a banner: comparison only, never NASA coverage.
- `INDEX.md` — generated list of every page with its owner (`scripts/build_index.py`).
- `offices.md` — the offices and how they hand off.
- `ai_crosswalk.md` — how the documents reach an AI-enabled flight system, and where their
  evidence methods stop transferring.

**Content rules.** This repo holds only public NASA governance facts
and our analysis of them: no contract text, no team working material, no internal mail, no
colleague names. Every claim carries a locator; quotes were checked against the source PDFs'
extracted text; our interpretations are marked "(our reading)". Documents that are not
publicly readable (login-gated or institution-internal) get no page; paywalled standards get a
citation and a one-line pointer only.

**Worked patterns.** SKILL.md lists eight example methods for using this material (reason-survival
sweep, per-risk document reach, consequence tiers, independence that a shared model defeats, office
hand-offs, status checks, handbook force, policy quality), so a reader learns the method, not just
the facts.

**What it does not do.** It makes no determination that NASA covers or fails to cover anything.
It is not the citation authority: the NASA document is. It does not track every NASA directive;
it covers about eighty NASA documents and thirty outside ones,
with depth concentrated on software, safety and mission assurance for flight systems.

**Provenance.** This map began as research for a NASA assurance study; it summarises only public
documents and is independent work. Page text and
quotes were checked against the extracted text of the source PDFs. An anonymous check from outside any
network confirmed which documents a member of the public can read; only those carry content here. Pages were drafted in parallel by several
agents; the quotes each one reports were grep-checked against that text, but page numbers can differ
by one between printed and PDF numbering, and several pages flag such offsets rather than resolve
them.

**Open.** Eval prompts are in `skills/nasa-guidance-docs/evals/evals.json` but have not been run.
The description has not been tuned against trigger tests.
