# Engineering Scenarios

These are common problems I investigate, not claims about specific clients or measured outcomes.

## An API slows down under load

I compare request timings, SQL execution, application logs, and external-service latency to locate the bottleneck. Depending on the cause, the fix may involve query changes, caching, smaller payloads, or better handling of slow providers. I check response times and failures again after the change.

## A legacy PHP system is hard to change

I trace the important code paths and dependencies before refactoring. I try to preserve existing behavior while isolating the parts that make changes risky. A complete rewrite needs a clear technical reason.

## MySQL performance gets worse as records grow

I inspect slow queries, execution plans, indexes, and the amount of data fetched. I also check how a proposed change affects writes and other queries, rather than optimizing a single request in isolation.

## A provider integration fails intermittently

I separate provider errors from local bugs, review sanitized logs, enforce timeouts, and handle retries carefully. With payments or other state-changing requests, duplicate execution is a specific risk to address.

For project responsibilities rather than illustrative scenarios, see [Selected projects](./SYSTEMS.md).
