# Track: Foundations (weeks 1–6)

Order matters — each module assumes the previous. Exercises accumulate in `exercises/`.

| # | Module | Tier | Objectives | How interviewers probe it |
|---|---|---|---|---|
| F1 | JS execution model | 1 | Call stack, event loop, microtasks vs macrotasks, `fetch`→`.then` timing, rendering interaction | "What logs and why?" ordering puzzles; "explain the event loop" cold |
| F2 | Closures, scope, `this`, prototypes | 1 | Lexical scope, closure lifetimes/memory, `this` binding rules, prototype chain vs `class` sugar | Loop-variable capture traps; "how does inheritance actually work?" |
| F3 | Async patterns | 1 | Promise internals, async/await desugaring, error propagation, `Promise.all/allSettled/race`, concurrency limits, cancellation | "Fetch 100 URLs, max 5 at a time"; async error-handling holes |
| F4 | TypeScript type system — **TEST-OUT week 1** | 1 | Structural typing, generics + constraints, narrowing/guards, discriminated unions, utility types, `unknown` vs `any` | "Type this function"; API-response modeling; when TS can't save you |
| F5 | HTML semantics + a11y | 2 | Semantic elements, forms, ARIA basics, keyboard nav, why a11y = senior signal | "Make this widget accessible"; div-soup critique |
| F6 | CSS layout | 2 | Flexbox, grid, cascade/specificity, positioning, responsive units, common layout bugs | "Center this / build this layout" live; specificity puzzles |
| F7 | DSA I + Big-O | 2 | Arrays, strings, hash maps, sets, two pointers, sliding window; time/space analysis said aloud fluently | LC-easy/medium in TS; "what's the complexity?" unprompted is the bar |
| F8 | DSA II | 2 | Stacks, queues, linked lists, trees, BFS/DFS, recursion patterns | LC-medium traversals; "iterative vs recursive trade-off?" |
| F9 | SQL | 2 | Modeling/normalization, joins, aggregation, indexes (why/when/cost), transactions + isolation basics, N+1 | "Design the schema for X"; "this query is slow — why?" |
| F10 | NoSQL + trade-offs | 3 | Document/KV/wide-column/graph families; when SQL vs NoSQL; consistency trade-offs at conversation level | "Would you use Mongo or Postgres for X, and why?" |
| F11 | Build tooling & bundlers | 2 | Vite/esbuild/webpack mental model, code splitting, tree shaking, lazy loading, source maps | "This bundle is 4MB — cut it in half"; "what does the bundler actually do?" |
| F12 | Web platform APIs | 2/3 | Tier 2: service workers + caching strategies, web/worker threading, WebSocket protocol layer (transport trade-offs live in SD4). Tier 3: web components/shadow DOM, view transitions — when-to-use only | "How would you make this work offline?"; "when would you use web components over React?" |

**F4 test-out rule:** the bar stays Tier 1 (interviews set tiers, not comfort), but Hari claims existing mastery — so week 1 includes a 30-min interview-grade spoken assessment with 3-level follow-ups. Pass → F4 becomes review-only and its ~5 hrs fund F11/F12. Fail → full module stays.

**Exit gate (week 6, +1 week buffer if F4 test-out fails):** diagnostic mock battery — one coding, one design, one behavioral round. Results reorder Phase B.
