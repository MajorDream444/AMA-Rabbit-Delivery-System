# AI & Cloud Cost Diagnostic — Internal Dry Run

Run the entire Phase A diagnostic on **AMA/Hanzo's own AI + cloud spend** before delivering to any paying client. This validates the playbook, the data request, the report, and the security posture on data AMA already controls. **No paid delivery until this passes.**

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## Why
- Proves the diagnostic works end-to-end without Zach (agency-trap avoidance).
- De-risks the metadata-only data request and the security handling on real-but-owned data.
- Surfaces gaps in the playbook and report before a client sees them.
- Establishes an internal reference baseline.

## Dry-run checklist (Phase A)

**Setup**
- [ ] Assemble AMA/Hanzo billing exports + inference-log metadata (metadata-only; treat as if client data).
- [ ] Confirm no payloads/PII are included; exercise the quarantine procedure deliberately with a planted content sample and verify it is caught and removed.

**Execution (follow `delivery-playbook.md`)**
- [ ] Build the baseline; reconcile to internal invoices.
- [ ] Categorize drivers; rank by dollar magnitude.
- [ ] Produce a confirmed-waste vs possible-optimization split.
- [ ] Reach a go/no-go recommendation — **including deliberately rehearsing a "do not proceed" write-up** so the honest-negative path is proven, not theoretical.
- [ ] Generate the client-facing report from `report-template.md`.

**Security & data (follow `security-and-access.md`)**
- [ ] Access was read-only, least-privilege, time-boxed.
- [ ] Retention/deletion executed and recorded.
- [ ] No secrets/PII/content reached logs, telemetry, fixtures, screenshots, or either repository.

**Evidence (follow `evidence-capture.md`)**
- [ ] Captured anonymized/aggregate evidence only; verified no confidential figures leaked.

**Readiness gates**
- [ ] Delivery gate (`delivery-playbook.md`) passes.
- [ ] Data/PII gate (`security-and-access.md`) passes.
- [ ] Outcome gate (`success-metrics.md`) passes, including the "do not proceed = success" path.

## Phase B dry run  ⛔ BLOCKED (DR-6, owner: Zach Kelling)
> No Phase B dry run is performed until the DR-6 data-governance policy exists. Phase B touches workload content and Enso; rehearsing it without the policy would mean inventing handling rules — explicitly out of scope.

## Sign-off
Record who ran the dry run, date, gaps found, fixes made, and confirmation that all Phase A gates passed. Only after sign-off may the module be used with a paying client. Re-run the dry run whenever the playbook, data request, or security posture changes materially.

## Operational readiness gates (summary for this module)
- **Tests (analysis correctness):** the dry run *is* the test — baseline reconciles to invoices; the do-not-proceed path is exercised; the quarantine procedure catches planted content. Re-run on material change.
- **Observability:** process telemetry (steps, timing, blockers, outcome type) captured in AMA systems, content-free and PII-free.
- **Data / PII:** metadata-only; least-privilege; retention/deletion enforced; unexpected-content quarantine proven. Phase B data handling BLOCKED pending DR-6.
