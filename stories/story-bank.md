# STAR Story Bank

8–10 stories from Hari's real 4–6 years, each mapped to senior signals and drilled to a 90-second spoken version. Built during IC2 (weeks 1–2), refined every time a `/mock` behavioral round surfaces a better telling. A story isn't "done" until it's been delivered aloud twice without notes.

## Signal coverage map

Every signal needs ≥1 strong story. Gaps here are behavioral-round risk.

| Senior signal | Story #s | Covered? |
|---|---|---|
| Ownership (end-to-end, beyond assigned scope) | S1 | ◐ (brackets pending) |
| Conflict / disagreement handled well | S2 | ◐ (brackets pending) |
| Ambiguity (acted without clear requirements) | | ☐ |
| Mentoring / multiplying others | S1 | ◐ (reframe monitoring→growing) |
| Failure + what changed after | | ☐ |
| Measurable impact (metric moved) | S1, S2 | ◐ (numbers needed) |
| Technical judgment (chose boring/right over shiny) | S2 | ◐ |
| AI adoption (tools today; project story grows here) | S3 | ◐ (needs IC6 vocabulary pass) |

## Story template

```
## S# — {short title}
**Signals:** {1–3 from the map}
**Situation:** {1–2 sentences of context — company, project, stakes}
**Task:** {what was YOURS to solve}
**Action:** {what YOU did — "I", not "we"; the decisions, not the chronology}
**Result:** {outcome with a number if at all possible + what you'd do differently}
**90-sec spoken version drilled:** ☐☐  (tick once per clean aloud delivery)
```

## Stories

_Further stories to be mined in the IC2 session — bring: past projects list, performance review fragments, anything with numbers._

## S1 — Localisation pipeline (ownership + delegation-as-growth)
**Signals:** Ownership, Mentoring, Measurable impact
**Situation:** Expanding to new markets; translations fetched from [the source] at runtime — slow and fragile.
**Task:** Owned the redesign end-to-end, with one junior engineer.
**Action:** Design-first process — options mapped before code. The contested call was [WHICH design choice? — fill in]. [WHO pushed back and what was their concern?]. Chose [X] because [trade-off]. Scoped deliberately against over-engineering. Delegated [component] to the junior with a mid-point design review.
**Result:** Round-trip time dropped [BY HOW MUCH? — fill in] because content ships closer to where it's built. Junior ran the next [launch/iteration] solo — the multiplier part.
**Homework brackets:** the contested design call · who pushed back · quantified round-trip win. Reframe delegation from *monitoring* ("kept him in scope") to *growing* ("by the end he owned X").
**90-sec spoken version drilled:** ☐☐

## S2 — POST-for-search disagreement (conflict + judgment) ⭐ strongest conflict story
**Signals:** Conflict, Technical judgment, Measurable impact
**Situation:** Localisation system fetches translations for 200–300 string keys per request; query-string length limits meant GET couldn't carry the payload.
**Task:** Needed a fetch design a skeptical colleague would ship.
**Action:** Proposed a single POST carrying the keys, with a deterministic-hash caching layer — subsequent lookups become plain cacheable GETs. Colleague objected on REST semantics; his underlying concern was [CONFIRM: cacheability? idempotency?] — which the hash-GET layer specifically addressed. Rather than argue principles, ran a performance test: single POST vs batched GETs.
**Result:** POST won by 2–3 seconds [per WHAT? — page load / request cycle — fill in]; colleague agreed; shipped. Keynote line: **"Architectural disagreements get resolved with measurements, not seniority."**
**Homework brackets:** colleague's real underlying concern · exact perf numbers and their denominator. NEVER open this story with a disclaimer.
**90-sec spoken version drilled:** ☐☐

## S3 (candidate, in progress) — Food-expiry app (AI adoption)
**Status: DESIGN only — nothing built yet.** The story arc this becomes: *"I designed my own AI product — vision extraction + RAG over government food-safety sources — and then built it end-to-end"* as the A-track proceeds (vision → RAG → agents → evals). Grows more tellable with every project milestone.
**⚠ Claim-calibration lesson (from the Q2 diagnostic):** first telling used "I created a RAG pipeline" for a design — one interviewer follow-up ("which embedding model?") would have collapsed credibility. Interview-safe verbs until built: *designed*, *specced*, *am building*. Precise claims impress more, not less.
Also needs the IC6 vocabulary pass (no "stateful model" phrasing), and — once built — one vision failure mode, one retrieval lesson, the grounding rule.
**90-sec spoken version drilled:** ☐☐ (do not drill until the build starts — the story isn't true yet)
