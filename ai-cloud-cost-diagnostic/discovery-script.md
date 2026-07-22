# AI & Cloud Cost Diagnostic — Discovery Script

A founder-informed discovery structure for Phase A. Follows the standard-work discovery shape: context → current state → cost of inaction → readiness → pilot decision. Objection responses stay inside `claim-governance.md` (strongest defensible version; no barred claims; no guarantee before discovery).

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## 0. Frame (say this early)

"This is a bounded, read-only diagnostic. We look at spend **metadata** — not your prompts, not your code. At the end you get a defensible baseline, a breakdown of what's driving cost, and an honest recommendation on whether a routing pilot is even worth it. Sometimes the answer is 'you're already efficient' — and that's a valid, useful result."

This sets the metadata-only boundary and the "valuable even when the answer is no" expectation up front.

## 1. Context
- What does the company sell, and which product features use AI?
- What changed recently that put AI/cloud cost on the agenda? (Listen for the triggering event / invoice shock.)
- Who owns this decision, and who feels the pain on the P&L?

## 2. Current state
- Which model providers and cloud services are in use? Roughly what's the monthly combined spend? *(Qualification gate: ≥ $20K/mo.)*
- Which workloads drive the most inference volume? Any obvious "expensive model on a cheap task" patterns?
- How is spend currently tracked — one dashboard, or scattered?
- What's manual, expensive, or unreliable about the current setup?

## 3. Cost of inaction
- What does the current spend trajectory cost over the next few quarters?
- Is any AI feature's unit economics upside-down (cost > revenue it drives)?
- What breaks or gets scrutinized if the bill keeps climbing?

## 4. Readiness
- Can you provide **read-only** billing access and a sample of **inference-log metadata** (token counts, model endpoints, latency) — no payloads? *(See `data-request.md`.)*
- Who authorizes that access? Any security/compliance steps we should plan for?
- What timeline matters to you?

## 5. Pilot decision (Phase A → Phase B)
- If we find a mathematically defensible optimization path, would you want to test it on a bounded workload?
- **Set expectations honestly:** "If we find you're already optimized, Phase A still gives you the baseline and the visibility — and we won't invent a pilot to sell you." 
- **Phase B gate:** "The Enso evaluation pilot involves looking at a small, consented, sanitized sample of workload content to measure quality. We're finalizing the data-governance policy for that, so we scope Phase B only once that's in place." *(DR-6, owner: Zach Kelling — do not promise Phase B data handling.)*

## 6. Objection library (Phase A)

- **"We can't give you API keys or our prompts."** → "Correct — we don't want payloads. We need read-only billing access and inference-log **metadata**: token counts, which endpoints were called, latency. We ingest the metadata, not the content."
- **"How do I know you'll actually save me money?"** → "We don't promise a percentage. Phase A establishes your baseline and identifies where savings are *possible* versus *confirmed*. If there's no meaningful opportunity, we tell you — that's a real outcome, and you still get the baseline."
- **"Isn't this just AWS Cost Explorer?"** → "Cost Explorer reports that you overspent. Our diagnostic categorizes drivers and tells you whether an *active* routing layer could change the economics — and Phase A is the read-only assessment that decides if that's even worth testing."
- **"Is Hanzo going to train on our data?"** → "Phase A never touches your content. For the optional Phase B pilot, the data-governance policy is being finalized by our technical founder before we scope it — we won't hand-wave that." *(DR-6.)*

## 7. Close
Confirm scope (Phase A only, metadata-only), price band ($12–20K), timeline, and the data-access request. Do **not** pre-sell Phase B; note it as a possible next step contingent on Phase A findings and the DR-6 gate.
