# Security-Aware Web3 Tooling Checklist

## Scope

Prefer read-only analytics and risk tooling when operating across uncertain legal
or financial boundaries. Avoid custody, order routing, trading for users, token
issuance, and any flow that requires users to trust your private infrastructure
with funds.

## Read-Only Design

- No private keys.
- No token approvals.
- No transaction signing.
- No custody.
- No trade execution.
- Clear warnings when a quote or static check is not execution proof.

## Data Checks

- Token metadata and owner/admin controls.
- Liquidity availability across known pools.
- Buy/sell quote availability.
- Transfer tax, blacklist, pause, mint, and ownership signals when detectable.
- Verified source availability and proxy implementation checks.
- Recent event history and suspicious holder concentration.

## Operational Guardrails

- Use separate RPC keys per project.
- Rate-limit scans and cache expensive reads.
- Record source block numbers for reproducibility.
- Avoid exposing internal dashboards without authentication.
- Keep secrets in environment variables or a secret manager, never in command
  arguments or repository files.

## Communication

Do not market read-only checks as guaranteed honeypot detection or investment
advice. State the limits clearly and recommend wallet-level simulation or manual
review for high-risk assets.
