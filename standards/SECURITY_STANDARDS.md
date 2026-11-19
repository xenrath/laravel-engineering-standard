# Application Security Standards

## 1. Risk-based baseline

Establish application criticality, data classification, public exposure, threat actors, and regulatory/contractual requirements. Use OWASP ASVS and OWASP Top 10/API Top 10 as references, selecting controls appropriate to risk rather than claiming blanket compliance.

## 2. Identity and access

- Use maintained framework-supported authentication.
- Protect password storage with approved password hashing.
- Consider MFA for privileged/high-risk access.
- Define session/token expiry, revocation, rotation, and recovery.
- Apply least privilege and deny-by-default where practical.
- Enforce object-level and function-level authorization on the server.
- Test both allowed and denied access, including cross-user/tenant attempts.
- Maintain an authorization matrix for meaningful roles/resources.

## 3. Input, output, and application vulnerabilities

Review SQL injection, XSS, CSRF, SSRF, IDOR/BOLA, broken access control, mass assignment, open redirects, path traversal, unsafe deserialization, command injection, and resource exhaustion. Validate input at trust boundaries and encode output for its context.

## 4. File handling

Validate size and actual content; do not trust filename or client MIME. Generate safe names, store private files outside public web root where appropriate, authorize downloads, prevent path traversal/executable uploads, and scan files where risk warrants.

## 5. Data and secrets

Minimize collection and retention. Classify sensitive fields. Encrypt in transit; assess encryption at rest and field-level encryption based on threat and requirements. Redact logs/exports. Store secrets in approved secret management/environment mechanisms. Rotate exposed secrets. Never commit `.env` or real credentials.

## 6. Configuration and infrastructure

Review debug mode, error pages, TLS, cookies, CORS, trusted hosts/proxies, headers, database exposure, filesystem permissions, service accounts, firewall/network boundaries, backup access, and production deployment permissions.

## 7. Dependencies and supply chain

Use maintained packages, lock dependencies, scan advisories, review licenses and transitive packages, protect CI credentials, and restrict workflow permissions. Establish a vulnerability triage and remediation process.

## 8. Verification

Use threat modeling, secure code review, SAST, dependency/secret scanning, DAST, focused penetration testing, and security regression tests according to risk. Tools are aids, not proof of security. Record findings, severity rationale, owner, remediation, retest evidence, and accepted residual risk.

## 9. Incident readiness

Define reporting channel, severity, containment, evidence preservation, credential rotation, recovery, communication, and post-incident review. Protect logs and forensic evidence.

## 10. External references

Use OWASP ASVS 5.0.0, OWASP Web Security Testing Guide, OWASP Top 10/API Security Top 10, and NIST SSDF as applicable. Record the version/date of the reference used.
