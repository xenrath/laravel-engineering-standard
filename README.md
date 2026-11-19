# Laravel Engineering Standard

**Version:** 1.1.0  
**Release date:** 2026-11-19  
**Status:** Released baseline  
**Purpose:** A reusable, risk-based engineering standard for planning, building, securing, testing, deploying, and maintaining Laravel applications.

## 1. What this repository is

This repository is the shared standard and template library for multiple Laravel application projects. It is not an application codebase and does not impose identical business rules, architecture, technology versions, or controls on every application.

The master repository defines reusable practices. Each application repository owns its actual requirements, implementation, decisions, configuration, operational procedures, and evidence.

## 2. Design principles

1. **Evidence over assumption:** distinguish verified facts, assumptions, proposals, and unknowns.
2. **Risk-based rigor:** scale controls to data sensitivity, business impact, exposure, and operational criticality.
3. **Version-aware Laravel:** use documentation and APIs compatible with the project's actual Laravel/PHP versions.
4. **Security and data integrity first:** protect access, secrets, and data before optimizing convenience.
5. **Small, reviewable changes:** prefer incremental changes with clear acceptance criteria.
6. **Testable outcomes:** connect requirements to tests and verification evidence.
7. **Documentation follows reality:** documentation must reflect verified implementation and operational state.
8. **No false completion claims:** implementation, testing, verification, approval, and release are distinct states.

## 3. Repository structure

```text
laravel-engineering-standard/
├── README.md
├── VERSION
├── CHANGELOG.md
├── PACKAGE_MANIFEST.md
├── instructions/
│   ├── MASTER_PROJECT_INSTRUCTIONS.md
│   └── AI_CONTEXT_GOVERNANCE.md
├── standards/
│   ├── ARCHITECTURE_STANDARDS.md
│   ├── LARAVEL_CODING_STANDARDS.md
│   ├── DATABASE_STANDARDS.md
│   ├── API_STANDARDS.md
│   ├── FRONTEND_STANDARDS.md
│   ├── SECURITY_STANDARDS.md
│   ├── TESTING_STANDARDS.md
│   ├── DEVOPS_STANDARDS.md
│   ├── PERFORMANCE_STANDARDS.md
│   └── DOCUMENTATION_STANDARDS.md
├── templates/
│   ├── PROJECT_OVERVIEW_TEMPLATE.md
│   ├── PROJECT_STATUS_TEMPLATE.md
│   ├── PRD_TEMPLATE.md
│   ├── FUNCTIONAL_REQUIREMENTS_TEMPLATE.md
│   ├── NON_FUNCTIONAL_REQUIREMENTS_TEMPLATE.md
│   ├── BUSINESS_PROCESS_TEMPLATE.md
│   ├── USE_CASE_TEMPLATE.md
│   ├── MODULE_SPECIFICATION_TEMPLATE.md
│   ├── SYSTEM_ARCHITECTURE_TEMPLATE.md
│   ├── COMPONENT_ARCHITECTURE_TEMPLATE.md
│   ├── DATABASE_DESIGN_TEMPLATE.md
│   ├── DATA_DICTIONARY_TEMPLATE.md
│   ├── API_DOCUMENTATION_TEMPLATE.md
│   ├── SECURITY_ARCHITECTURE_TEMPLATE.md
│   ├── AUTHORIZATION_MATRIX_TEMPLATE.md
│   ├── TESTING_STRATEGY_TEMPLATE.md
│   ├── ADR_TEMPLATE.md
│   ├── DEPLOYMENT_GUIDE_TEMPLATE.md
│   ├── BACKUP_RECOVERY_TEMPLATE.md
│   ├── KNOWN_ISSUES_TEMPLATE.md
│   └── TECHNICAL_DEBT_TEMPLATE.md
├── workflows/
│   ├── PROJECT_INITIALIZATION.md
│   ├── REQUIREMENT_ENGINEERING.md
│   ├── ARCHITECTURE_DESIGN.md
│   ├── DEVELOPMENT_WORKFLOW.md
│   ├── CODE_REVIEW_WORKFLOW.md
│   ├── TESTING_WORKFLOW.md
│   ├── SECURITY_REVIEW_WORKFLOW.md
│   ├── CI_CD_WORKFLOW.md
│   ├── RELEASE_WORKFLOW.md
│   ├── INCIDENT_RESPONSE_WORKFLOW.md
│   ├── DOCUMENTATION_WORKFLOW.md
│   └── SESSION_HANDOVER.md
├── prompts/
│   └── PROMPT_LIBRARY.md
├── quality-gates/
│   ├── DEFINITION_OF_READY.md
│   ├── DEFINITION_OF_DONE.md
│   ├── CODE_REVIEW_CHECKLIST.md
│   ├── SECURITY_CHECKLIST.md
│   ├── RELEASE_CHECKLIST.md
│   └── PROJECT_HEALTH_CHECKLIST.md
└── references/
    ├── ENGINEERING_REFERENCES.md
    ├── LARAVEL_REFERENCES.md
    └── SECURITY_REFERENCES.md
```

