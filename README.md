# NASA-Guidance-Docs

A Claude skill that answers the questions people get wrong about NASA's governance documents: who owns this document, is it binding or only guidance, is it still in force, where does it stop, and how does it reach a flight system that contains AI or machine learning. It is written for engineers, assurance staff and proposal writers who need to cite NASA requirements correctly, and for the agents that help them.

Load it in Claude Code and it fires when a task cites NPR 7150.2, NASA-STD-8739.8, NPR 7123.1, a NID or similar, or asks "is this binding" or "which office owns this". It is plain markdown, so a person can read it without Claude.

## What is different about it

**Force before content.** Most wrong answers about NASA requirements confuse a document's type with its authority. The skill leads with ten traps (`skills/nasa-guidance-docs/SKILL.md`), for example: a handbook is guidance even when it copies an NPR `shall` word for word; a requirement's force can live in the stem of a list, so filtering on `shall` loses items; and a definition can be borrowed from a document that has since been cancelled.

**Status conflicts are recorded, not resolved.** Where NASA's own registers disagree (a cover page says expired, the directives register says extended), the page records both and says which register to check. Examples are in worked pattern 6 of `SKILL.md`.

**A map of where the evidence stops.** `skills/nasa-guidance-docs/references/ai_crosswalk.md` walks the software-class and safety-criticality ladder rung by rung and marks where the gates transfer to an AI-enabled system and where the evidence methods (code coverage, cyclomatic complexity) stop saying anything about learned behaviour. All interpretation is labelled "(our reading)".

**Every claim has a locator.** Document, clause or SWE tag, and page. Quotes were checked against the extracted text of the source PDFs. The skill never says "NASA covers X" or "NASA has a gap in X"; it says what a clause says and whose call the determination is.

**Outside frameworks are kept apart.** EASA, FAA, NIST, DoD, ASTM, RTCA, ISO and OMB pages carry a banner: comparison only, never evidence of NASA coverage.

## Quick start

Clone and link the skill into Claude Code:

    git clone https://github.com/Lmandrake/NASA-Guidance-Docs.git
    ln -s "$PWD/NASA-Guidance-Docs/skills/nasa-guidance-docs" ~/.claude/skills/nasa-guidance-docs

Then ask, for instance, "Which NASA requirements bind software on a Class B lander, and does 100% MC/DC apply to a neural network? Give clause numbers." Four such prompts with expected behaviour are in `skills/nasa-guidance-docs/evals/evals.json`.

Without Claude, start at `skills/nasa-guidance-docs/SKILL.md`, then use `skills/nasa-guidance-docs/references/INDEX.md` to find a document page.

## Map of the repo

| Path | What it holds |
|---|---|
| `skills/nasa-guidance-docs/SKILL.md` | Navigation, the ten traps, eight worked methods |
| `skills/nasa-guidance-docs/references/force.md` | What each document type binds and how to check status in each register |
| `skills/nasa-guidance-docs/references/offices.md` | The offices behind the documents and how they hand off |
| `skills/nasa-guidance-docs/references/ai_crosswalk.md` | How the documents reach an AI-enabled flight system |
| `skills/nasa-guidance-docs/references/documents/` | One page per NASA document (about 80) |
| `skills/nasa-guidance-docs/references/external/` | Outside frameworks and papers (about 48) |
| `skills/nasa-guidance-docs/references/INDEX.md` | Generated list of every page with its owner |
| `skills/nasa-guidance-docs/evals/evals.json` | Four eval prompts with expected outputs |
| `scripts/build_index.py` | Rebuilds `INDEX.md`: `python3 scripts/build_index.py` |
| `docs/DESIGN.md` | Why this is a skill, content rules, provenance |

About twenty headline documents (NPR 7150.2D, the Software Engineering Handbook, NASA-STD-8739.8B, NASA-STD-7009B, NPR 7123.1D, NPR 7120.5F and others) get a full page; every other document gets a short one.

## Status and limits

- It summarises public documents only. A document that is not publicly readable has no page, and paywalled standards get a citation and a pointer, nothing more.
- It covers software, safety and mission assurance for flight systems, not every NASA directive.
- The NASA document, not this repo, is the authority. Check the current revision and the clause before relying on anything here.
- Page numbers can differ by one between printed and PDF numbering; several pages flag the offset.
- The eval prompts have not been run, and the skill description has not been tuned against trigger tests (`docs/DESIGN.md`, "Open").
- Pages record the revision they were written against and will lag when NASA reissues a document.

## Credit

Please credit me if you find this work useful. Released under the MIT licence.
