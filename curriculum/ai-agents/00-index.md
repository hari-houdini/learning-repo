# Track: AI & Agents (weeks 5–20)

The differentiator track. Every module pairs theory with a commit to the [portfolio project](../../project/) — no module is "learned" until something in the project uses it. Primary sources: Anthropic's *Building Effective Agents* essay and Claude Docs (see [RESOURCES.md](../../RESOURCES.md)).

**Baseline (2026-07-07 diagnostic, corrected same day):** zero built — the food-expiry app (Gemini Vision + RAG over government food-safety sources) exists as a self-authored DESIGN only, not code. A1/A2 are NOT compressible; A7 stays a full module. The design's existence is still a genuine positive — it shows product-thinking and gives the A-track a concrete target from day one. Vocabulary also needs formalizing (he described products as "stateful models").

| # | Module | Tier | Objectives | Project pairing |
|---|---|---|---|---|
| A1 | LLMs, practically | 1 | Tokens, context windows, temperature/sampling, prompting patterns, why models hallucinate, model selection & cost | Choose model + budget for the project |
| A2 | LLM APIs from TypeScript | 1 | Messages API, streaming, structured output (JSON/tool-shaped), retries & error handling, prompt caching | First working API call; streaming CLI |
| A3 | Tool use | 1 | Function calling: schemas, the tool loop, parallel calls, tool design principles (few, well-described, forgiving) | First tool: fetch + parse a job posting |
| A4 | Single agent | 1 | The agent loop (LLM + tools + memory in a loop), context management, stopping conditions, failure modes | Company-research agent working end-to-end |
| A5 | Multi-agent orchestration | 1 | Orchestrator-workers, handoffs, shared vs isolated context, when multi-agent is WORSE (usually), workflow-vs-agent decision | Add CV-tailoring + interview-prep agents under an orchestrator |
| A6 | Evals | 1 | Why evals separate professionals from tutorial-followers: golden sets, LLM-as-judge (and its traps), regression harness in CI | Eval harness grading research-agent output quality |
| A7 | RAG + embeddings | 2 | Embeddings, chunking, retrieval quality, when RAG vs long context vs fine-tuning | Optional: index his own story bank / CV corpus |
| A8 | Production concerns | 2 | Cost + latency budgets, observability/tracing, guardrails, prompt injection basics, graceful degradation | Hardening pass before the week-20 demo |

**Interview payoff:** after A5+A6, "have you used multi-agent AI?" gets answered with a demo, an architecture diagram, and opinions ("multi-agent was only worth it for X because Y — for Z a single agent with better tools beat it"). That last clause is what standout sounds like.
