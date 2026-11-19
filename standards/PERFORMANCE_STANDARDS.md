# Performance and Scalability Standards

## 1. Measure first

Establish baseline and target before optimization. Record environment, dataset, workload, measurement method, and result. Do not present local benchmark results as production performance.

## 2. Web and application performance

Review response time distribution (not only averages), throughput, error rate, memory, CPU, payload size, rendering, external service latency, and queue delay where relevant.

## 3. Laravel/database performance

Inspect N+1 queries, query count, eager loading, pagination, indexes, query plans, transaction duration, connection use, caching, and large data processing. Use chunking/cursors for large jobs where appropriate.

## 4. Caching

Define cache key, scope, TTL, invalidation, consistency, stampede prevention, and behavior on cache failure. Do not cache authorization-sensitive data across users/tenants without correct key isolation.

## 5. Queues and background work

Move suitable long-running work to queues. Define idempotency, retry/backoff, timeout, dead-letter/failed-job handling, monitoring, and capacity. Avoid unbounded queue growth.

## 6. Load and capacity

Use realistic, authorized test environments and representative synthetic data. Define workload profile, ramp-up, duration, success criteria, and stop conditions. Do not load-test production without explicit approval.

## 7. Optimization decision

Prioritize measured bottlenecks and business impact. Record trade-offs and re-measure after changes. Avoid speculative caching, premature microservices, or unnecessary infrastructure.
