# AI & Cloud Cost Diagnostic — Security & Access

Data handling, access controls, and the data/PII readiness gate. **Phase A is fully specified and production-ready.** **Phase B is a set of gated placeholders — no data-governance terms are invented here; they are owned by Zach Kelling (DR-6).**

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## Data / PII readiness gate (must pass before delivery)

- [ ] The only data requested for Phase A is metadata + billing exports (`data-request.md`); no payloads, no PII, no regulated data.
- [ ] Access is read-only, least-privilege, time-boxed, and revocable.
- [ ] A redaction/quarantine procedure exists for content that arrives unexpectedly.
- [ ] Retention and deletion terms for Phase A metadata are agreed with the client.
- [ ] No secrets, tokens, prompt content, or PII will reach logs, telemetry, fixtures, screenshots, or this repository.
- [ ] For Phase B: **DR-6 policy exists in writing** before any content-handling step is scoped. *(If unchecked, Phase B is BLOCKED.)*

## Phase A — data handling (production-ready)

**What we hold:** billing exports and inference-log **metadata** only (token counts, endpoints, latency, workload tags). No prompts, no outputs, no customer data.

- **Ingress:** client-generated exports or read-only billing roles, delivered via an agreed secure channel.
- **Access control:** least-privilege; only the assigned analyst/architect; access time-boxed to the engagement and revoked at close.
- **Storage:** in AMA's controlled environment, encrypted at rest; not in this repository, not in shared drives, not in chat.
- **Retention:** hold only for the engagement plus an agreed short window; then delete. Record the deletion.
- **Deletion:** on request or at retention expiry, delete metadata and confirm in writing.
- **Unexpected content:** if prompt/response content or PII arrives, **stop**, quarantine it, notify the client, and delete on agreement. Do not analyze it.
- **Tenant isolation (Phase A):** each client's metadata is kept segregated; no cross-client mixing. (This is an AMA operational control for the diagnostic's own handling — it is **not** a claim about Enso's internal isolation, which is a DR-6 matter.)

**What we never do in Phase A:** touch production, hold API keys with write scope, request or retain payloads, or make any Enso data claim.

## Phase B — data handling  ⛔ BLOCKED (DR-6, owner: Zach Kelling)

> **⛔ Every subsection below is a placeholder to be completed FROM Zach Kelling's written DR-6 policy. Nothing here is asserted as current policy. Do not fill these in by inference.**

- **Minimization:** `⛔ TBD — DR-6`
- **Redaction / sanitization of samples:** `⛔ TBD — DR-6`
- **Permissions / consent per workload:** `⛔ TBD — DR-6`
- **Storage & encryption:** `⛔ TBD — DR-6`
- **Model providers / subprocessors:** `⛔ TBD — DR-6`
- **Retention:** `⛔ TBD — DR-6`
- **Deletion:** `⛔ TBD — DR-6`
- **Tenant isolation (Enso):** `⛔ TBD — DR-6` — whether customer data can influence shared Enso weights is precisely the unresolved question (commercialization repo OPEN-QUESTIONS D6).
- **Prohibited data / regulated-data eligibility:** `⛔ TBD — DR-6`
- **Human approval steps:** `⛔ TBD — DR-6`

Until this section is completed from Zach's policy, **Phase B is not sellable, not scopeable to a client, and not deliverable.**

## Claims discipline
Do not assert "zero data egress," "no training on your data," or "fully isolated" as blanket properties for Enso — each is deployment-specific and, for the pilot, unresolved (DR-6). Phase A claims are limited to how AMA handles the client's **metadata**, exactly as specified above.

## Ownership
- Phase A security posture: **AMA Solutions** (operational owner).
- Phase B / Enso data-governance policy: **Zach Kelling** (DR-6). This module does not speak for that policy.
