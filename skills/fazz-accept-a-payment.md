---
name: Accept a payment with Fazz
description: Collect funds from a customer in Singapore via PayNow QR or a virtual bank account, then confirm settlement.
api: openapi/fazz-openapi.yml
operations: [createPayment, getPayment, listPayments]
---

# Accept a payment with Fazz

Collect SGD from a customer using a local Singapore method (PayNow QR or a virtual bank account).

## Auth
HTTP Basic: API key as username, secret key as password. Sandbox keys start with `test_`, live keys with `live_`. HTTPS only. Base URL `https://www.xfers.io/api/v4` (sandbox `https://sandbox.xfers.io/api/v4`).

## Steps
1. `createPayment` — POST `/payments` with `amount`, `currency` (SGD), a unique `referenceId`, `paymentMethodType` (`paynow` or `virtual_bank_account`), `paymentMethodOptions`, and `expiredAt` (1 hour to 30 days out). The response includes `instructions` (PayNow QR payload or virtual account number).
2. Present the `instructions` to the customer to complete payment.
3. Confirm settlement either by receiving the signed `payment` callback (HMAC-SHA256 `X-Xfers-Signature`) or by polling `getPayment` — GET `/payments/{paymentId}` — until `status` is `completed`.
4. Reconcile with `listPayments` — GET `/payments` — using `filter[referenceId]` / `filter[status]` and `page[size]`/`page[number]`.

## Rules
- **Idempotency:** the `referenceId` is the idempotency key — reuse the same value on retries so a payment is never created twice.
- **Errors:** handle the codes in `errors/fazz-error-codes.yml` (e.g. `005` invalid parameters, `TXN0002` invalid amount). Back off on HTTP 429.
- See `conventions/fazz-conventions.yml` for pagination and error-envelope details.
