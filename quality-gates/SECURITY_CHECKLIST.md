# Security Checklist

- [ ] Data classification and threat scope identified.
- [ ] Authentication and session/token lifecycle reviewed.
- [ ] Server-side authorization tested for roles and object ownership.
- [ ] Privileged operations have appropriate controls/audit.
- [ ] Input validation and output encoding reviewed.
- [ ] SQL injection, XSS, CSRF, SSRF, IDOR/BOLA, mass assignment considered.
- [ ] Rate limiting and resource exhaustion considered.
- [ ] File upload/download and storage access secured.
- [ ] Secrets excluded from code, logs, docs, and Project Sources.
- [ ] Sensitive data minimized, masked, retained, and deleted appropriately.
- [ ] Dependencies and CI/CD permissions reviewed.
- [ ] Production configuration, TLS, cookies, CORS, network access reviewed.
- [ ] Backups protected and recovery tested.
- [ ] Findings have severity, owner, remediation, retest, and residual-risk decision.

This checklist is not a certification or substitute for a scoped security assessment.
