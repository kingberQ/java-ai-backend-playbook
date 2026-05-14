# Production LLM Integration Checklist

## Architecture

- Put model access behind a service boundary instead of calling providers from
  random business code.
- Store prompts, model names, temperature, max tokens, and tool schemas as
  versioned configuration.
- Keep request/response audit logs with redaction for secrets and personal data.
- Add provider failover only when product behavior remains acceptable with the
  fallback model.

## Reliability

- Use request timeouts, retry budgets, exponential backoff, and circuit breakers.
- Separate synchronous user flows from long-running AI jobs.
- Make expensive jobs idempotent with deterministic job keys.
- Persist intermediate state so retries do not duplicate external side effects.

## Cost Control

- Track token usage per feature, tenant, user, and job type.
- Add hard monthly and per-request limits.
- Cache deterministic or near-deterministic outputs.
- Use smaller models for extraction, classification, and formatting before
  escalating to stronger models.

## Safety

- Treat model output as untrusted data.
- Never execute generated code, shell commands, SQL, or financial actions without
  explicit validation and authorization.
- Validate JSON output with schemas and reject malformed data.
- Add human review for irreversible actions.

## Evaluation

- Keep a small golden dataset for common and high-risk cases.
- Run evals before prompt/model changes.
- Track false positives, false negatives, latency, and cost, not only subjective
  answer quality.
