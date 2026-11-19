# Database Design

```yaml
document_id: DATABASE_DESIGN
project: [PROJECT_NAME]
version: 1.0
document_status: Draft
owner: [OWNER]
last_updated: YYYY-MM-DD
source_commit: [COMMIT_OR_UNKNOWN]
```

## 1. Scope and evidence
[Migration files, schema introspection, models, engine/version, commit/date. State whether live DB was inspected.]

## 2. Conventions
[Keys, naming, timestamps, soft deletes, precision, timezone, statuses.]

## 3. ERD
```mermaid
erDiagram
    PARENT ||--o{ CHILD : contains
```

## 4. Table inventory and definitions
| Table | Purpose | PK | Relationships | Source |
|---|---|---|---|---|

For each table, document columns, types, nullability, defaults, constraints, indexes, and deletion behavior.

## 5. Integrity and business invariants
| Invariant | Enforced by DB/application | Test |
|---|---|---|

## 6. Query and index strategy
[Critical access patterns, query plans, measured evidence.]

## 7. Transactions and concurrency
[Atomic operations, locks, idempotency, race conditions.]

## 8. Migration and backfill plan
[Compatibility, batching, expand/contract, downtime, recovery.]

## 9. Data lifecycle and protection
[Classification, retention, archival, deletion, backup, restore.]

## 10. Known gaps and validation checklist
[Discrepancies, unresolved issues, schema verification.]
