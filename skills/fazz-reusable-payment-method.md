---
name: Create a reusable Fazz payment method
description: Create a reusable virtual bank account or PayNow object that collects unlimited payments, then list its payments.
api: openapi/fazz-openapi.yml
operations: [createPaymentMethod, listPaymentsForPaymentMethod]
---

# Create a reusable Fazz payment method

Set up a persistent collection object (virtual bank account or PayNow) that accepts unlimited payments from one customer.

## Auth
HTTP Basic (API key : secret key), HTTPS only. See `authentication/fazz-authentication.yml`.

## Steps
1. `createPaymentMethod` — POST `/payment_methods/{type}` where `{type}` is `virtual_bank_accounts` or `paynow`. Provide `referenceId` and optional `displayName` / `paymentMethodOptions`. The response `instructions` carry the account number or PayNow details to hand to your customer.
2. Every subsequent transfer the customer makes to that account/PayNow is collected automatically.
3. `listPaymentsForPaymentMethod` — GET `/payment_methods/{paymentMethodId}/payments` — to list the payments collected by this method.

## Rules
- Use a unique `referenceId` per payment method (idempotency key).
- Reconcile incoming collections against the signed `payment` callbacks (`X-Xfers-Signature`, HMAC-SHA256) — see `asyncapi/fazz-webhooks.yml`.
- Handle errors per `errors/fazz-error-codes.yml`.
