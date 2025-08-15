# Summary
*What infra/config changed and why? 2–3 sentences.*
*Example: "Add Terraform module for GCS logs bucket with lifecycle. Reduces storage cost and meets retention policy."*

# Context / Links
*Where can reviewers learn more?*
- *Tracker link:*
- *Design/spec doc:*
- *Affected envs:* dev / staging / prod / all

# Changes
*Bullets of infra modifications.*
- Example: "New GKE node pool np-spot", "Helm app version bump to 2.3.0"

# Infrastructure / Config Impact
- *Cloud services touched:* AWS/GCP/Azure (which and why)
- *IaC modules changed:* Terraform/Helm/Kustomize/Ansible (paths)
- *State file impact:* Yes / No (explain)
- *Env vars / secrets added or changed:*
- *Cost estimate impact:*

# Deployment Plan
- *Method:* CI/CD, manual, blue-green, canary, rolling
- *Order of steps:* Example: plan → approve → apply → verify
- *Expected duration:*
- *Downtime expected:* Yes / No (explain)
- *Coordination required:* SRE / App Team / Security / Biz

# Rollback Plan
- *How to revert:* previous state, prior Helm chart, old image
- *Data restoration needed:* Yes / No
- *Automated rollback available:* Yes / No
- *Rollback risks:*

# Monitoring & Post-Deploy Verification
- *Dashboards to watch:*
- *Critical metrics:* CPU/mem, latency, error rate, saturation
- *Logs to check:*
- *Alerts that may fire:*
- *SLO/SLA impact:*

# Security & Compliance
- *Access control changes:* IAM, RBAC
- *Secrets management reviewed:* Yes / No
- *Compliance impact:* ISO 27001, SOC 2, PCI, GDPR
- *Vulnerability scans run:* Yes / No (tool/results summary)

# Testing
- *Plan/apply dry-run performed:* Yes / No
- *Staging apply tested:* Yes / No
- *Perf/load checks:*
- *DR/backout tested:*

# How to Verify After Merge
1. Run pipeline job XYZ
2. Confirm resource ABC exists and healthy
3. Check dashboard DEF for no
