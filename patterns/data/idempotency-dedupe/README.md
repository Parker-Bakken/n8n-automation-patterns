# Idempotency + Dedupe Pattern

## Problem
Automations often re-run:
- retries
- partial failures
- manual replays

Without dedupe, you may:
- double-post content
- double-charge APIs
- produce duplicate renders

## Pattern
1. Generate a unique `run_key` (example: hash of title + date or sheet row ID)
2. Check storage (Sheets / DB / Redis / Data Store) for existing run_key
3. If run_key exists → stop safely
4. If not → write run_key and continue

## Common storage options
- Google Sheets (simple)
- n8n Data Store
- SQLite/Postgres
- Redis

## Notes
If your API supports it, use an **Idempotency-Key** header too.
