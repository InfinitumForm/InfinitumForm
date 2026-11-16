# How I Work on Backend Systems

My main work is in PHP applications, WordPress, APIs, MySQL, and Linux-based infrastructure. I handle both new development and existing systems that have become slow, difficult to change, or unreliable.

## Start with the actual problem

Before changing architecture, I inspect the code path, database queries, external dependencies, logs, and server configuration. A slow page does not automatically need a new framework. It may need a better query, a smaller payload, or a fix to an external API call.

## Keep changes proportionate

I prefer focused fixes where they solve the problem. Larger refactoring makes sense when tightly coupled code, duplicated logic, or an unsuitable data model keeps causing the same failures. I avoid replacing working components just to introduce a newer stack.

## Pay attention to boundaries

- **Database access:** query plans, indexes, expensive reads, and write contention.
- **External services:** authentication, timeouts, retries, error handling, and logging.
- **Caching:** cache contents, expiration, and invalidation.
- **Security:** input validation, permissions, secrets, and sensitive data.
- **Deployment:** configuration differences, rollback options, and production diagnostics.

## Verify the result

I compare behavior before and after a change using measurements available in the project. Performance improvements also need correctness checks: a faster response is not useful if it returns stale or incomplete data.

[Selected projects](./SYSTEMS.md) | [Engineering scenarios](./CASES.md)
