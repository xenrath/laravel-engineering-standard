# Laravel and PHP Coding Standards

## 1. Version baseline

Confirm PHP and Laravel versions from Composer constraints/lockfile and runtime/deployment evidence. Use version-matched documentation. Do not copy APIs or configuration from a newer major version without compatibility verification.

## 2. PHP quality

- Follow the project's formatter and coding standard (for example, PSR-12 where adopted).
- Use meaningful names, typed signatures, explicit return types where practical, and narrow responsibilities.
- Handle exceptions intentionally; do not swallow errors or expose stack traces to users.
- Avoid global state and hidden side effects.
- Document non-obvious business constraints and public extension points.
- Prefer immutable/value objects when they simplify correctness, not as ceremony.

## 3. Laravel conventions

- Keep route definitions readable and group middleware deliberately.
- Keep controllers focused on HTTP orchestration.
- Validate requests at a clear boundary, commonly Form Requests.
- Authorize server-side using policies/gates/middleware or explicit domain authorization.
- Define Eloquent relationships and casts accurately.
- Avoid business rules hidden in views, model observers, or event listeners without clear ownership.
- Use service/action classes when a workflow has meaningful complexity or reuse.
- Use API Resources or an explicit response contract for APIs.
- Use dependency injection and the service container appropriately.
- Keep configuration in config files; do not call `env()` throughout application code.
- Avoid mass assignment exposure; define fillable/guarded behavior deliberately.

## 4. Database access

- Avoid N+1 queries through deliberate eager loading.
- Select only needed columns where useful.
- Paginate unbounded result sets.
- Avoid unsafe raw SQL; bind parameters.
- Review query plans for critical/high-volume paths.
- Use transactions for multi-step atomic changes.
- Define concurrency and idempotency behavior for operations vulnerable to duplicate requests.

## 5. Queues, events, and scheduling

- Jobs should be retry-safe and idempotent where possible.
- Set timeout, retry, backoff, and failure handling intentionally.
- Avoid serializing large or stale model state unnecessarily.
- Use unique/overlap prevention for scheduled work when needed.
- Define monitoring and operational ownership for failed jobs and scheduled tasks.
- Do not assume event dispatch timing is safe around database transactions; use after-commit behavior where appropriate.

## 6. Files and notifications

- Authorize uploads and downloads.
- Validate file size and actual content, generate server-side names, and store private files privately.
- Do not trust client filenames or MIME declarations.
- Avoid sending sensitive data through notifications or logs.
- Handle delivery failure and duplicate notification risk.

## 7. Exceptions and logging

- Return safe user-facing errors.
- Log actionable context with correlation identifiers where available.
- Redact secrets and sensitive personal data.
- Avoid logging entire request bodies by default.
- Preserve useful exception context without leaking internal implementation details.

## 8. Dependencies

Before adding/updating a package, check PHP/Laravel compatibility, maintenance activity, release history, security advisories, license, transitive dependencies, and whether native framework features suffice. Commit lockfile changes. Avoid broad updates mixed with unrelated feature changes.

## 9. Code review expectations

Review correctness, authorization, validation, data integrity, failure handling, performance, readability, tests, migration safety, and documentation. See `CODE_REVIEW_WORKFLOW.md` and quality gates.

## 10. Exceptions

Record deviations from project conventions with rationale, impact, owner, and review date.
