# Quick Start

## Prerequisites

1. Dynatrace tenant with Workflows enabled.
2. Account Management access to create an OAuth client with `account-uac-read`.
3. Environment API token with `events.ingest` scope.
4. Credential Vault access to store both credentials.

## Deploy (Focused Workflow)

1. Download `byok-key-access-monitor.workflow.json`.
2. In Dynatrace, open Workflows and upload the file.
3. In task `fetch_byok_notifications`, set:
- `ACCOUNT_UUID`
- `OAUTH_CREDENTIAL_VAULT_ID`
- `EVENTS_TOKEN_VAULT_ID`
4. Enable the workflow.

## Verify

Run in a notebook:

```dql
fetch events
| filter event.name == "BYOK key access lost" or event.name == "BYOK key access restored"
| sort timestamp desc
| limit 20
```

If no records appear after one schedule cycle, check workflow run logs and vault access.
