# Portfolio Project — Agentic App in TypeScript

The ONE project (see [MISSION.md](../MISSION.md) — one, not three). Purpose: turn "have you used multi-agent AI?" from a fatal question into a demo + architecture story + trade-off opinions.

## Candidate concepts (decide at week-3 kickoff)

### Candidate B (added after baseline diagnostic): build the food-expiry app
Hari has a self-authored DESIGN (no code yet): Gemini/vision model extracts product/date from photos + RAG over government food-safety sources → expiry estimate; agents + evals to be added on top. Pros: his own idea (motivation + authorship — "I designed it, then built it end-to-end" is a strong arc), naturally covers multimodal + RAG (A7) alongside tools/agents/evals. Cons: no head start — greenfield like Candidate A; and the domain is less obviously "agentic" — must avoid agents-for-agents'-sake (though "I evaluated and multi-agent WASN'T worth it here" is itself a strong answer if backed by evals).

### Candidate A: multi-agent job-search assistant
**Multi-agent job-search assistant** — dogfooded weekly on the real search:
- **Research agent** — given a company/posting: gathers facts, recent news, tech stack, sponsorship signals
- **CV-tailoring agent** — maps the story bank + CV against a posting; proposes targeted bullet edits
- **Interview-prep agent** — generates likely questions for the specific role + drills from the story bank
- **Orchestrator** — routes, shares context deliberately, and knows when NOT to fan out
- **Eval harness** — golden set of postings; grades research accuracy and tailoring quality; runs on CI

Why this concept: it's demo-able in interviews, produces weekly real value (funnel!), and every architecture decision becomes a first-person interview answer.

## Non-negotiable requirements (these ARE the interview material)

1. TypeScript end-to-end; Claude API (direct or Agent SDK — decide at kickoff, document why)
2. Tool use with well-designed schemas (module A3 standards)
3. Explicit memory/context-management strategy — written down as a short ADR
4. Multi-agent only where measurably better than single-agent — the comparison itself is a headline interview story
5. **Evals from week one of the build** — even 10 golden cases; expand as it grows
6. A `docs/decisions/` folder of mini-ADRs: every trade-off recorded = every interview answer pre-written

## Build order (tracks modules A2→A6)

1. Streaming API call from TS (A2) → 2. one tool: fetch+parse a posting (A3) → 3. research agent loop (A4) → 4. eval harness v1 (A6, early on purpose) → 5. remaining agents + orchestrator (A5) → 6. hardening pass (A8) → week-20 demo.
