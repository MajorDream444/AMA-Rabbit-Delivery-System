# AI & Cloud Cost Diagnostic — Statement of Work (Template)

Fill-in-the-blanks SOW. **Phase A and Phase B are separate SOWs / separate contracts.** Never issue one combined SOW covering both. Bracketed `[…]` fields are per-engagement.

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

---

## SOW A — Phase A: AI & Cloud Cost Diagnostic

**Parties:** AMA Solutions ("AMA") and `[Client legal name]` ("Client").
**Effective date:** `[date]`.

**1. Objective.** A bounded, read-only, metadata-only diagnostic of Client's AI and cloud spend, producing a defensible baseline, categorized cost drivers, a confirmed-waste vs possible-optimization split, and a go/no-go recommendation on a subsequent Enso Evaluation Pilot.

**2. Scope (in).** Ingestion and analysis of Client-provided billing exports and inference-log **metadata** (per `data-request.md` Phase A); baseline construction; driver categorization; documented assumptions/limitations; written recommendation; client-facing report (`report-template.md`).

**3. Scope (out).** No prompt/response payloads; no source-code or production access; no write access; no live traffic rerouting; no Phase B activities. **No savings percentage is promised.**

**4. Access.** Client grants read-only billing access and provides metadata via `[secure channel]`, least-privilege and time-boxed. See `security-and-access.md`.

**5. Timeline.** `[e.g., 2–3 weeks]` from data receipt to report.

**6. Fee.** **$12,000–$20,000**, fixed at `[$amount]` for this engagement. Payable `[terms]`. **Fee is earned on delivery of the diagnostic regardless of whether a Phase B pilot is recommended** — including a recommendation not to proceed.

**7. Success criteria.** As defined in `success-metrics.md`: a reliable baseline, categorized drivers, documented limitations, a confirmed-vs-possible split, and a clear Phase-B recommendation. **A recommendation of "do not proceed to Phase B" is a successful completion.**

**8. Data handling.** Metadata-only; retention and deletion per `security-and-access.md` §Phase A. No Client personal or regulated data is requested or stored.

**9. Claims.** AMA makes no guarantee of savings, no benchmark or model-supremacy claim, and no representation about Enso performance beyond what Client's own data shows.

---

## SOW B — Phase B: Optional Enso Evaluation Pilot  ⛔ PROVISIONAL — DO NOT ISSUE

> **⛔ DR-6 GATE — Owner: Zach Kelling.** This SOW may **not** be issued to any Client until Zach Kelling supplies the written Enso data-governance policy (retention, training/no-training, tenant isolation, access control, deletion). The data-handling, content-inspection, and regulated-data clauses below are intentionally left as gated placeholders and must be completed from that policy — **not invented here.**

**1. Objective (intent only).** Measure whether Enso routing reduces cost without degrading agreed quality/latency on `[bounded workload]`.

**2. Fee.** **$8,000–$15,000**, separate contract, only if SOW A recommended proceeding.

**3. Data handling.** `⛔ BLOCKED — to be completed from Zach Kelling's DR-6 policy: minimization, redaction, permissions, storage, model providers, retention, deletion, tenant isolation, prohibited data, human approval.` No terms are asserted here.

**4. Regulated data.** `⛔ BLOCKED — eligibility determined solely by the DR-6 policy.` Not sellable into regulated data until then.

**5. Success criteria.** Per `success-metrics.md` §Phase B (also gated for any content-inspecting measurement).

---

## Issuance rules
- Issue **SOW A only** at first sale.
- Issue **SOW B only** after SOW A delivery, a positive recommendation, **and** DR-6 resolution.
- Never merge the two into a single fee or contract.
