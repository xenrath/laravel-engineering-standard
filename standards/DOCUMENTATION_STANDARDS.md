# Documentation Standards and Governance

## 1. Documentation purpose

Documentation must help stakeholders understand, operate, change, test, and secure the system. Create documents when they have an owner and a practical use; avoid empty paperwork.

## 2. Naming and location

Use clear uppercase snake case for shared Markdown files, e.g. `SYSTEM_ARCHITECTURE.md`. Keep project documentation in the application repository under a documented location such as `/docs`. Keep templates in the master standard repository.

## 3. Metadata

Use consistent metadata:

```yaml
---
document_id: SYSTEM_ARCHITECTURE
project: PROJECT_NAME
version: 1.0
document_status: Draft
owner: TEAM_OR_ROLE
last_updated: YYYY-MM-DD
source_commit: COMMIT_OR_UNKNOWN
---
```

`Current` is an applicability designation, not a lifecycle status. Track approval separately if needed.

## 4. Lifecycle and review

Draft → In Review → Approved → Superseded/Archived. Only authorized owners approve documents. Review documents after material architecture, schema, security, API, or operational changes and on a cadence appropriate to risk.

## 5. Evidence and traceability

Link requirements to modules, ADRs, tests, and releases where useful. Identify source commit, inspected environment, and date for implementation-sensitive claims. Mark assumptions and unknowns.

## 6. Change control

Update impacted documentation in the same change set where practical. Record significant decisions in ADRs and release-visible changes in changelog/release notes. Do not silently change approved business rules.

## 7. Project Sources curation

ChatGPT Project Sources are selected reference material, not the canonical version-control system. Keep canonical documents in Git. Add approved, current, non-sensitive references to Project Sources; remove stale duplicates through the user's supported file/project controls. Never upload secrets or unnecessary production data.

## 8. Quality review

Check links, filenames, metadata, diagrams, terminology, status, and consistency with code/tests. Avoid claims that exceed available evidence.
