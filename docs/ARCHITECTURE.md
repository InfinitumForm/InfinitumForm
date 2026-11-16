# How I Work on Backend Systems

My main work is in PHP applications, WordPress, APIs, MySQL, and Linux-based infrastructure. I handle both new development and existing systems that have become slow, difficult to change, or unreliable.

## Start with the actual problem

Before changing architecture, I inspect the code path, database queries, external dependencies, logs, and server configuration. A slow page does not automatically need a new framework. It may need a better query, a smaller payload, or a fix to an external API call.

## Keep changes proportionate

I prefer focused fixes where they solve the problem. Larger refactoring makes sense when tightly coupled code, duplicated logic, or an unsuitable data model keeps causing the same failures. I avoid replacing working components just to introduce a newer stack.

## Pay attention to boundaries

The areas I check most closely are:

- **Database access:** query plans, indexes, expensive reads, and write contention.
- **External services:** authentication, timeouts, retries, error handling, and logging.
- **Caching:** what is cached, when it expires, and how stale data is invalidated.
- **Security:** input validation, permissions, secrets, and sensitive data handling.
- **Deployment:** configuration differences, rollback options, and production diagnostics.

## Verify the result

I compare behavior before and after a change, using measurements available in the project. Performance work should include correctness checks: a faster response is not an improvement if it returns stale or incomplete data.

For examples of systems I have worked on, see [Systems](./SYSTEMS.md). For common debugging situations, see [Engineering Cases](./CASES.md).
