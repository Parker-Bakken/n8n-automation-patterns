# Run Logging Pattern

## Goal
Make debugging easy by logging:
- run_id
- input summary (safe fields only)
- key outputs (job_id, urls)
- error messages and status codes
- timestamps and durations

## Minimal log schema
```json
{
  "run_id": "2026-03-05T12:34:56Z_001",
  "pattern": "retry-backoff",
  "step": "render.submit",
  "ok": true,
  "status": 200,
  "duration_ms": 8421,
  "job_id": "abc123",
  "notes": "submitted render job"
}
