# Remote Contract Delivery Process

## Discovery

- Identify the business problem, existing codebase constraints, and deadline.
- Convert vague requests into a short written scope with inputs, outputs, and
  non-goals.
- Ask for logs, traces, database schema, API examples, and deployment details
  before changing code.

## Implementation Sprint

- Start with a small branch or isolated proof of concept.
- Keep changes reviewable and scoped to the agreed problem.
- Send short written updates with what changed, what is blocked, and what will
  happen next.
- Prefer tests, scripts, and reproducible commands over verbal explanation.

## Handover

- Provide the final diff summary, setup steps, test commands, deployment notes,
  and known limitations.
- Document new environment variables and operational dashboards.
- Leave rollback instructions for production-facing changes.

## Retainer Work

- Maintain a visible backlog.
- Batch non-urgent work into weekly delivery windows.
- Reserve emergency time for production incidents.
- Track recurring issues and convert them into prevention tasks.
