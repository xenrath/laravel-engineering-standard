# CI/CD Workflow

## 1. Pipeline stages
A typical pipeline may include:
1. Checkout and trusted dependency installation.
2. Formatting/lint.
3. Static analysis.
4. Unit/feature/integration tests.
5. Dependency and secret scanning.
6. Frontend build and artifact creation.
7. Artifact provenance and retention.
8. Staging deployment.
9. Smoke/acceptance checks.
10. Approval-gated production promotion.

Adapt stages to project risk and infrastructure.

## 2. Pipeline security
- Use least-privilege workflow permissions.
- Protect deployment environments and secrets.
- Avoid printing secrets in logs.
- Pin or verify third-party actions according to organizational policy.
- Do not run untrusted pull-request code with privileged production secrets.
- Separate build and deploy permissions where practical.

## 3. Quality gates
Define blocking vs advisory checks, required approvals, branch protection, and exception expiry. A skipped/failed required check is not a pass.

## 4. Artifact promotion
Prefer promoting the same immutable artifact through environments rather than rebuilding different binaries per environment. Record commit, artifact identifier, dependency lock, and build result.

## 5. Operations
Monitor pipeline failures, flaky tests, deployment duration, rollback frequency, and vulnerabilities. Document owner and recovery for failed deployment.
