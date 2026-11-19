# DevOps and Delivery Standards

## 1. Version control

Use a documented branch and pull request strategy appropriate to team size. Protect shared branches. Use meaningful commits and reviewable PRs. Do not force-push or rewrite shared history without explicit approval. Never discard uncommitted user changes.

## 2. CI/CD

Automate appropriate quality checks: formatting, static analysis, tests, dependency/security scans, build, artifact creation, and deployment verification. Keep pipelines reproducible and least-privileged. Separate build from deploy where practical and promote the same artifact across environments.

## 3. Environment management

Maintain clear development, test, staging, and production separation. Document required configuration keys without secret values. Use secret management, least privilege, and environment-specific access. Never copy production secrets into local files or chat context.

## 4. Build and dependency reproducibility

Use lockfiles and repeatable build commands. Pin or constrain dependencies deliberately. Record runtime, extensions, Node/build tooling, and database requirements. Review package updates before adoption.

## 5. Deployment

Use reviewed release artifacts, explicit approvals for production, migration planning, backup/recovery readiness, smoke tests, health checks, and rollback/forward-recovery criteria. Do not blindly run generic deployment commands; follow the actual host and Laravel version.

## 6. Infrastructure

Document web server, PHP runtime/FPM, database, cache, queue workers, scheduler, storage, TLS, firewall, DNS, backups, monitoring, and capacity where applicable. Use Infrastructure as Code when scale/repeatability justifies it.

## 7. Observability and operations

Define structured logs, correlation IDs, metrics, health checks, error monitoring, queue monitoring, alert thresholds, ownership, and retention. Redact sensitive data. Alerts must be actionable and have a response owner.

## 8. Operational safety

Document maintenance windows, access approvals, rollback, incident escalation, and recovery. Production changes require explicit authorization and evidence of readiness.
