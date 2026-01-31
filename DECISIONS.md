# Engineering Decisions I Default To

These are not theoretical preferences.  
They are defaults shaped by production failures, operational pain, and long-term ownership.

---

## 1. Explicit Over Clever

If behavior is not obvious from reading the code, it will fail in production.

- Prefer explicit flows over abstractions
- Prefer readable logic over reusable magic
- Prefer boring code that survives context loss

---

## 2. Fewer Services Beat Premature Microservices

Most systems fail because of **coordination**, not scale.

- Start with fewer, well-defined services
- Split only when boundaries are painfully clear
- Optimize for operability before topology

Distributed systems multiply failure modes.

---

## 3. Data Is the System

Most outages are data problems pretending to be code problems.

- Schemas are first-class design artifacts
- Migrations are treated as production events
- Data loss is worse than downtime
- Backfills and rollbacks are planned early

---

## 4. Ownership Must Be Obvious

Shared responsibility is often disguised ambiguity.

- Every system has a clear owner
- Every decision has a reason
- Every service has an escalation path

If no one owns it, it will rot.

---

## 5. Observability Is a Requirement, Not a Feature

If you can’t explain why something happened, you don’t control the system.

- Logs, metrics, and traces are designed early
- Silent failures are unacceptable
- Alerting favors signal over noise

Debuggability is part of correctness.

---

## 6. AI Is Probabilistic, Not Authoritative

AI systems fail *politely* and *confidently*.

- AI outputs are always validated
- Deterministic systems guard probabilistic ones
- Fallbacks are mandatory
- No silent automation

AI assists decisions — it does not make them.

---

## 7. Incremental Correction Beats Rewrites

Rewrites feel clean. They usually fail.

- Fix boundaries before rebuilding cores
- Replace parts, not entire systems
- Earn simplicity gradually

Systems improve through pressure, not resets.

---

## Final Note

These decisions trade speed for **control**.

In the long run, control is what creates speed.
