# Summary
*What changed in CI/CD and why? 2–3 sentences.*
*Example: "Switch to matrix builds to parallelize tests. Cuts pipeline time by ~40%."*

# Context / Links
- *Tracker link:*
- *Pipeline files touched:* .github/workflows/... or .gitlab-ci.yml, etc.
- *Runners/executors affected:* self-hosted / shared / docker / k8s

# Changes
- Example: "Add caching step for dependencies", "Introduce OIDC auth for cloud deploy"

# Risk & Blast Radius
- *Repos/pipelines impacted:*
- *Protected branches/environments affected:*
- *Secrets or tokens usage changed:*

# Rollout Plan
- *How to deploy the pipeline change:* merge to default, manual import, versioned template
- *Fallback plan:* revert to previous workflow file rev
- *Who to notify:* teams that rely on this pipeline

# Security
- *Runner permissions:* least-privilege verified
- *Token scope/TTL:* reduced or unchanged
- *Supply chain checks:* checksums, SLSA, provenance

# Performance
- *Before → After wall time:* build, test, package, deploy
- *Parallelization and cache strategy:* keys and restore behavior

# Testing
- *Dry-run on fork or test branch:* Yes / No
- *E2E pipeline run in staging:* Yes / No
- *Failure scenarios tested:* cache miss, flaky tests, permission denied

# Verification Steps
1. Trigger pipeline on branch test-pipeline
2. Confirm all jobs succeed and artifacts produced
3. Validate cache hits on second run
4. Confirm deploy job gated by approvals (if required)

# Related Work
- Linked PRs:
- Closes/Fixes: #issue

# Reviewer Checklist
- [ ] *Least-privilege on tokens and runners confirmed*
- [ ] *Secrets masked and not echoed*
- [ ] *Rollback path documented*
- [ ] *Pipeline time improvement or neutrality shown*
- [ ] *Notifications to impacted teams prepared*

# Notes for Ops
- Re-run instructions:
- Known transient failures and how to retry:
- Links to pipeline dashboards:
