# Track: Foundations (weeks 1–6)

Order matters — each module assumes the previous. Exercises accumulate in `exercises/`.

| # | Module | Tier | Objectives | How interviewers probe it |
|---|---|---|---|---|
| F1 | JS execution model | 1 | Call stack, event loop, microtasks vs macrotasks, `fetch`→`.then` timing, rendering interaction | "What logs and why?" ordering puzzles; "explain the event loop" cold |
| F2 | Closures, scope, `this`, prototypes | 1 | Lexical scope, closure lifetimes/memory, `this` binding rules, prototype chain vs `class` sugar | Loop-variable capture traps; "how does inheritance actually work?" |
| F3 | Async patterns | 1 | Promise internals, async/await desugaring, error propagation, `Promise.all/allSettled/race`, concurrency limits, cancellation | "Fetch 100 URLs, max 5 at a time"; async error-handling holes |
| F4 | TypeScript type system | 1 | Structural typing, generics + constraints, narrowing/guards, discriminated unions, utility types, `unknown` vs `any` | "Type this function"; API-response modeling; when TS can't save you |
| F5 | HTML semantics + a11y | 2 | Semantic elements, forms, ARIA basics, keyboard nav, why a11y = senior signal | "Make this widget accessible"; div-soup critique |
| F6 | CSS layout | 2 | Flexbox, grid, cascade/specificity, positioning, responsive units, common layout bugs | "Center this / build this layout" live; specificity puzzles |
| F7 | DSA I + Big-O | 2 | Arrays, strings, hash maps, sets, two pointers, sliding window; time/space analysis said aloud fluently | LC-easy/medium in TS; "what's the complexity?" unprompted is the bar |
| F8 | DSA II | 2 | Stacks, queues, linked lists, trees, BFS/DFS, recursion patterns | LC-medium traversals; "iterative vs recursive trade-off?" |
| F9 | SQL | 2 | Modeling/normalization, joins, aggregation, indexes (why/when/cost), transactions + isolation basics, N+1 | "Design the schema for X"; "this query is slow — why?" |
| F10 | NoSQL + trade-offs | 3 | Document/KV/wide-column/graph families; when SQL vs NoSQL; consistency trade-offs at conversation level | "Would you use Mongo or Postgres for X, and why?" |

**Exit gate (week 6):** diagnostic mock battery — one coding, one design, one behavioral round. Results reorder Phase B.
