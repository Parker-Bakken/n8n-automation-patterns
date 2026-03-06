# n8n Automation Patterns — Ongoing

A library of reusable automation architecture patterns for building scalable n8n workflows.

This repository acts as a **toolkit of automation building blocks** that can be reused across projects.
Patterns are designed to be small, composable, and easy to adapt into new workflows.
This repository contains reusable n8n workflow patterns for building scalable automation systems, including routing, retries, validation, scheduling, API chaining, and AI-content automation.

**Status:** 🚧 Ongoing / Actively Expanding

📐 Architecture: [docs/architecture.md](docs/architecture.md)

---

## Purpose

When building automation systems with multiple APIs, workflows often need common reliability patterns such as retries, validation, logging, and webhook handling.

This repository collects those patterns so they can be reused instead of reinvented.

---

## What You'll Find Here

Patterns for:

* API request and response normalization
* retry and backoff strategies
* idempotency and deduplication
* webhook intake and validation
* observability and run logging
* rate limiting and batching
* scheduling and queue-style workflows

## Automation Patterns Included

- API Integration Pattern
- Conditional Routing Pattern
- Error Handling & Retry Pattern
- Scheduled Workflow Pattern
- Data Transformation Pattern
- Notification & Alert Pattern

---

## Repository Structure

```
patterns/
  api/
  data/
  retries/
  observability/
  webhooks/
  scheduling/

docs/

examples/
```

---

## How to Use These Patterns

1. Browse the pattern folder relevant to your use case
2. Read the `README.md` describing the automation pattern
3. Import the example workflow into n8n if available
4. Replace the placeholder nodes labeled `TODO`
5. Connect the workflow into your automation pipeline

---

## Example Use Cases

These patterns are useful when building systems such as:

* AI content generation pipelines
* API orchestration workflows
* automated video rendering pipelines
* webhook-based integrations
* background processing automations
* scheduled data pipelines

## Example Workflows

This repository includes reusable n8n workflow patterns that can be imported and adapted for real automation systems.

| Pattern | Description |
|---|---|
| api-retry-pattern | Retry-ready API request workflow |
| conditional-router-pattern | Branching logic for workflow routing |
| webhook-to-api-pattern | Webhook-triggered API automation |
| scheduled-api-sync-pattern | Scheduled sync with an external API |
| error-alert-pattern | Error simulation and alerting pattern |
| webhook-validation-pattern | Webhook input validation before processing |
| multi-step-api-enrichment-pattern | Multi-step API chaining and enrichment |
| google-sheets-to-api-pattern | Read rows from Google Sheets and send to API |
| ai-content-routing-pattern | Route AI/content jobs to different pipelines |

## Importing Workflows

1. Download any JSON file from the `workflows/` folder.
2. Open n8n.
3. Click **Import from File**.
4. Select the workflow JSON.
5. Update credentials, URLs, and node settings as needed.

---

## Security

Workflow examples in this repository are **sanitized**.

This repository **never contains:**

* API keys
* tokens
* personal endpoints
* production credentials

Secrets should always be stored in:

* n8n credential manager
* environment variables
* secret managers

---

## Related Project

This repository supports my main automation project:

n8n AI Content Pipeline
https://github.com/Parker-Bakken/n8n-ai-content-pipeline

The pipeline project uses many of the reusable patterns defined in this toolkit.

---

## Author

Parker Bakken
GitHub: https://github.com/Parker-Bakken
