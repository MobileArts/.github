# Summary
*What performance goal and why (SLO, cost, throughput).*

# Context / Links
- *Baseline metrics and dashboards:*
- *Hot paths / queries / endpoints targeted:*

# Hypothesis & Approach
- *Bottleneck identified:* CPU, I/O, lock contention, GC, N+1, missing index
- *Optimizations attempted:* caching, indexes, batching, algorithmic changes

# Results
- *Before → After:* p95/p99 latency, throughput (RPS), CPU/mem, DB QPS
- *Load profile used:* request mix, dataset size
- *Cost impact:* infra or query cost deltas

# Safety & Correctness
- *Cache coherence / invalidation notes:*
- *Consistency/ordering guarantees preserved:*
- *Fallback to previous behaviour if degraded:*

# Observability
- *New metrics/traces/logs to track regressions:*
- *Dashboards updated:*

# Rollout
- *Flagged rollout or canary size:*
- *Abort conditions and rollback plan:*

# Testing
- *Unit and integration tests unaffected or updated:*
- *Load/perf test steps others can run:*

# Related Work
- *Linked PRs:*
- *Closes/Fixes:* #issue

# Reviewer Checklist
- [ ] *Results reproduced against baseline*
- [ ] *No functional regressions*
- [ ] *Monitoring for regressions in place*
- [ ] *Rollback path clear*
