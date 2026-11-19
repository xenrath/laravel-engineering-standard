# Deployment Guide

```yaml
document_id: DEPLOYMENT_GUIDE
project: [PROJECT_NAME]
version: 1.0
document_status: Draft
owner: [OWNER]
last_updated: YYYY-MM-DD
source_commit: [COMMIT_OR_UNKNOWN]
```

## 1. Environment and topology
[Hosting, runtime, web server, database, cache, queue, storage, DNS/TLS.]

## 2. Prerequisites
[PHP extensions/version, Composer, Node/build tools, services, permissions.]

## 3. Configuration
[List variable names and descriptions only; never include real values/secrets.]

## 4. Build and release artifact
[Reproducible commands and artifact provenance.]

## 5. Deployment procedure
[Environment-specific, reviewed steps. Include maintenance/downtime.]

## 6. Database migration
[Reviewed migration plan, compatibility, backup, backfill.]

## 7. Queue, scheduler, cache, and storage
[Worker restart, scheduler, cache rebuild, storage permissions.]

## 8. Smoke tests and health checks
[Critical routes/workflows and expected outcomes.]

## 9. Rollback/recovery
[Trigger, owner, application rollback, database recovery limits.]

## 10. Post-deployment evidence
[Commit/artifact, environment, timestamp, checks, incidents.]
