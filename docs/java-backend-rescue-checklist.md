# Java Backend Rescue Checklist

## First Hour

- Confirm the failure mode: latency, errors, data inconsistency, resource
  exhaustion, deploy regression, queue backlog, or customer-visible outage.
- Capture exact reproduction steps, affected endpoints/jobs, timestamps, request
  IDs, release versions, and traffic shape.
- Freeze assumptions until logs, metrics, traces, database state, and recent
  changes agree.

## Observability

- Check HTTP status/error rate by endpoint and client.
- Compare p50/p95/p99 latency before and after the suspected regression.
- Inspect JVM memory, GC pauses, thread pools, connection pools, and CPU.
- Trace database query count, slow SQL, lock waits, missing indexes, and N+1
  query patterns.
- Verify queue lag, retry storms, dead-letter messages, and idempotency keys.

## Common Java/Spring Boot Causes

- Blocking I/O inside request paths.
- Unbounded thread pools or executor saturation.
- Missing database indexes after feature growth.
- Inefficient ORM fetch plans and accidental N+1 queries.
- Cache stampedes, stale cache invalidation, or inconsistent TTLs.
- Retry loops without budget, jitter, or circuit breaking.
- Serialization overhead on large response objects.
- Memory pressure from large collections, file reads, or batch jobs.

## Fix Pattern

- Reproduce the issue locally or in staging with a focused test.
- Reduce blast radius: feature flag, traffic split, rollback, queue pause, or
  targeted rate limit.
- Patch the smallest failing path first.
- Add a regression test or a repeatable benchmark before broad refactoring.
- Document the root cause, customer impact, fix, and prevention rule.
