# Summary
*What security posture change and why?*
*Example: "Enforce mTLS between services and rotate service account keys. Reduces risk of credential leakage."*

# Context / Links
- *Threat model or risk register item:*
- *Policy or standard referenced:* ISO 27001, SOC 2, PCI, CIS, NIST
- *Affected systems/environments:*

# Changes
- *Access control (IAM/RBAC) updates:*
- *Network controls:* firewall, SG, NACL, WAF, ingress/egress
- *Secrets management:* rotation, storage backend, envelope encryption
- *Image/code security:* signing, SBOM, vulnerability scan gates
- *Audit/logging changes:*

# Compatibility & Risk
- *Breaking changes:* Yes / No (coordination plan)
- *Dependency on app teams or libraries:*
- *Known edge cases and mitigations:*

# Rollout Plan
- *Phasing/flags:* shadow, permissive, enforce
- *Validation steps:* handshake tests, authz checks
- *Rollback plan:* how to disable controls safely

# Monitoring & Evidence
- *Security dashboards to watch:*
- *Alerts newly added:*
- *Evidence collection for audit:* pipeline logs, scan reports, approvals

# Testing
- *Pen test or ad-hoc checks performed:*
- *Negative and boundary tests:*
- *Disaster recovery or key loss scenarios:*

# Verification Steps
1. Confirm policy enforced in staging
2. Attempt unauthorized access; verify denied and logged
3. Validate key/cert rotation without downtime
4. Capture evidence artifacts

# Related Work
- Linked PRs:
- Closes/Fixes: #issue

# Reviewer Checklist
- [ ] *Least-privilege validated*
- [ ] *Secrets rotated or scoped with TTL*
- [ ] *mTLS/policies enforced and observable*
- [ ] *Audit evidence attached or linked*
- [ ] *Rollback documented and tested*

# Notes for Ops
- Commands to apply and rollback:
- Evidence links for auditors:
- Who to contact (SecOps owner):
