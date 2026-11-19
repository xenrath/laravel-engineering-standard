# Release and Deployment Workflow

## 1. Release scope
Record release identifier, commit/artifact, included changes, exclusions, known issues, target environment, release window, and approvers.

## 2. Readiness
- Acceptance criteria met.
- Required code review and CI checks passed.
- Security findings triaged.
- Dependencies and configuration reviewed.
- Database migration and backfill plan reviewed.
- Backup and recovery readiness verified.
- Monitoring, queue, scheduler, and storage impacts understood.
- Rollback/forward recovery and communication plan ready.

## 3. Approval
Production deployment requires explicit approval from the responsible owner. Confirm target, scope, migration, downtime, backup, rollback, and communication.

## 4. Deployment
Follow the environment-specific runbook and Laravel-version-matched guidance. Use reviewed artifacts and controlled commands. Do not run generic commands blindly.

## 5. Verification
Run health checks and critical smoke tests. Verify authentication, authorization, core workflows, database state, queue/scheduler, integrations, logs, and error rates.

## 6. Rollback/recovery
Define trigger, decision owner, application rollback, database compatibility, data-loss implications, backup restore, and communication. Database rollback may be unsafe after writes; forward recovery may be necessary.

## 7. Release report
Record actual deployed artifact/commit, environment, timestamps, migration actions, verification evidence, deviations, incidents, and follow-up.
