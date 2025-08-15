# Summary
*What did you change and why does it matter? Keep it to 2–3 sentences.*  
*Example: "Add PATCH /v1/users/{id} to update profile fields. Fixes missing validation on email update."*

# Context / Links
*Where can reviewers learn more?*
- *Tracker link (e.g., JIRA / GitHub Issue):*
- *Design/spec doc (if any):*
- *Service / module (e.g., user-svc, billing-api):*

# Changes
*List the main code or behavior changes in bullets. Avoid implementation detail here.*  
*Example: "Add UsersController.patch()", "Introduce UserEmailUpdated event", "Refactor validation utils".*
- Changes_number_1

# API and Compatibility
*Call out any API surface changes so client teams aren’t surprised.*
- *Endpoints touched/added:* Example: "PATCH /v1/users/{id}" added; "GET /v1/users" response adds is_active.
- *Breaking change:* Yes / No. If Yes, describe how clients must change and by when.
- *Contract examples (before → after):*

*Example request (before):*
```
PATCH /v1/users/123  
{ "email": "a@b.com" }
```

*Example request (after):*
```
PATCH /v1/users/123  
{ "email": "a@b.com", "display_name": "Alice" }
```

# Data and Migrations
*If the DB changes, explain it. Reviewers need safety and rollback steps.*
- *Schema/data change:* Yes / No
- *Migration ID(s):* Example: "20250815_add_display_name_to_users"
- *Type:* schema / data backfill / reindex
- *Is it idempotent?* If re-run, will it safely do nothing harmful?
- *Rollback plan:* How to undo (e.g., revert migration X; keep nullable column until cleanup).
- *Expected runtime & size:* e.g., "Affects ~2M rows; ~10 min off-peak".
- *Backfill approach:* Batch size, rate limit, pause/resume. Example: "1k rows/batch, sleep 200ms".

# Config and Feature Flags
*New env vars, secrets, or flags need extra care.*
- *New env vars / secrets:* Name, purpose, default, who owns rotation.
- *Feature flags:* Name, default (on/off), who can flip, removal date/plan.

# Security and Privacy
*Think auth, permissions, data exposure, and logging.*
- *AuthN/AuthZ impact:* Who can call this? New roles/permissions?
- *Input validation changes:* What did you validate that wasn’t before?
- *Sensitive data touched (PII/PCI/Secrets):* Yes / No. If Yes, where stored and encrypted?
- *Logging & redaction:* Confirm sensitive fields are masked or not logged.
- *Threats considered:* e.g., SQL injection, IDOR, race conditions, replay attacks.

# Observability
*So SRE/on-call can see what’s happening.*
- *Metrics:* Names and labels. Example: user_update_attempt_total{result="success|error"}
- *Logs:* New messages and levels. Avoid PII. Example: "user_patch_success" at info level.
- *Traces/spans:* Key spans or attributes added.
- *Alerts / SLO:* Any alert rule changes or dashboards to update?

# Performance
*Did you measure? Put simple numbers here.*
- *Load test results vs baseline:* e.g., "p95 220ms → 180ms @ 200 RPS; CPU -5%; DB QPS +2%".
- *Hot paths affected:* Endpoints/queries likely impacted.

# Rollout Plan
*How to deploy safely and undo if needed.*
- *Order of deploys (if multi-service):* Example: "Deploy schema first, then app v2, then enable flag."
- *Smoke test steps:* Simple check right after deploy. Example curl below.
- *Rollback plan:* Exactly how to revert (flags to off, rollback image, revert migration?).
- *Coordination needed:* Teams, time window, migration guardians.
- *Monitoring after deploy:* How to monitor, and alerted if there's any error.

# Testing
*What you tested and how others can run it.*
- *Unit tests:* New/updated tests and main cases covered.
- *Integration/contract tests:* How to run locally (commands).
- *Edge/failure cases:* What could break and how you covered it (timeouts, duplicates, invalid input).

# How to Verify Locally / Staging
*Exact steps reviewers can follow. Copy-paste friendly is best.*
1. *Prereqs:* Run DB migration, set env vars (list them).
2. *Run app:* Example: make up or docker compose up api db.
3. *Try this request:*
```bash
curl -X PATCH http://localhost:8080/v1/users/123 \
  -H "Authorization: Bearer <token>" \
  -H "Content-Type: application/json" \
  -d '{ "email": "a@b.com", "display_name": "Alice" }'
```
4. *Expected result:* HTTP 200; response includes "display_name":"Alice".

# Related Work
*Link anything connected so reviewers see the full picture.*
- *Linked PRs (other services/IaC):*
- *Closes/Fixes:* #issue-number

# Related Documentation
*Links to runbooks, diagrams, or config files used for this changes*
- *[Runbook: JWT Token Service](https://link-to-doc)*

# Reviewer Checklist
*Tick these before requesting review (self-check).*
- [ ] *Style/lint pass locally (include command if non-standard).*
- [ ] *All tests passing locally/CI.*
- [ ] *Migrations tested on a recent DB snapshot.*
- [ ] *OpenAPI/API docs updated (if API changed).*
- [ ] *Metrics/logs/traces added or updated.*
- [ ] *Security/privacy risks considered; no secrets in code or logs.*
- [ ] *Release notes and changelog entries added for this change (if applicable).*

# Notes for Release / Ops
*Short bullets the on-call will read at 2 AM. Ports, flags to flip, dashboards to watch, runbooks.*

