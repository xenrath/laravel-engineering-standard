# Laravel Engineering Prompt Library

Use prompts inside the relevant application Project. Replace placeholders and provide access to evidence. Prompts do not replace inspection, approvals, or tests.

## 1. Project baseline assessment
```text
Assess [PROJECT_NAME] using current Project Sources and repository evidence if available.
Verify purpose, stack/versions, architecture, modules, database, security, tests,
CI/CD, deployment, operations, and documentation. Separate verified facts,
assumptions, unknowns, risks, and next actions. Do not modify code or data.
```

## 2. Requirements analysis
```text
Analyze [REQUIREMENT]. Identify problem, actors, business rules, functional and
non-functional requirements, permissions, data/API impact, edge cases,
dependencies, risks, and testable acceptance criteria. Assign stable IDs.
Mark assumptions and obtain owner decisions for unresolved business rules.
```

## 3. Legacy assessment
```text
Compare actual legacy behavior, code, schema, and workflows with current
requirements. Classify each capability Keep, Improve, Redesign, Remove, or New.
Explain evidence, migration impact, security risks, and acceptance criteria.
Do not copy legacy implementation blindly.
```

## 4. Architecture review
```text
Review [SCOPE] against requirements and current implementation. Evaluate
boundaries, dependencies, data ownership, integration failure handling,
security, reliability, performance, operability, and maintainability.
Identify evidence-backed issues and recommend the smallest effective change.
Record material decisions as ADRs.
```

## 5. Database review
```text
Review [TABLES/MODULE] using migrations, models, schema evidence, and queries.
Assess keys, constraints, relationships, indexes, normalization, transactions,
concurrency, migration safety, backfill, retention, privacy, and recovery.
Do not run destructive operations or change production data.
```

## 6. Authorization review
```text
Build or review the authorization matrix for [MODULE]. Map actor, role,
resource, action, ownership/tenant condition, policy enforcement, and negative
test. Identify IDOR/BOLA and privilege-escalation paths. Verify server-side
enforcement; UI visibility is not authorization.
```

## 7. API design/review
```text
Design/review [API USE CASE]: routes, methods, authn/authz, validation,
contracts, error format, pagination, filtering, rate limits, idempotency,
versioning, OpenAPI, and contract tests. Use synthetic examples only.
```

## 8. Feature implementation
```text
Implement [FEATURE] against approved requirements. Inspect current code,
callers, dependencies, and tests first. State scope and impact. Make the
smallest coherent change, preserve unrelated work, add tests, run relevant
checks, and report exact files/commands/results and unverified areas.
Obtain approval for destructive, production, breaking, or scope-expanding work.
```

## 9. Bug investigation
```text
Investigate [BUG] with reproduction steps and evidence. Compare expected and
actual behavior, establish root cause, affected components, security/data
impact, and regression risk. Do not guess. Fix within scope and add a regression
test where practical. Report actual validation.
```

## 10. Security review
```text
Perform a scoped security review of [AREA]. Review trust boundaries,
authentication, authorization, validation, output encoding, CSRF, SSRF,
file handling, sensitive data, logging, dependencies, CI permissions, and
production configuration as relevant. Map findings to suitable OWASP controls.
Report evidence, attack scenario, severity, remediation, and retest.
Do not claim full audit/compliance from partial evidence.
```

## 11. Performance investigation
```text
Investigate [PERFORMANCE ISSUE]. Establish measurements first. Inspect query
patterns, N+1, indexes/query plans, payload, cache, queues, external latency,
and resource limits. Separate measurements from hypotheses. Recommend a
measurable fix and define how it will be verified.
```

## 12. Testing plan
```text
Create a risk-based test plan for [CHANGE]. Map acceptance criteria to unit,
feature, integration, API/contract, authorization, database, E2E, accessibility,
security, and performance tests as relevant. Include negative paths and test
environment/data needs. Do not claim tests have run.
```

## 13. Code review
```text
Review this change set against requirements and project standards. Inspect the
full diff. Report only actionable findings with severity, evidence, impact,
and remediation. Check security, data integrity, compatibility, performance,
tests, dependencies, and documentation.
```

## 14. CI/CD design
```text
Design a proportionate CI/CD pipeline for [PROJECT/PLATFORM]. Include least
privilege, protected secrets, quality gates, tests, dependency/security scans,
build artifact, environment promotion, approval, deployment verification,
and failure recovery. Distinguish mandatory from optional checks.
```

## 15. Documentation synchronization
```text
Compare actual implementation evidence with Project Sources. Update only
documents affected by [CHANGE]. Keep status, source commit, dates, and
assumptions accurate. Do not change approval status without authorization.
List discrepancies and unresolved unknowns.
```

## 16. Release readiness
```text
Assess [RELEASE] for [ENVIRONMENT]. Review scope, tests, CI, dependencies,
security findings, migrations/backfills, backup/recovery, monitoring, queue,
scheduler, smoke tests, approvals, and rollback/forward recovery. Give Go/No-Go
with evidence and blockers. Do not deploy without explicit authorization.
```

## 17. Incident response
```text
Help triage [INCIDENT]. Establish timeline, scope, severity, affected assets,
ongoing risk, containment options, evidence preservation, communication,
recovery, and post-incident actions. Do not expose secrets or destroy evidence.
```

## 18. Project status
```text
Update project status from verified changes since [DATE/REPORT]. Separate
Planned, In Progress, Implemented, Tested, Verified, Blocked, and Released.
Include evidence, tests, risks, documentation changes, and next priorities.
Do not invent progress percentages.
```

## 19. Session handover
```text
Prepare a handover with context, objective, completed work, changed files,
branch/commit/working-tree state, decisions, exact test commands/results,
known issues, pending tasks, relevant sources, and one concrete next action.
Separate facts from assumptions. Exclude secrets and sensitive data.
```
