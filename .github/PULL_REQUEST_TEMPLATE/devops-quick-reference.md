# DevOps PR Template — Quick Reference

Use this guide to pick the **right PR template** fast.

============================================================
DECISION TREE
============================================================

Start
 ├─ Is this primarily infrastructure or config-as-code (Terraform/Helm/Kustomize/Ansible)?
 │    ├─ Yes → Use: infra-change.md
 │    └─ No
 │
 ├─ Is this mainly CI/CD pipeline or runner/executor changes?
 │    ├─ Yes → Use: pipeline-update.md
 │    └─ No
 │
 ├─ Are you changing dashboards, metrics, traces, logs, or alert rules/SLOs?
 │    ├─ Yes → Use: monitoring-alerting-change.md
 │    └─ No
 │
 ├─ Are you tightening security posture (IAM/RBAC, network policy, secrets, scanners)?
 │    ├─ Yes → Use: security-hardening.md
 │    └─ No
 │
 └─ Does the PR span multiple areas above (e.g., cluster upgrade + pipeline + alerts + RBAC)?
      ├─ Yes → Use: devops-mega-checklist.md
      └─ No → Use the closest single-area template and keep answers concise.

============================================================
QUICK CHOOSER TABLE
============================================================

| If your change is mainly about…                     | Pick this template                     | Examples                                                                          |
|-----------------------------------------------------|----------------------------------------|-----------------------------------------------------------------------------------|
| Cloud infra, Kubernetes, Helm, Terraform, Ansible   | infra-change.md                         | New node pool, storage class change, Helm chart upgrade, VPC/WAF rules via IaC    |
| CI/CD workflows, runners, build/deploy steps        | pipeline-update.md                      | Matrix builds, cache keys, OIDC auth, gated deploy job, self-hosted runner config |
| Dashboards, metrics, logs, traces, alert thresholds | monitoring-alerting-change.md           | New Grafana panels, Prometheus rules, log sampling, SLO burn-rate alerts          |
| IAM/RBAC, secrets, network policy, scanners         | security-hardening.md                   | mTLS, key rotation, firewall/NACL updates, image signing, SBOM, vuln gates        |
| Multi-area release (infra + pipeline + monitoring)  | devops-mega-checklist.md                | Cluster upgrade touching workflows, alerts, and RBAC                              |

============================================================
REMINDERS BEFORE YOU OPEN THE PR
============================================================

- Link the tracker ticket and any design/spec docs.
- Include a Deployment Plan and a concrete Rollback Plan.
- Surface Monitoring: dashboards, key metrics, alerts to watch post-merge.
- Call out Security and Compliance (least privilege, secrets handling, scans).
- Notify impacted teams (SRE, Security, App owners) if the change is high risk.
- Add runbook links or quick commands under “Notes for Ops”.

============================================================
WHERE THESE FILES LIVE
============================================================

Place all templates in:
  .github/PULL_REQUEST_TEMPLATE/
    infra-change.md
    pipeline-update.md
    monitoring-alerting-change.md
    security-hardening.md
    devops-mega-checklist.md
    QUICK_REFERENCE.md  ← this file

GitHub will show a "Choose a template" picker when opening a new PR.
