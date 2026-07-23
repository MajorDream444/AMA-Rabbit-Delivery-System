# AI & Cloud Cost Diagnostic — Disqualification Rules

When to decline or route away, protecting AMA focus and the client from a bad fit. Complements `qualification-scorecard.md`. Mirrors the anti-ICP in the commercialization repo's `icp-framework.md` §5.

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## 1. Phase A — disqualify or route away when

- **Below the $20,000/month floor** with no AMA-approved strategic exception → route to rabbit/self-serve or standardized offers, do not pursue high-touch.
- **Cannot provide baseline data** — no read-only billing access and no inference-log metadata → there is nothing to audit.
- **Subsidized cloud-credit program** (e.g., large free-credit grant) with no near-term expiry → efficiency doesn't matter to them yet; nurture, don't sell.
- **No decision-maker or no budget authority** for a $12–20K engagement.
- **Expects a guaranteed savings percentage before discovery** → violates claim governance; reset expectations or decline.
- **Wants unpaid custom development** dressed up as an "audit."
- **Demands Zach's involvement before commercial qualification** → disqualifier signal, not an escalation trigger.
- **Cannot satisfy KYC/KYB** or seeks unauthorized access/circumvention.

## 2. Absolute disqualifiers (never proceed)

- Prospect wants a **liability-free autonomous shell company** or "AI that legally operates itself" → declined on principle (human governance, Decision 10).
- Prospect expects **production deployment without testing, observability, or security controls**.
- Any request that would require AMA to make legal/regulatory representations it cannot make.

## 3. Phase B — hard block (independent of prospect quality)

Phase B may **not** be sold to anyone — regardless of score, budget, or enthusiasm — until:

> **⛔ DR-6 GATE — Owner: Zach Kelling.** No written Enso data-governance policy (retention, training/no-training, tenant isolation, access control, deletion) → Phase B is **BLOCKED**. Do not scope content-inspecting evaluation, quote a client-specific Phase B, or promise regulated-data handling. This is not a scoring penalty; it is a stop.

Additionally, even once DR-6 resolves, disqualify Phase B for a given workload if the client cannot provide a **consented, sanitized** evaluation sample under the resolved policy, or if the data is regulated and the policy does not permit it.

## 4. Handling a disqualification well

Declining is part of the strategy (`commercialization-doctrine-v1.md` §9). Decline in prose, not bullet-pointed dismissal; offer the honest reason and, where appropriate, the lower-touch route (self-serve, standardized). A clean "not now / not this way" preserves the relationship for a future rabbit.

## 5. Record

For every disqualified/routed prospect, log the rule triggered, the routing decision (if any), and any strategic-exception review. No client-confidential data in this repository.
