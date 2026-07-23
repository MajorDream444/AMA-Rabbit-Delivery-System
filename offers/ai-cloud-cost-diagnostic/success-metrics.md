# AI & Cloud Cost Diagnostic — Success Metrics

Defines what "done well" means. **Phase A success is NOT a minimum savings percentage** (per the resolved decision DR-5 in the commercialization repo). Phase B outcome metrics are partly gated (DR-6).

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## Phase A — success criteria (outcome gate)

Phase A is successful when AMA has:

1. **Established a reliable baseline** of AI + cloud spend for the agreed window, reconciled to invoice totals.
2. **Identified and categorized material cost drivers** (by model/provider, workload, endpoint, environment).
3. **Documented assumptions and data limitations** explicitly.
4. **Distinguished confirmed waste from possible optimization** (hypotheses labeled as such).
5. **Determined whether a Phase B pilot is justified** — a clear go/no-go.
6. **Produced an actionable client report** (`report-template.md`).

### Explicitly NOT a success criterion
- **No minimum "identified savings ≥ X%" gate.** Phase A does not have to find a given savings level to have succeeded (DR-5).
- **"Do not proceed to Phase B" is a full success.** If the client is already well-optimized, delivering that honest conclusion — with the baseline and driver breakdown — is a complete, valuable outcome. AMA is paid for the diagnostic, not for manufacturing a pilot.

### Optional internal signal (only if Major approves)
An internal "identified savings ≥ X%" figure may be tracked **as a private qualification signal** for whether to *offer* Phase B — never as a Phase A success gate and never as an external guarantee. Not enabled unless Major explicitly approves (DR-5 default: none).

## Phase B — success criteria (partly gated)

Intent: demonstrate a **mathematically defensible, reproducible** path to reduced cost on a bounded workload **without statistically significant degradation** in agreed quality/latency thresholds — measured on the client's own workloads.

> **⛔ DR-6 GATE — Owner: Zach Kelling.** Any success measurement that requires inspecting workload **content** (quality scoring on real prompts/outputs) is blocked until the DR-6 data-governance policy exists. Cost/latency metrics computed from metadata may be defined now; **quality metrics that need content are gated.** Do not finalize Phase B success criteria involving content until DR-6 resolves.

## Claims discipline
Success is expressed in the client's own numbers, within the scope of their data. No savings percentage is marketed or guaranteed; no Enso benchmark or supremacy claim is made (`claim-governance.md`). A dashboard or demo is supporting evidence, not proof.

## Measurement hygiene
Baselines and comparisons use documented methodology and stated assumptions. Where data is incomplete, the limitation is reported rather than smoothed over. Reproducibility of the analysis is preferred over a headline number.
