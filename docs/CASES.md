# Engineering Cases

These are examples of the kinds of problems I investigate. They describe my approach, **not** individual client case studies or measured outcomes.

## An API becomes slow during busy periods

I check which requests are slowing down, whether the delay comes from application code, SQL queries, or external providers, and whether errors correlate with traffic. I then address the bottleneck: query changes, caching, controlled concurrency, or better handling of slow external calls. I measure response time and error rates again after the change.

## A legacy PHP application is difficult to maintain

I map the important flows and dependencies before refactoring. I isolate changes into manageable pieces, preserve existing behavior, and add checks where practical. A full rewrite is a last resort, not the starting point.

## MySQL queries degrade as data grows

I examine the slow queries and execution plans, review indexes, and check whether the application fetches more data than it needs. Changes are tested against realistic data volumes, including their effect on writes and other queries.

## A third-party integration fails intermittently

I distinguish provider failures from local bugs. I inspect request and response logs without exposing sensitive data, set explicit timeouts, handle retries carefully, and ensure one failed provider does not unnecessarily break unrelated operations. For payments and other state-changing requests, I pay particular attention to duplicate operations.

These examples are intentionally general. Project-specific responsibilities are listed in [Systems](./SYSTEMS.md).
