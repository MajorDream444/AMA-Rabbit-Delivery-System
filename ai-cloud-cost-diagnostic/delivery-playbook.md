# AI & Cloud Cost Diagnostic — Delivery Playbook

Step-by-step execution for **Phase A**, designed for repeatable analyst-/architect-led delivery **after** the internal dry run, playbook validation, and escalation protocol are complete (a design goal, not a claim of current readiness). Phase B execution is **gated** (DR-6).

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## Delivery readiness gate (must pass before any paid delivery)

- [ ] `internal-dry-run.md` executed end-to-end on AMA/Hanzo's own spend.
- [ ] This playbook validated against that dry run; gaps fixed.
- [ ] Escalation protocol (commercialization repo `zach-escalation-policy.md`) understood; default is zero Zach involvement.
- [ ] Data/PII gate in `security-and-access.md` passed for the engagement.

If any box is unchecked, do not deliver to a paying client.

## Phase A — steps

### 1. Intake & access
- Confirm signed **SOW A** and the ≥ $20K/mo qualification.
- Receive read-only billing exports + inference-log **metadata** per `data-request.md`. Verify **no payloads/PII** arrived; if content slipped in, stop and follow `security-and-access.md` handling.
- Log the data inventory (what, window, format) — metadata only.

### 2. Baseline construction
- Normalize billing across providers into a common schema (provider, service, workload tag, period, cost).
- Build the spend **baseline** for the agreed window; reconcile against invoice totals.
- Note gaps/assumptions (missing tags, partial windows) explicitly.

### 3. Driver categorization
- Attribute spend by model/provider, workload class, endpoint, and environment.
- Identify patterns: expensive-model-on-cheap-task, redundant calls, idle/overprovisioned resources, data-transfer/storage drivers.
- Rank drivers by dollar magnitude.

### 4. Confirmed-waste vs possible-optimization
- **Confirmed waste:** defensible from the data alone (e.g., idle resources, duplicate spend). State it plainly.
- **Possible optimization:** hypotheses that would require validation (e.g., "workload X *might* route to a cheaper model") — labeled as hypotheses, never as promised savings.
- Do **not** compute or present a guaranteed savings percentage (`claim-governance.md`).

### 5. Phase-B recommendation (go/no-go)
- Decide, from the evidence, whether an Enso Evaluation Pilot is economically justified.
- **A "do not proceed" recommendation is a valid, complete deliverable.** If the client is already efficient, say so; the baseline and driver breakdown stand on their own.
- If "proceed," define the smallest bounded workload that would test the hypothesis — and mark Phase B **BLOCKED pending DR-6** in the report (do not scope content handling).

### 6. Report & handoff
- Produce the client-facing report from `report-template.md`.
- Capture engagement evidence per `evidence-capture.md` (metadata/aggregates only; no client-confidential content).
- Walk the client through findings; present the recommendation honestly.

## Phase B — execution  ⛔ BLOCKED

> **⛔ DR-6 GATE — Owner: Zach Kelling.** Phase B execution (which may inspect workload content) has **no playbook steps here** because the governing data policy does not exist. Do not draft, dry-run, or deliver Phase B until DR-6 resolves and `security-and-access.md` §Phase B is completed from Zach's policy.

## Escalation
Default: no Zach involvement. Escalate only per the commercialization repo's `zach-escalation-policy.md` (qualified, funded, proprietary-capability-dependent, strategic). A recurring delivery blocker is a productization signal — feed it back into this playbook.

## Observability of the delivery process (operational)
Each engagement records, in AMA's systems (not this repo): data received (inventory only), steps completed, time per step, blockers/escalations, and the final recommendation. This is process telemetry — it must contain **no client-confidential content, no secrets, no PII** (see `security-and-access.md`).
