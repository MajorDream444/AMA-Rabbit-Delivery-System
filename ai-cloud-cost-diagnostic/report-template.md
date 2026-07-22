# AI & Cloud Cost Diagnostic — Report Template (Phase A)

The client-facing deliverable skeleton for Phase A. Fill bracketed fields from the client's own data. No barred claims; no guaranteed savings percentage; the recommendation may be "do not proceed."

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

---

## `[Client]` — AI & Cloud Cost Diagnostic
**Prepared by:** AMA Solutions · **Window analyzed:** `[dates]` · **Data basis:** billing exports + inference-log metadata (metadata-only)

### 1. Executive summary
- Current combined AI + cloud spend (baseline): `[$ / month]`.
- Top cost drivers: `[driver 1, driver 2, driver 3]`.
- Confirmed waste identified: `[$ or "none material"]`.
- Possible optimization (requires validation): `[summary or "limited"]`.
- **Recommendation:** `[Proceed to a bounded Enso Evaluation Pilot | Do not proceed — already well-optimized]`.

> If the recommendation is "do not proceed," state plainly that the client's spend is already efficient and that this baseline + visibility is the value delivered. This is an honest, complete result.

### 2. Baseline
- Spend by provider/service, reconciled to invoices: `[table]`.
- Assumptions and data limitations: `[list]`.

### 3. Cost drivers
- By model/provider: `[breakdown]`.
- By workload class / endpoint / environment: `[breakdown]`.
- Notable patterns (e.g., expensive-model-on-cheap-task, idle/overprovisioned, redundant calls): `[list]`.

### 4. Confirmed waste vs possible optimization
- **Confirmed waste** (defensible from the data): `[items with $ impact]`.
- **Possible optimization** (hypotheses to validate — not promises): `[items, each labeled hypothesis]`.
- **No savings percentage is guaranteed.** Figures are Client's own data; optimization items require a pilot to confirm.

### 5. Phase-B recommendation
- Go / no-go: `[decision + rationale]`.
- If go: smallest bounded workload to test: `[workload]`.
- **Phase B (Enso Evaluation Pilot) note:** the pilot involves a consented, sanitized evaluation sample; its data-governance policy is being finalized by AMA's technical founder (Zach Kelling) and Phase B is scoped only once that is in place. *(DR-6.)*

### 6. Scope & method (transparency)
- What we looked at (metadata-only), what we did not (no payloads, no code, no live traffic).
- Method and any reproducibility notes.

### 7. Appendix
- Data inventory (metadata only). No client-confidential content is reproduced in this report beyond aggregates.

---

**Claims footer (include verbatim):** *This diagnostic reflects Client's own spend data for the stated window. AMA makes no guarantee of savings, no benchmark or model-supremacy claim, and no representation about Enso performance beyond what this data shows.*
