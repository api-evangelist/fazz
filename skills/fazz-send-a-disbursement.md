---
name: Send a disbursement with Fazz
description: Pay out funds from your Fazz Business account to a recipient via bank transfer, then confirm completion.
api: openapi/fazz-openapi.yml
operations: [createDisbursement, getDisbursement, listDisbursements]
---

# Send a disbursement with Fazz

Send a payout from your Fazz Business SGD balance to a recipient bank account.

## Auth
HTTP Basic (API key : secret key), HTTPS only.

## Steps
1. `createDisbursement` — POST `/disbursements` with `amount`, `currency` (SGD), a unique `referenceId`, and `disbursementMethod` (destination bank code, account number, account holder name).
2. Confirm completion via the signed `disbursement` callback (`X-Xfers-Signature`, HMAC-SHA256) or by polling `getDisbursement` — GET `/disbursements/{disbursementId}` — until `status` is `completed` (may pass through `processing`; `failed` on error).
3. Reconcile with `listDisbursements` — GET `/disbursements` — filtering by `filter[status]` / `filter[referenceId]`.

## Rules
- **Idempotency:** reuse the same `referenceId` on retries so a payout is never sent twice — this API moves real money.
- Watch for `TXN0001` (insufficient funds), `TXN0003`/`TXN0004` (limit exceeded), `MA-001` (unverified account) in `errors/fazz-error-codes.yml`.
- High-consequence: agentic use should default to human-in-the-loop (see `agentic-access/fazz-agentic-access.yml`).
