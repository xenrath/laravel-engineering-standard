# Database Engineering Standards

## 1. Design

- Model entities and relationships from business rules, not only UI forms.
- Define primary keys, foreign keys, uniqueness, nullability, defaults, check constraints where supported, and deletion behavior.
- Normalize to protect integrity; denormalize only for a justified read/performance need with consistency strategy.
- Define monetary precision, timezone/date semantics, status representation, and identifier strategy explicitly.
- Document ownership, retention, sensitivity, and lifecycle of important data.

## 2. Laravel migrations

- Use migrations as reviewed, version-controlled schema changes.
- Keep migrations deterministic and safe to run in deployment order.
- Do not edit historical migrations that have already been applied in shared environments; create forward migrations unless the team has an explicit pre-release policy.
- Avoid destructive or long-locking operations in a single release on large/critical tables.
- Consider expand-and-contract: add compatible schema, deploy compatible code, backfill, switch reads/writes, then remove obsolete schema in a later release.
- Review generated SQL and engine-specific behavior for high-risk migrations.
- Never run destructive migration commands against production without explicit approval and recovery plan.

## 3. Data access and performance

- Avoid N+1 and unbounded queries.
- Use pagination or chunking for large datasets.
- Add indexes based on query patterns, selectivity, write cost, and measured plans.
- Avoid indexing every column.
- Use parameter binding for raw queries.
- Review lock scope and transaction duration.
- Avoid network calls or long CPU work inside database transactions.

## 4. Transactions and concurrency

Identify business operations requiring atomicity. Consider optimistic version checks or pessimistic locks for contested updates. Make retry behavior safe. Prevent duplicate processing with unique constraints/idempotency keys where appropriate. Do not rely solely on application-level checks for invariants that can be enforced by the database.

## 5. Data migration and backfill

For data transformations, define source/target mapping, validation rules, batching, idempotency, error handling, reconciliation counts, restart behavior, rollback/forward recovery, and audit evidence. Test with sanitized representative data. Protect personal data during extraction and transfer.

## 6. Backup and recovery

Define database and file backup coverage, encryption, offsite copies, retention, access control, restore tests, RPO, RTO, and recovery owner. A successful backup job is not proof of recoverability; perform restore exercises.

## 7. Environment separation

Never use production credentials or data in local/test environments by default. Use sanitized fixtures or approved masking. Confirm environment before running SQL or migrations. Test destructive commands only against disposable test databases.

## 8. Documentation

Maintain `DATABASE_DESIGN.md` and `DATA_DICTIONARY.md` for material schemas. Record schema source, commit/date, engine/version, relationships, constraints, indexes, sensitive fields, and known discrepancies. Distinguish migration-defined schema from live database observations.
