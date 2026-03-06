# API Response Normalization Pattern

## Problem
Different APIs return different shapes:
- some return `data`, others `results`
- error formats vary
- success may be 200 or 201

This pattern standardizes responses into:

```json
{
  "ok": true,
  "status": 200,
  "data": {},
  "error": null,
  "meta": {}
}
