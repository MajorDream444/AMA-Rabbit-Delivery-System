# Production Readiness Gate

Every delivery module must pass this gate before demo, sale, deployment, or client handoff.

## Tests

- [ ] Changed behavior and critical journeys have automated coverage.
- [ ] Failure, retry, timeout, invalid-input, and authorization paths are covered where relevant.
- [ ] CI passes using synthetic or irreversibly anonymized data.

Evidence:

> Add commands, CI links, coverage, and exceptions.

## Observability

- [ ] Structured, privacy-safe logs and error capture exist.
- [ ] Health, latency, error rate, dependency signals, and alerts exist where relevant.
- [ ] Alerts and rollback/containment have named owners.
- [ ] No secrets, prompt contents, or unnecessary PII reach telemetry.

Evidence:

> Add dashboards, alerts, sanitized sample events, owner, and rollback path.

## Data and PII

- [ ] Inputs, purpose, storage, processors, outputs, retention, and deletion are mapped.
- [ ] Collection is minimized and sensitive fields are encrypted.
- [ ] Access is least-privilege and auditable.
- [ ] PII is redacted from prompts, logs, traces, analytics, fixtures, screenshots, and support artifacts.
- [ ] Model providers and other subprocessors are approved and documented.
- [ ] Consent, export, correction, deletion, and incident obligations are handled where applicable.

Data flow:

> Source → processing → storage → subprocessors → output → retention/deletion.

## Decision

- [ ] PASS
- [ ] EXCEPTION — owner, risk acceptance, compensating control, and expiry recorded
- [ ] BLOCKED — do not commercialize or deploy

Codex, Claude Code, and other coding agents must treat this gate as part of every task and may not claim completion without evidence.

## 2026-10-18 workspace strategy and skills update — scoped review
Owner: Major Dream Williams (product decision); author: Codex. Scope: documentation and instructional skill files only; no runtime changes.
- Tests: four SKILL.md packages pass quick_validate.py. Synthetic forward test verified 60/40 provisional allocation, 50/50 after an additional payment, disputed-entry exclusion, design-defect classification and new-feature change control. No application tests or CI run claimed; runtime behavior is unchanged.
- Observability: not applicable to this documentation-only patch; no executing production paths or telemetry added. Runtime logging/alerting remains a proposed release gate, not certified complete.
- Data/PII: input was current repo documentation, user instructions and a supplied handbook sample. Outputs are abstract strategy, fictional templates and skills stored in GitHub. No sponsor originals, credentials, real contributor ledger or handbook PDF copied. No live data migration, model integration or new retention processor.
- Decision: documentation ready for review only. Commercial product release remains BLOCKED pending pilot and production gates in docs/workspace-product-family-2026-10-18.md. Existing unchecked runtime controls above remain unchanged.
