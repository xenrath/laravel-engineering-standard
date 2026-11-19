# API Engineering Standards

## 1. Contract-first thinking

Define consumers, use cases, authorization, request/response contracts, errors, and compatibility before implementation. Use OpenAPI where API size, external consumers, or collaboration justify it.

## 2. HTTP and resource conventions

- Use HTTP methods and status codes consistently.
- Keep route naming and resource nesting predictable.
- Avoid exposing internal database structure as a public contract without reason.
- Define API versioning/deprecation policy when breaking changes are possible.
- Use pagination for collections and bounded filtering/sorting.
- Validate and normalize all inputs server-side.

## 3. Authentication and authorization

Document supported mechanisms (session, Sanctum, Passport, OAuth/OIDC, service credentials, or other verified approach). Authorize every operation and resource. Enforce tenant/ownership boundaries server-side. Never assume possession of an object ID grants access.

## 4. Responses and errors

Define consistent success, validation, authentication, authorization, not-found, conflict, rate-limit, and server-error formats. Do not leak stack traces, SQL, secrets, or sensitive fields. Include correlation/request IDs where useful.

## 5. Reliability and abuse controls

Define rate limits, timeouts, idempotency for retryable writes, duplicate request behavior, payload limits, and external integration retry/backoff. Do not retry non-idempotent writes without a safe strategy.

## 6. Security

Apply TLS, least privilege, secure token storage/rotation, CORS restrictions, input validation, output filtering, logging redaction, and relevant OWASP API security controls. Protect against BOLA/IDOR, broken function-level authorization, excessive data exposure, mass assignment, SSRF, and resource exhaustion.

## 7. Documentation and tests

Maintain examples using synthetic data. Test contract shape, validation, authn/authz, ownership, pagination, errors, rate limiting, and backward compatibility. Update OpenAPI/API documentation when contracts change.
