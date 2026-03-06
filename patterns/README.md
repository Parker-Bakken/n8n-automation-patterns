# Patterns

Each folder contains one or more reusable patterns.

**Conventions:**
- workflow JSON exports should be sanitized (no secrets)
- each pattern should have:
  - a short README explaining the problem it solves
  - a workflow export file (when available)
  - an example input/output payload

Folders:
- `api/` — API request/response patterns
- `data/` — validation, dedupe, transforms
- `retries/` — retries, backoff, idempotency
- `observability/` — logging, metrics, alerts
- `webhooks/` — intake, verification, routing
- `scheduling/` — cron patterns, batching windows
