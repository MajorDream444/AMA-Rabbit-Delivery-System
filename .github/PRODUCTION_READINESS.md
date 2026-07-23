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
