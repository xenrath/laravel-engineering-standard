# Security Review Workflow

## Steps
1. Establish scope, data classification, exposure, actors, and criticality.
2. Identify assets, entry points, trust boundaries, and abuse cases.
3. Review authentication, session/token lifecycle, authorization, object ownership, and privileged operations.
4. Review validation, output encoding, SQL, CSRF, SSRF, file handling, redirects, rate limits, and error leakage.
5. Review sensitive data, logs, secrets, backups, dependencies, CI permissions, and production configuration.
6. Map relevant controls to OWASP ASVS/WSTG or applicable policy; do not claim full compliance from partial review.
7. Run authorized SAST, dependency/secret scanning, DAST, and focused tests where available.
8. Rate findings with severity rationale, impact, exploitability, evidence, owner, and remediation.
9. Retest fixes and document residual risk/accepted exceptions.
10. Escalate suspected active compromise through incident response.

## Exit criteria
Critical findings addressed or explicitly blocked from release; residual risks owned; evidence and scope limitations recorded.
