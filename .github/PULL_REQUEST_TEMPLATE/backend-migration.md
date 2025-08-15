# Summary
*What schema/data change and why (compliance, feature, performance).*

# Context / Links
- *Tracker / design doc:*
- *Tables/indexes affected:*

# Migration Details
- *Type:* schema / data backfill / reindex
- *DDL/DML description:* high-level summary
- *Idempotency:* how safe to re-run
- *Expected runtime & rows affected:*
- *Locking and impact on traffic:*
- *Batching strategy:* batch size, pause, rate limit
- *Failure handling:* resume strategy and checkpoints

# Safety Checks
- *Pre-check queries on snapshot:*
- *Query plans for hot paths after change:*
- *Write amplification / WAL considerations:*
- *Storage growth estimate:*

# Rollout Plan
- *Order:* create nullable column → dual write → backfill → switch reads → drop old
- *Windows:* off-peak times, maintenance window if needed
- *Feature flags involved:*

# Rollback Plan
- *How to revert schema/data safely:*
- *Time to restore and data loss risk:*

# Verification
- *Row counts / checksums before vs after:*
- *Sample queries returning expected results:*
- *Dashboards/alerts to watch:*

# Testing
- *Ran on staging with prod-like data:*
- *Load test / contention test results:*

# Related Work
- *Linked PRs:*
- *Closes/Fixes:* #issue

# Reviewer Checklist
- [ ] *Backfill safe and resumable*
- [ ] *Zero/low-downtime path defined*
- [ ] *Rollback documented and tested*
- [ ] *Indexes and queries reviewed*
- [ ] *Monitoring in place*
