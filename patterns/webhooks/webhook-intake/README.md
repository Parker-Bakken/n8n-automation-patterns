# Webhook Intake Pattern

## Problem
Inbound webhooks can be:
- unauthenticated
- duplicated (retries from sender)
- malformed
- noisy

## Pattern
1. Validate signature (if supported)
2. Validate required fields
3. Dedupe using event_id
4. Route by event type
5. Log the run

## Suggested folders
- Add examples of payloads in `/examples/webhooks/`
