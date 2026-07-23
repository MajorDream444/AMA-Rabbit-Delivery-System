# AI & Cloud Cost Diagnostic — Data Request

Exactly what AMA asks the client to provide, by phase. **Phase A is metadata-only and read-only.** Phase B's data request is **provisional and blocked** pending DR-6.

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## Phase A — data request (production-ready, metadata-only)

AMA requests the **minimum** needed to build a defensible baseline. No prompt or response payloads. No write access.

**Requested (read-only):**
1. **Billing exports** for AI/model providers and cloud providers for an agreed window (e.g., last 1–3 billing cycles). CSV/console export is fine.
2. **Inference-log metadata** for a representative sample window: timestamp, model/endpoint identifier, token counts (in/out), request/response size, latency, and workload/service tag. **No prompt text, no completion text, no customer data.**
3. **Model/provider inventory:** which models and services are in use, and for what workload classes.
4. **Latency / error summaries** if available (aggregate, not per-record content).
5. **Workload classification hints:** which services/features generate which traffic.

**Explicitly NOT requested in Phase A:**
- prompt payloads or model outputs;
- API keys with write/production scope;
- source code or production system access;
- any personal or regulated customer data.

**Access mechanics:** read-only billing roles, or client-generated exports handed over through an agreed secure channel. Least-privilege; time-boxed; revocable. Details and handling in `security-and-access.md` §Phase A.

**If the client cannot provide metadata:** there is nothing to audit — see `disqualification-rules.md`.

## Phase B — data request (PROVISIONAL — BLOCKED by DR-6)

> **⛔ DR-6 GATE — Owner: Zach Kelling.** Measuring routing **quality** may require a sample of actual workload content (prompts/outputs). The rules for requesting, minimizing, redacting, storing, retaining, and deleting that content — and whether it may ever influence Enso — **do not yet exist and must be provided in writing by Zach Kelling.** This section is a placeholder and must not be sent to a client until DR-6 resolves.

Provisional intent only (subject to the DR-6 policy, not to be treated as settled):
- a **consented**, **sanitized/redacted** evaluation sample scoped to specific workloads;
- explicit client authorization per workload;
- regulated data excluded unless the resolved policy permits it.

**Until DR-6 resolves, AMA does not request any Phase B content and does not describe how it would be handled.** No invented retention, training, isolation, access-control, or deletion terms appear here by design.

## Data minimization principle (both phases)

Collect the least data that answers the question. Prefer aggregates over records, metadata over content, samples over full history. Everything requested must map to a specific analytical need in `delivery-playbook.md`.
