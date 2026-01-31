# Failures I’ve Learned From

Experience is measured in failures understood — not features shipped.

These are anonymized lessons from real production systems.

---

## 1. “Temporary” Fixes Are Permanent

Short-term workarounds often outlive the systems they were meant to patch.

Lesson:
- Treat temporary fixes as permanent until proven otherwise
- Document intent, always
- Schedule removal immediately — or accept the debt consciously

---

## 2. Silent Failures Destroy Trust

The most damaging failures are not outages — they are incorrect behavior.

Lesson:
- Crashes are easier to detect than lies
- Systems must fail loudly when correctness is at risk
- Monitoring must detect *wrong* results, not just errors

---

## 3. Most Outages Happen at Boundaries

Rarely inside core logic.

Lesson:
- Validate inputs aggressively
- Assume downstream systems will misbehave
- Treat integrations as hostile by default

---

## 4. Data Quality Is an Operational Problem

Bad data bypasses most safeguards.

Lesson:
- Validate early
- Normalize aggressively
- Track provenance
- Make corruption visible

---

## 5. AI Fails Confidently

AI systems produce plausible nonsense.

Lesson:
- Never trust AI outputs blindly
- Constrain AI with deterministic checks
- Always provide fallbacks
- Make uncertainty visible to users

---

## 6. Rewrites Fail More Often Than They Succeed

Most rewrites fail because they underestimate edge cases.

Lesson:
- Replace parts, not systems
- Preserve institutional knowledge
- Fix what hurts most first

---

## Final Lesson

The cost of failure is rarely downtime.

The real cost is **loss of trust** — from users, teams, and stakeholders.

Every system I design now optimizes to preserve trust under failure.
