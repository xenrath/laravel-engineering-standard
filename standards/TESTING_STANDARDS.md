# Testing and Quality Assurance Standards

## 1. Test strategy

Derive tests from requirements, acceptance criteria, risks, and architecture boundaries. Use a balanced test pyramid; do not rely exclusively on slow end-to-end tests or shallow unit tests.

## 2. Test levels

- Unit: isolated domain/business logic.
- Feature: Laravel HTTP/application behavior.
- Integration: database, queue, storage, and service boundaries.
- API/contract: request/response compatibility.
- Authorization: role, object ownership, tenant boundaries.
- E2E/browser: critical end-user journeys.
- Regression: previously working behavior affected by changes.
- Accessibility: keyboard, semantics, contrast, assistive technology.
- Performance: load, stress, soak, and capacity as required.
- Security: focused abuse cases and security control verification.

## 3. Test quality

Tests should be deterministic, isolated, readable, and meaningful. Use factories and synthetic data. Avoid production data and uncontrolled external dependencies. Fake external systems where suitable; maintain separate contract/integration tests when real integration behavior matters.

## 4. Coverage

Do not use one universal coverage percentage as the sole quality measure. Set project targets for critical modules and risk areas. Coverage indicates execution, not assertion quality or correctness.

## 5. CI requirements

Run appropriate formatting, static analysis, dependency/security checks, tests, and builds in CI. Define blocking and advisory checks. Protect release branches and production secrets. Preserve test artifacts and useful failure output without exposing secrets.

## 6. Failure management

Do not silently skip flaky or failing tests. Track flakiness, owner, cause, temporary quarantine rationale, and removal deadline. A quarantined test does not count as passed.

## 7. Evidence

Record commit, environment, command, test suite, counts if available, result, date, and known gaps. Distinguish Passed, Failed, Blocked, Not Run, and Not Applicable.
