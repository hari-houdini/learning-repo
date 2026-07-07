# Portfolio Project — Agentic App in TypeScript

The ONE project (see [MISSION.md](../MISSION.md) — one, not three). Purpose: turn "have you used multi-agent AI?" from a fatal question into a demo + architecture story + trade-off opinions.

## Candidate concept (confirm at week-3 kickoff)

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
