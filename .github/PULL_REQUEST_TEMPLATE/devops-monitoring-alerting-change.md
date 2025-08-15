# Summary
*What changed in monitoring/alerting and why?*
*Example: "Add error-budget burn alerts and update p95 latency SLO for checkout-api."*

# Context / Links
- *Service(s) monitored:*
- *Dashboards/alerting tools:* Grafana, Prometheus, Cloud Monitoring, Datadog, etc.
- *Runbooks involved:*

# Changes
- *Metrics added/updated:* names and labels
- *Logs added/updated:* levels, sampling
- *Traces/spans added/updated:* names, attributes
- *Dashboards modified:* titles/panels
- *Alert rules:* thresholds, windows, burn-rate math

# SLO/SLA Impact
- *Targets:* e.g., availability 99.9%, latency p95 300ms
- *Error budget policy changes:*
- *Customer-visible impact if breached:*

# Rollout & Validation
- *How to deploy changes:* config repo, provisioner, UI change
- *How to test:* synthetic checks, load test, replay traffic
- *What to watch after deploy:* specific panels, alert preview

# Noise & Reliability
- *Past false positives addressed:*
- *Rate-limiting / grouping / deadman switch settings:*
- *Paging policy review:* severity mapping to on-call

# Security / Data Sensitivity
- *PII in logs scrubbed:* Yes / No
- *Access control on dashboards/alerts:* updated

# Verification Steps
1. Force a test condition (safe trigger)
2. Confirm alert fires in preview channel
3. Check runbook link is present and accurate
4. Ensure auto-resolve works when condition clears

# Related Work
- Linked PRs:
- Closes/Fixes: #issue

# Reviewer Checklist
- [ ] *Metric names and labels follow conventions*
- [ ] *Dashboards render and variables work*
- [ ] *Alert thresholds justified by SLOs*
- [ ] *Runbooks linked and up-to-date*
- [ ] *Noise controls in place (grouping, delay, suppression)*

# Notes for Ops
- Links to primary dashboards:
- Alerts expected to change frequency:
- On-call rotation informed:
