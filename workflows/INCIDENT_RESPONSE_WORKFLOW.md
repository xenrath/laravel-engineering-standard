# Incident Response Workflow

## 1. Purpose
Provide a repeatable response for security, availability, data integrity, and operational incidents. Adapt contacts and obligations to the organization.

## 2. Initial response
1. Record detection time, reporter, affected service, symptoms, and evidence.
2. Assign incident owner and severity.
3. Protect people, data, and critical operations.
4. Preserve relevant logs/evidence; avoid destructive troubleshooting.
5. Establish a communication channel and update cadence.

## 3. Triage
Assess scope, affected users/data, duration, exploitability, availability, integrity, confidentiality, dependencies, and ongoing risk.

## 4. Containment
Choose proportionate containment: disable vulnerable path, revoke credentials, isolate service, block abusive traffic, pause jobs/integrations, or fail over. Obtain approval where required; document actions and impact.

## 5. Eradication and recovery
Fix root cause, rotate exposed secrets, restore clean systems/data if needed, validate integrity, deploy through controlled release, and monitor recovery.

## 6. Communication and obligations
Notify internal owners and affected parties according to applicable policy, contract, and law. Do not speculate or disclose sensitive incident details unnecessarily.

## 7. Post-incident review
Document timeline, root cause, impact, response effectiveness, evidence gaps, corrective actions, owners, and due dates. Focus on system improvements, not blame.
