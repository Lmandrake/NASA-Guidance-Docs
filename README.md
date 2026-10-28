# NASA-Guidance-Docs

A Claude skill, `nasa-guidance-docs`, that maps NASA's software, safety and mission-assurance
governance documents for flight systems: who owns each one, how binding it is, where to get the
current copy, what it obliges and where it stops, and how it reaches systems with an AI or
machine-learning component. Also covers the offices behind the documents (OCE, OSMA, OCIO, Chief
Data Officer, Chief AI Officer, IV&V, the Technical Authorities) and how they hand off, and outside
frameworks (EASA, FAA, NIST, DoD, ASTM, RTCA, ISO, OMB) for comparison.

- Skill: `skills/nasa-guidance-docs/SKILL.md`
- Page index: `skills/nasa-guidance-docs/references/INDEX.md` (rebuild with `python3 scripts/build_index.py`)
- Design and content rules: `docs/DESIGN.md`

This map began as research for a NASA assurance study; it summarises only public documents and is independent work.

Everything here is drawn from public NASA documents, with a locator on every claim. Interpretations
are marked as ours. The NASA document, not this repo, is the authority; check the current revision
before relying on anything here.

Install for Claude Code: symlink `~/.claude/skills/nasa-guidance-docs` to
`skills/nasa-guidance-docs` in this repo.

## Credit

Please credit me if you find this work useful.
