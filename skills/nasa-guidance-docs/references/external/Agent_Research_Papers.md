# Agent and LLM research papers — background only

> Background reading on agentic-AI research, not a standard, regulation, or NASA/JPL document. These carry no assurance obligations and must not be cited as NASA or external-standard coverage.

- **ReAct** (Yao et al., Princeton/Google, 2022) — introduces interleaving chain-of-thought reasoning with action generation in a large language model (LLM); the "reason + act" prompting pattern underlying many later agent architectures.
- **Toolformer** (Schick et al., Meta AI Research, 2023) — a model that teaches itself which external tools (APIs) to call, when, and with what arguments, via self-supervision rather than hand-written rules.
- **AutoGen** (Wu et al., Microsoft Research and others) — an open-source framework for building applications out of multiple conversable LLM-, tool-, and human-based agents talking to each other.
- **Generative Agents** (Park et al., Stanford/Google, 2023) — the "Smallville" paper: 25 simulated agents with memory, reflection, and planning producing believable human-like behavior in a sandbox town.
- **Reflexion** (Shinn et al., Northeastern/Princeton/MIT, 2023) — agents that improve through verbal self-reflection on their own failures, rather than through weight updates (no retraining).
- **Multi-agent risks report** (Cooperative AI Foundation, with Oxford, DeepMind, Anthropic and others; 95pp) — catalogues failure modes — miscoordination, conflict, collusion — that arise specifically from *systems of multiple* interacting AI agents, not single-model risk. (Our reading: the one source here squarely about multi-agent risk rather than single-model risk.) (own page: `CooperativeAI_2025_Multi-Agent_Risks.md`)
- **METR Frontier Risk Report** (Model Evaluation and Threat Research; assessment window Feb 16–Mar 16, 2026, published May 19, 2026) — pilot third-party assessment, with Anthropic, Google, Meta, and OpenAI participating, of whether internal AI agents had the means, motive, and opportunity to start an unauthorized ("rogue") autonomous deployment. (Our reading: concluded plausible means/motive/opportunity for small-scale rogue deployment, but not yet for a highly robust one.) (own page: `METR_2026_Frontier_Risk_Report.md`)
- **LangChain, "The Fundamentals of Agent Observability"** — a vendor/practitioner guide, not peer-reviewed research, on why monitoring non-deterministic agent behavior (via runs, traces, threads) differs from traditional deterministic-software observability and testing.

These inform risk-candidate framing generally; none maps to a specific NASA/JPL document.
