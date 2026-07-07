# Track: System Design (weeks 7–20, ×3 cycles)

Hari's diagnosed failure: **not asking the right questions.** SD1 is therefore the core module and gets re-drilled every cycle — the first 10 minutes of every design mock are the primary grade.

| # | Module | Tier | Objectives |
|---|---|---|---|
| SD1 | The method: the first 5 minutes | 1 | Requirements → users/scale → constraints → success criteria BEFORE any boxes. A drilled question checklist: who uses it, how many, read/write ratio, latency tolerance, consistency needs, what's explicitly out of scope. Then: API → data model → high-level design → deep-dive → bottlenecks. |
| SD2 | Core vocabulary | 2/3 | Load balancing, caching layers + invalidation, CDNs, queues + backpressure, sharding/partitioning, replication, CAP in plain words. Bar: use each term correctly in a sentence with a trade-off attached. |
| SD3 | Product-scale backend designs | 1 | Full walkthroughs: notification system, news feed, chat, file upload, rate limiter, URL shortener. One per cycle, done as a mock first, then studied. |
| SD4 | Frontend system design | 1 | The product-engineer differentiator: state architecture, data fetching/caching (SWR patterns), real-time (polling/SSE/WebSocket trade-offs), optimistic UI, performance budgets, bundle strategy. Designs: autocomplete, live dashboard, infinite feed UI, collaborative editor (shallow). |
| SD5 | AI-feature design | 1 | Designing systems WITH LLM components: streaming UX, latency/cost budgets, fallbacks and degradation, eval/feedback loops, prompt+context management as a system concern. Bridges to [ai-agents](../ai-agents/00-index.md) and the portfolio project. |

**Drill format:** every SD session opens with a 10-minute "first 5 minutes" rep on a fresh prompt — questions only, no design — graded before anything else happens.
