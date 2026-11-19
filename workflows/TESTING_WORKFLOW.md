# Testing Workflow

## Steps
1. Convert acceptance criteria and risks into test cases.
2. Identify unit, feature, integration, API/contract, authorization, database, E2E, accessibility, performance, and security coverage as applicable.
3. Confirm isolated test environment and synthetic data; never point destructive tests at production.
4. Use factories and deterministic setup; fake external services where appropriate.
5. Run focused tests first, then relevant regression and broader suites.
6. Run formatting, static analysis, dependency checks, and frontend build where configured.
7. Investigate failures; do not silently skip or relabel flaky tests as passed.
8. Add regression tests for defects where practical.
9. Record exact commands, commit, environment, results, test counts if available, and gaps.
10. Map evidence to acceptance criteria and release gates.

## Status
Passed, Failed, Blocked, Not Run, Not Applicable. A test file existing is not evidence it passed.
