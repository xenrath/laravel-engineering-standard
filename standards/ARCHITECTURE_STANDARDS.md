# Architecture Standards

## 1. Objective and applicability

Define maintainable architecture decisions for Laravel applications. Apply proportionately; a small CRUD application does not need the same architecture artifacts as a multi-domain, high-criticality system.

## 2. Architecture principles

- Start from business capabilities, requirements, and quality attributes.
- Define clear module responsibilities and dependency direction.
- Keep business rules independent of transport/UI where practical.
- Separate infrastructure concerns when doing so improves testability or change isolation.
- Prefer a modular monolith unless independently deployable services solve a real organizational or technical need.
- Avoid premature abstraction and pattern adoption without measurable benefit.
- Make security, observability, failure handling, and operability architectural concerns.

## 3. Required design views

For medium/high complexity systems, document:
- System context and external actors.
- Container/runtime/deployment view.
- Component/module responsibilities.
- Data ownership and key relationships.
- Integration and trust boundaries.
- Authentication and authorization flows.
- Critical workflows and failure paths.
- Quality attributes and constraints.

Use C4-style context/container/component views where useful; diagrams must reflect verified design.

## 4. Laravel application boundaries

Document the responsibility of routes/controllers, requests, policies, models, services/actions, jobs/events, repositories (if used), integrations, and infrastructure. Do not mandate a universal folder structure. Define dependency rules for the chosen architecture and prevent business logic from being duplicated across controllers, jobs, and commands.

## 5. Architecture decisions

Record material choices in ADRs, including context, options, decision, consequences, status, owner, and date. Revisit decisions when constraints materially change. Do not silently rewrite accepted decisions.

## 6. Integration resilience

For external calls, define timeout, retry policy, backoff, idempotency, error mapping, rate limits, authentication, observability, and fallback behavior. Avoid retrying non-idempotent operations blindly. Use circuit breakers only where justified by failure patterns and operational needs.

## 7. Cross-cutting concerns

Define approaches for authentication, authorization, validation, logging, audit, caching, queues, file storage, notifications, configuration, exception handling, and localization/timezone where relevant.

## 8. Quality attributes

Set measurable targets where meaningful: availability, response latency, throughput, data durability, recovery, accessibility, security verification, and maintainability. Record measurement method and environment.

## 9. Architecture review triggers

Review architecture when introducing a new bounded module, external integration, sensitive data class, authorization model, major database change, queue/cache infrastructure, multi-tenancy, or deployment topology change.

## 10. Anti-patterns

Avoid god controllers/models, duplicated business rules, circular dependencies, generic repositories with no value, direct infrastructure calls scattered through business logic, unbounded synchronous work, hidden side effects, and architecture diagrams that do not match the code.
