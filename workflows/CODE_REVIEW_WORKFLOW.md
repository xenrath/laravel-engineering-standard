# Code Review Workflow

## Inputs
Pull request/change set, linked requirements, acceptance criteria, relevant architecture and tests.

## Steps
1. Confirm scope and inspect full diff, including generated/configuration files.
2. Verify requirement alignment and absence of unrelated changes.
3. Review correctness, edge cases, readability, maintainability, and compatibility.
4. Review authorization, ownership/tenant isolation, validation, output encoding, secrets, file handling, and logging.
5. Review database constraints, migration safety, transaction/concurrency, and data impact.
6. Review query performance, N+1, unbounded operations, queue/retry behavior, and external failure handling.
7. Review tests and whether they assert meaningful outcomes, including negative authorization paths.
8. Check dependencies, licenses, advisories, lockfile, CI, and deployment/configuration impact.
9. Classify findings: Blocker, Major, Minor, Suggestion. Findings must include evidence and actionable remediation.
10. Verify fixes and record review outcome.

## Exit criteria
No unresolved blocker/major finding without explicit risk acceptance; required tests and approvals are recorded. Review is not a substitute for automated testing.
