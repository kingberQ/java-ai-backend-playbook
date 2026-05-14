# Java AI Backend Playbook

Public, non-confidential engineering notes for Java backend, AI automation, and
security-aware tooling work.

This repository intentionally contains no company source code. It documents the
kind of production problems I work on in proprietary Java systems and the
delivery process I use when helping remote teams.

## Focus Areas

- Java/Spring Boot backend rescue: latency, reliability, database bottlenecks,
  async job failures, memory pressure, and production debugging.
- LLM integration: model gateways, prompt/version control, cost limits,
  retry/rate-limit handling, audit logs, human review paths, and eval loops.
- Security-aware automation: private-key isolation, read-only risk analysis,
  webhook hardening, secret handling, and operational guardrails.
- Async remote delivery: scoped implementation sprints, written status updates,
  reproducible test cases, and handover docs.

## Documents

- [Java backend rescue checklist](docs/java-backend-rescue-checklist.md)
- [Production LLM integration checklist](docs/production-llm-integration-checklist.md)
- [Security-aware Web3/read-only tooling checklist](docs/security-aware-web3-tooling.md)
- [Remote contract delivery process](docs/remote-contract-delivery-process.md)

## Why This Exists

Most serious backend work happens in private company repositories. This repo is
a public substitute for those private codebases: it shows the engineering
standards, debugging process, and risk controls I use without exposing client or
employer IP.
