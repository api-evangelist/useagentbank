---
name: useagentbank-payout-flow
description: Create a fiat payout, then view the list of payouts and retrieve a specific payout.
api: openapi/useagentbank-openapi.json
operations:
- createPublicX402Payout
- listPublicX402Payouts
- getPublicX402Payout
generated: '2026-10-20'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/useagentbank-openapi.json ; every operationId checked against the contract
---

# useagentbank-payout-flow

Create a fiat payout, then view the list of payouts and retrieve a specific payout.

## Steps

1. 1. `createPublicX402Payout` – send a POST request with the required body fields and include the `SIGN-IN-WITH-X` header for authentication.
2. 2. `listPublicX402Payouts` – send a GET request with the `SIGN-IN-WITH-X` header to list payouts funded by the authenticated wallet.
3. 3. `getPublicX402Payout` – send a GET request to `/api/public/x402/payments/{flowId}` with the `SIGN-IN-WITH-X` header to retrieve a specific payout.

## Rules

- Authentication: include the `SIGN-IN-WITH-X` header (apiKey) in every request.
