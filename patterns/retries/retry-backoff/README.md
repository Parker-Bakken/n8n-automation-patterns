# Retry + Backoff Pattern

## Problem
External APIs fail intermittently:
- 429 rate limits
- 5xx server errors
- timeouts

This pattern retries safely using:
- exponential backoff
- jitter
- max attempts
- “fail loud” after threshold

## Recommended behavior
- Retry on: 429, 408, 5xx
- Do NOT retry on: 401/403 (auth), 400 (bad request)
- Use idempotency keys when supported

## Nodes typically used
- HTTP Request
- IF (status code check)
- Wait (dynamic backoff)
- Merge / Loop
- Error Trigger (optional)

## TODOs
- Define max attempts (ex: 5)
- Define base delay (ex: 2s)
- Add alerting after final failure
