# PR Template Picker

Choose the template that best fits your change. The page will reload with the selected template applied.

## Backend
- [Backend — Feature](?template=backend-feature.md)
- [Backend — Bugfix](?template=backend-bugfix.md)
- [Backend — Hotfix (Prod)](?template=backend-hotfix.md)
- [Backend — Migration (Schema/Data)](?template=backend-migration.md)
- [Backend — API Contract Change](?template=backend-api-change.md)
- [Backend — Performance](?template=backend-performance.md)
- [Backend — Mega Checklist (Multi-area)](?template=backend-mega-checklist.md)

## DevOps
- [DevOps — Infra Change (IaC)](?template=devops-infra-change.md)
- [DevOps — Pipeline Update](?template=devops-pipeline-update.md)
- [DevOps — Monitoring / Alerting](?template=devops-monitoring-alerting-change.md)
- [DevOps — Security Hardening](?template=devops-security-hardening.md)
- [DevOps — Mega Checklist (Multi-area)](?template=devops-mega-checklist.md)

---

### Having trouble?
- Ensure this picker file is at: `.github/pull_request_template.md` (org-level `.github` repo, default branch).
- Ensure specific templates live in: `.github/PULL_REQUEST_TEMPLATE/` in the **target repo** (or are inherited from this org `.github` repo if the target repo has no local overrides).
- If links don’t reload with a template (rare browser quirk), open a new PR and append `&template=backend-feature.md` (or the file you want) to the URL.
