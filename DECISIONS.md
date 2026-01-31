# Engineering Decisions

These are defaults I take into systems when there is uncertainty.  
They are shaped by production failures, operational pressure, and long-term ownership — not theory.

---

## Explicit > Clever

If behavior isn’t obvious by reading the code, it will fail in production.

- Favor explicit over implicit
- Favor clear logic over reusable magic
- Favor readability over abstraction

---

## Fewer Services, Happier Teams

Complex topology increases failure modes.

- Start with fewer, well-defined services
- Split only when boundaries are unavoidable
- Optimize for operations before topology

---

## Data Is the System

Most outages are not bugs in logic — they are data problems.

- Schemas are first-class
- Migrations are treated as events
- Backfills and rollbacks are planned, not afterthoughts

---

## Ownership Must Be Obvious

Shared responsibility creates ambiguity.

- Every service has a clear owner
- Every decision has a reason
- Every critical path has an escalation path

---

## Observability Is Required

If you can’t explain what happened, you don’t control the system.

- Logs, metrics, traces designed early
- Silent failures unacceptable
- Alerts designed to emphasize signal over noise

---

## AI Is Probabilistic

AI systems produce plausible yet incorrect outputs.

- Validate all outputs
- Constrain AI with deterministic logic
- Provide fallback paths
- Make uncertainty visible

---

## Rewrite Is Usually the Wrong First Move

Rewrites wipe institutional knowledge.

- Fix boundaries first
- Replace parts, not systems
- Earn simplicity through hard constraint

---

## Final Note

These decisions trade speed for **control** — and control delivers long-term velocity.
