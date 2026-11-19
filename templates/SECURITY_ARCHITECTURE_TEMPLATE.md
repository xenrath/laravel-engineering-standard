# Security Architecture

```yaml
document_id: SECURITY_ARCHITECTURE
project: [PROJECT_NAME]
version: 1.0
document_status: Draft
owner: [OWNER]
last_updated: YYYY-MM-DD
source_commit: [COMMIT_OR_UNKNOWN]
```

## 1. Scope and risk context
[Application exposure, data classification, criticality, threat actors.]

## 2. Trust boundaries and data flows
[Diagram and external entry points.]

## 3. Identity and authentication
[Guards/providers, session/token lifecycle, MFA, recovery.]

## 4. Authorization model
[Roles, policies, ownership/tenant checks; link authorization matrix.]

## 5. Sensitive data and secrets
[Classification, storage, encryption, masking, rotation.]

## 6. Application controls
[Validation, output encoding, CSRF, rate limits, file controls, audit.]

## 7. Infrastructure controls
[TLS, network, service accounts, backups, monitoring.]

## 8. Threat model
| Threat | Asset/boundary | Attack path | Impact | Control | Verification |
|---|---|---|---|---|---|

## 9. Residual risks and exceptions
[Owner, mitigation, approval, expiry/review.]

## 10. Verification evidence
[ASVS/control mapping, tests, scans, review date.]