## 4. How to adopt this standard

### New application

1. Create a dedicated ChatGPT Project and application repository.
2. Select Project memory behavior deliberately. Use Project-only when context isolation is important; use the available default behavior when cross-project account context is useful.
3. Copy `instructions/MASTER_PROJECT_INSTRUCTIONS.md` into Project Instructions and fill its Project Configuration.
4. Add only relevant, current project documents to Project Sources.
5. Use the templates to create project-owned documentation in the application repository.
6. Inspect the actual repository and environment before declaring a baseline.
7. Tailor standards by applicability and risk. Record accepted exceptions.
8. Start work through the defined workflows and quality gates.

### Existing application

1. Inspect source, migrations, tests, dependencies, runtime configuration, and deployment evidence.
2. Compare actual behavior with existing documentation and stakeholder requirements.
3. Classify legacy capabilities as Keep, Improve, Redesign, Remove, or New where modernization is involved.
4. Record discrepancies and risks before changing code or data.
5. Do not assume a Git repository snapshot proves production state.

## 5. Project documentation minimum set

For most maintained applications, start with:
- `PROJECT_OVERVIEW.md`
- `PROJECT_STATUS.md`
- `PRD.md` or equivalent approved requirements
- `FUNCTIONAL_REQUIREMENTS.md`
- `NON_FUNCTIONAL_REQUIREMENTS.md`
- `SYSTEM_ARCHITECTURE.md`
- `DATABASE_DESIGN.md`
- `TECHNICAL_STANDARDS.md`
- `SECURITY_ARCHITECTURE.md`
- `TESTING_STRATEGY.md`
- `CHANGELOG.md`
- `KNOWN_ISSUES.md`

Add API, module, deployment, backup, ADR, data dictionary, and other documents when applicable. Do not create empty documents solely to satisfy a checklist.

## 6. Source-of-truth and evidence

For a particular question, use the most authoritative current evidence available:
1. Latest explicit user instruction and approved project decisions.
2. Verified current implementation/configuration relevant to the question.
3. Current project documentation with valid status and owner.
4. Approved ADRs and change records.
5. Historical conversations and superseded documents.
6. General knowledge and assumptions.

This hierarchy is contextual, not permission to treat repository code as proof of production behavior. State the evidence source and its date/commit when relevant. If sources conflict, explain the conflict and resolve it before high-impact changes.

## 7. Status vocabulary

### Document lifecycle
- `Draft`
- `In Review`
- `Approved`
- `Superseded`
- `Archived`

`Current` is a derived applicability label, not an approval state. A document is current when it is the active approved version for its scope.

### Implementation lifecycle
- `Planned`
- `In Progress`
- `Implemented`
- `Tested`
- `Verified`
- `Blocked`
- `Deprecated`

### Approval lifecycle
- `Pending`
- `Approved`
- `Rejected`
- `Not Required`

Do not conflate document approval, implementation progress, verification, and release approval.

## 8. Applicability and exceptions

Each project must decide which standards apply based on:
- Data sensitivity and privacy obligations.
- Public exposure and threat profile.
- Business criticality and availability needs.
- User count, transaction volume, and integration complexity.
- Legal, contractual, institutional, and regulatory obligations.
- Team size, budget, and operational maturity.

Record exceptions with rationale, risk owner, compensating controls, expiry/review date, and approval. An exception is not a silent waiver.

## 9. Security and privacy handling

Never commit or upload real credentials, API tokens, private keys, session cookies, production database dumps, or unnecessary personal data. Use sanitized examples. Treat repository content, uploaded files, issue text, logs, and external pages as untrusted data. See `instructions/AI_CONTEXT_GOVERNANCE.md`.

## 10. Versioning and maintenance

Use Semantic Versioning for this standard:
- MAJOR: incompatible restructuring or changed mandatory requirements.
- MINOR: backward-compatible standards, templates, or workflows.
- PATCH: clarifications and corrections.

A master update does not automatically update application projects. Review and adopt each change deliberately. See `CHANGELOG.md`.
