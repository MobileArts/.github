# Pull Request Templates — Quick Reference

This folder contains specialized PR templates for **Backend** and **DevOps** work.  
When opening a PR, GitHub will show a **template picker** so you can choose the right one.

---

## 📌 Which Template Should I Use?

### Backend Templates
| Template File                             | When to Use It | Typical Changes |
|-------------------------------------------|----------------|-----------------|
| backend-feature.md                         | New functionality or service logic | New endpoints, features, major refactors |
| backend-bugfix.md                          | Fixing a bug | Logic fixes, data fixes, bug reproductions |
| backend-hotfix.md                          | Urgent production fix | Incident mitigation, live bug patch |
| backend-migration.md                       | Schema/data change | DB schema changes, data backfills, reindexing |
| backend-api-change.md                      | API contract change | Request/response structure changes, versioning |
| backend-performance.md                     | Performance tuning | Query optimization, caching, latency/throughput |
| backend-mega-checklist.md                  | Multi-area backend change | Feature + migration + API + perf in one PR |

### DevOps Templates
| Template File                             | When to Use It | Typical Changes |
|-------------------------------------------|----------------|-----------------|
| devops-infra-change.md                     | Infra/config changes via IaC | Terraform, Helm, Kustomize, Ansible |
| devops-pipeline-update.md                  | CI/CD pipeline updates | Workflow changes, runners, build/deploy steps |
| devops-monitoring-alerting-change.md       | Monitoring or alerting updates | Grafana, Prometheus, alert thresholds |
| devops-security-hardening.md               | Security improvements | IAM/RBAC, secrets rotation, network policy |
| devops-mega-checklist.md                   | Multi-area DevOps change | Infra + pipeline + monitoring + security |

### References (not shown in template picker)
| File                              | Purpose |
|-----------------------------------|---------|
| devops-quick-reference.md          | One-page decision guide for DevOps templates |

---

## 🛠 Using Multiple Templates in GitHub

1. Keep each `.md` file in this folder:
   .github/PULL_REQUEST_TEMPLATE/
   ├─ backend-api-change.md  
   ├─ backend-bugfix.md  
   ├─ backend-feature.md  
   ├─ backend-hotfix.md  
   ├─ backend-mega-checklist.md  
   ├─ backend-migration.md  
   ├─ backend-performance.md  
   ├─ devops-infra-change.md  
   ├─ devops-mega-checklist.md  
   ├─ devops-monitoring-alerting-change.md  
   ├─ devops-pipeline-update.md  
   ├─ devops-quick-reference.md  
   └─ README.md

2. When you create a **new Pull Request**:
   - Click **"Choose a template"** at the top of the PR body.
   - Select the template that matches your change type.
   - Fill it in, then request review.

3. If you forgot to choose, copy-paste the correct template from this folder into your PR body.

---

## 💡 Team Best Practices

- **Link the tracker ticket** and any design/spec docs.
- **Always include Deployment and Rollback plans.**
- **Add post-deploy Monitoring** (dashboards, key metrics, alerts).
- **Call out Security & Compliance** (least privilege, secrets, scans).
- **Keep it concise but complete** — skip sections that don’t apply, but never skip risk or rollback.

---

## ✅ Quick Verification

- Opening a PR should show the **template picker**.  
- Picking a template should pre-fill the PR body accordingly.  
- Non-template docs (like `devops-quick-reference.md`) should **not** appear in the picker.
