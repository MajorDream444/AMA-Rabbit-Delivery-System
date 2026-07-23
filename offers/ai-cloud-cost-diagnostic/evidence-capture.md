# AI & Cloud Cost Diagnostic — Evidence Capture

What to capture per engagement so that, over time, "Founder-Reported" claims can become "Verified" — without ever storing client-confidential content in this repository. Ties to the commercialization repo's `evidence-registry.md`.

> Canonical spellings: Hanzo, Enso, Lux, AMA Solutions, Zach Kelling, MAIM.

## Purpose

The reproducible-evidence gap is the roadmap (`commercialization-doctrine-v1.md` §6). Each diagnostic is an opportunity to build defensible, **anonymized/aggregate** evidence toward eventually-Verified claims about the diagnostic's value — and, once DR-6 unblocks Phase B, toward the Enso evidence package (DR-8).

## Capture per Phase A engagement (anonymized/aggregate only)

- **Engagement metadata:** anonymized client id, ICP, spend band (bucketed, not exact), window length.
- **Method reproducibility:** the analysis steps and assumptions used (so a second analyst could reproduce the baseline).
- **Outcome type:** proceed / do-not-proceed recommendation (both are valuable data points).
- **Driver categories found** (categorical, not client-identifying).
- **Confirmed-waste categories** (categorical).
- **Cycle time** per delivery step (process telemetry).
- **Objections encountered** (feeds `discovery-script.md` and the commercialization `icp-framework.md`).

**Never captured here:** client names in a way that ties to figures, exact spend, billing exports, inference metadata, prompts, outputs, secrets, or any PII. Evidence lives as anonymized/aggregate summaries; raw client data stays in AMA's controlled environment and is deleted per `security-and-access.md`.

## Feeding the evidence registry

- Aggregate results (e.g., "across N diagnostics, do-not-proceed rate was M%") can, once independently reviewable, support moving specific diagnostic-value claims toward **Demonstrated** and eventually **Verified** in `evidence-registry.md`. Company-published or founder-reported status is never auto-upgraded — only independent, reproducible evidence upgrades a claim (`claim-governance.md`).
- **Case-study naming remains gated on DR-7.** No named client case study is produced without written client permission.

## Phase B evidence  ⛔ BLOCKED (DR-6)

> Capturing Phase B evidence would involve workload content and the Enso pilot. **No Phase B evidence is captured until the DR-6 data-governance policy exists** (owner: Zach Kelling). At that point, this section is extended to define what reproducible artifacts feed the Enso evidence package (DR-8) — under Zach's policy, not invented here.

## Hygiene
All captured evidence is reviewed for accidental PII/secret/content leakage before it is stored. Anything that could identify a client's confidential figures is bucketed or removed.
