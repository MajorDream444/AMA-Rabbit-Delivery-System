# AI & Cloud Cost Diagnostic — Offer Specification

The flagship rabbit offer. Sold as **two separate contracts**: **Phase A — AI & Cloud Cost Diagnostic** (production-ready, metadata-only) and **Phase B — optional Enso Evaluation Pilot** (provisional, gated). Governed by the commercialization repo's `claim-governance.md`, `commercialization-doctrine-v1.md`, `offer-portfolio.md`, and `icp-framework.md`.

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## 0. Two-contract structure (do not collapse)

| | Phase A — AI & Cloud Cost Diagnostic | Phase B — optional Enso Evaluation Pilot |
|---|---|---|
| Price | **$12,000–$20,000** | **$8,000–$15,000** |
| Contract | Separate contract, signed first | Separate contract, only if Phase A justifies it |
| Status | **Production-ready** | **PROVISIONAL — BLOCKED by DR-6** (owner: **Zach Kelling**) |
| Access | Metadata-only, read-only | May require consented, sanitized sample — **policy not yet defined; see `security-and-access.md`** |
| Outcome | Baseline + drivers + a go/no-go recommendation | Measured cost/quality of Enso routing on agreed workloads |

The two bands are **working hypotheses, never presented as guaranteed outcomes**, and the contracts are never merged into one price.

## 1. Problem

Organizations with material AI + cloud spend rarely have a defensible, itemized view of where that money goes or whether it is justified by the value produced. The buyer feels the pain as an "invoice shock" (a frontier-model line item out of proportion to the revenue it drives) but lacks a bounded, low-risk way to get an honest answer.

## 2. Who it is for

Primary ICP-1 (AI-native SaaS, 50–500 employees) at or above the **$20,000/month combined AI + cloud spend** qualification floor (see `qualification-scorecard.md`). Economic buyer: CFO. Champion: VP Eng / Head of AI. Below-floor or non-fit prospects are routed or declined per `disqualification-rules.md`.

## 3. Phase A — scope (production-ready)

**Phase A is a historical, read-only, metadata-only audit.** It does not touch production code, does not require API keys with write scope, and does not ingest prompt payloads by default.

Deliverables:
1. A reliable **spend baseline** across AI inference and cloud compute for an agreed window.
2. **Cost drivers** identified and categorized (by model/provider, workload class, endpoint, environment).
3. **Assumptions and data limitations** documented explicitly.
4. A clear separation of **confirmed waste** from **possible optimization** (hypotheses requiring validation).
5. A **go/no-go recommendation** on whether a Phase B Enso Evaluation Pilot is economically justified.
6. A client-facing **diagnostic report** (`report-template.md`).

**Phase A succeeds even when the recommendation is "do not proceed to Phase B."** A legitimate, valuable Phase A outcome is: *"Your spend is already well-optimized; no economically meaningful Enso pilot is warranted."* The client still receives the baseline, the driver breakdown, the confirmed-waste findings, and a unified view of their spend — worth the fee on its own. AMA never manufactures a Phase B recommendation to sell the next contract (`commercialization-doctrine-v1.md` §1).

Phase A explicitly does **not**:
- promise any savings percentage (barred; `claim-governance.md` §3);
- move or reroute any live traffic;
- require prompt/response payloads (metadata only — see `data-request.md`).

## 4. Phase B — optional Enso Evaluation Pilot (PROVISIONAL — BLOCKED)

> **⛔ DR-6 GATE — Owner: Zach Kelling.** Phase B measures whether Enso routing reduces cost without degrading agreed quality/latency on a bounded set of workloads. Doing so may require inspecting some workload content (a consented, sanitized evaluation sample). **The data-governance policy that would make this safe — retention, training/no-training, tenant isolation, access control, deletion — does not yet exist and must be supplied in writing by Zach Kelling before Phase B may be scoped, priced to a specific client, or sold.** This document does not invent that policy. See `security-and-access.md` for the gated placeholders.

Phase B is described here only at the level of intent. Its concrete data handling, success thresholds involving content inspection, and any regulated-data eligibility remain blocked until DR-6 is resolved. Phase B is **not** sellable into regulated ICP-5 data until then.

## 5. Boundaries and claim discipline

- No barred claims anywhere in Phase A or Phase B materials (no "number-one AI," no guaranteed savings %, no benchmark supremacy).
- Enso is described as the intelligent routing/transmission layer, never a benchmark winner.
- Any reference to the regulated-market case study is gated on client permission (DR-7).
- Every quantitative claim in a client deliverable traces to that client's own data, not to founder-reported figures.

## 6. Readiness gates (operational)

This offer may not be delivered, demoed, or sold until the module's readiness gates pass: see `delivery-playbook.md` (delivery gate), `security-and-access.md` (data/PII gate), `success-metrics.md` (outcome gate), and `internal-dry-run.md` (must be executed on AMA/Hanzo's own spend before the first paid client).
