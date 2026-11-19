# Development Workflow

## 1. Intake
Establish desired outcome, scope, exclusions, acceptance criteria, dependencies, and risk.

## 2. Inspect
Check repository branch/status/diff, relevant routes, controllers, requests, policies, models, services/actions, jobs/events, frontend, migrations, tests, and configuration. Preserve unrelated user changes.

## 3. Assess impact
Consider business behavior, authorization, schema/data, API compatibility, concurrency, integrations, performance, deployment, and documentation.

## 4. Plan
For medium/high-risk work, list files/components, intended behavior, tests, migration plan, security concerns, and rollout. Obtain approval for destructive, production, breaking, or scope-expanding changes.

## 5. Implement
Make the smallest coherent change. Follow project conventions and supported Laravel APIs. Add tests with behavior changes. Avoid unrelated refactoring and unreviewed dependencies.

## 6. Review
Inspect diff for correctness, authorization, validation, data integrity, error handling, secrets, performance, compatibility, and maintainability.

## 7. Validate
Run relevant syntax, formatting, static analysis, tests, build, and migration checks in a safe environment. Record exact commands and results.

## 8. Document
Update only impacted requirements, architecture, database, security, API, status, changelog, ADR, and issue records.

## 9. Report
Summarize outcome, files changed, actual checks, risks/unverified areas, docs updated, and next action.
