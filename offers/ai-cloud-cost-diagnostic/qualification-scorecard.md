# AI & Cloud Cost Diagnostic — Qualification Scorecard

Applies the commercialization repo's 0–100 qualification framework (`icp-framework.md` §3) to this specific offer, plus the resolved **$20,000/month** floor (DR-4). Applies to **Phase A**. Phase B has an additional gate (DR-6) that is not a scoring question — it is a hard block.

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## 1. Hard gate before scoring (Phase A)

The qualification question, asked first: **"What is your current monthly spend on AI inference and cloud compute?"**

- **≥ $20,000/month combined** → proceed to scoring.
- **< $20,000/month** → do not pursue high-touch Phase A. Route to rabbit/self-serve or a standardized offer, **unless** an AMA-approved **strategic exception** applies (expansion potential, proprietary-data value, channel leverage, or sovereign/critical-infrastructure mission relevance). Record the exception rationale and approver.

A prospect that cannot or will not disclose approximate spend is treated as unqualified until they can (see `disqualification-rules.md`).

## 2. Scorecard (0–100)

| Dimension | Weight | What "high" looks like for this offer |
|---|---:|---|
| Pain severity | 20 | Acute invoice shock; unit economics upside-down on an AI feature |
| Measurable financial impact | 15 | Spend is large and itemizable; savings would be material in dollars |
| Urgency / triggering event | 15 | Recent bill spike, budget mandate, or board pressure |
| Offer fit | 15 | Multi-model + cloud usage that a routing/optimization lens can actually address |
| Budget capacity | 10 | Can authorize $12–20K without a heavy procurement cycle |
| Access to decision-maker | 10 | CFO economic buyer + VP-Eng champion reachable |
| Technical readiness | 5 | Can provide read-only billing access + inference-log metadata |
| Expansion potential | 5 | Plausible path to production routing (Phase B, once unblocked) or elephant work |
| Proof availability | 5 | Willing to define success criteria and share baseline metadata |

**Tiers:** 80–100 → immediate personalized outreach · 65–79 → research and warm-up · 50–64 → nurture · below 50 → do not prioritize. A large company is not automatically qualified.

## 3. Phase-B readiness (not scored — gated)

Phase B is **not** qualified by score. Even a 100-scoring account cannot be sold Phase B until:

- **DR-6 is resolved** (Zach Kelling's written Enso data-governance policy exists); and
- the client can provide a **consented, sanitized evaluation sample** under that policy; and
- for regulated data (ICP-5), the policy explicitly permits the workload.

Until DR-6 resolves, mark Phase B eligibility as **BLOCKED (DR-6, owner: Zach Kelling)** on every account record.

## 4. Recording

For each prospect capture: monthly AI+cloud spend (approx.), score by dimension, total, tier, whether a strategic exception was applied (and approver), and Phase-B status (default: BLOCKED — DR-6). No client-confidential figures are stored in this repository; scoring happens in AMA's CRM, not here.
