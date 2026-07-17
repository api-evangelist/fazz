# Fazz (fazz)

Fazz is a Southeast Asian business banking and payments group formed from the 2021 merger of Indonesia's Payfazz and Singapore's Xfers. Its Fazz Business Payments API (served on the xfers.io hosts) lets platforms accept payments via local methods like PayNow QR and virtual bank accounts, and send bulk disbursements across Singapore (SGD) and Indonesia (IDR). Not to be confused with the consumer-facing Payfazz agent app.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fazz/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fazz/refs/heads/main/apis.yml)

## Tags

- Fintech
- Payments
- Business Banking
- Disbursements
- Southeast Asia
- PayNow
- Virtual Accounts

## Timestamps

- **Created:** 2026-07-17
- **Modified:** 2026-07-17

## APIs

### Fazz Accept API (Singapore)

Accept payments securely across local Singapore payment methods - PayNow QR (UEN-based instant transfer) and virtual bank accounts - for one-time or unlimited collections, billed in SGD.

- **Human URL:** [https://docs.fazz.com/reference/create-payment](https://docs.fazz.com/reference/create-payment)
- **Base URL:** `https://www.xfers.io/api/v4`

#### Tags

- Payments
- Collections
- PayNow
- Virtual Accounts

#### Properties

- [Documentation](https://fazz.com/business/products/payments-api/)
- [API Reference](https://docs.fazz.com/reference/create-payment)
- [OpenAPI](openapi/fazz-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fazz.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Fazz Send API (Singapore)

Send payouts to recipients in bulk via automated bank-transfer disbursements from your Fazz Business account, billed in SGD.

- **Human URL:** [https://docs.fazz.com/reference/create-disbursement](https://docs.fazz.com/reference/create-disbursement)
- **Base URL:** `https://www.xfers.io/api/v4`

#### Tags

- Disbursements
- Payouts
- Bank Transfer

#### Properties

- [Documentation](https://fazz.com/business/products/payments-api/)
- [API Reference](https://docs.fazz.com/reference/create-disbursement)
- [OpenAPI](openapi/fazz-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fazz.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Fazz Payment Methods API

Create and manage reusable payment method objects (virtual bank accounts, PayNow) that collect unlimited payments from your customers.

- **Human URL:** [https://docs.fazz.com/reference/accept-payment-methods](https://docs.fazz.com/reference/accept-payment-methods)
- **Base URL:** `https://www.xfers.io/api/v4`

#### Tags

- Payment Methods
- Virtual Accounts
- PayNow

#### Properties

- [API Reference](https://docs.fazz.com/reference/accept-payment-methods)
- [OpenAPI](openapi/fazz-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fazz.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Fazz Indonesia Payments API (v4-ID)

Indonesia-market payments and disbursements (v4-ID) covering local virtual accounts and bank transfers, billed in IDR. Shares the Fazz/Xfers v4 request patterns with region-specific methods and destinations.

- **Human URL:** [https://docs.fazz.com/v4-ID/docs/home](https://docs.fazz.com/v4-ID/docs/home)
- **Base URL:** `https://www.xfers.io/api/v4`

#### Tags

- Payments
- Disbursements
- Indonesia
- Virtual Accounts

#### Properties

- [Documentation](https://docs.fazz.com/v4-ID/docs/home)
- [API Reference](https://docs.fazz.com/v4-ID/docs/disbursements)

### Fazz Callbacks (Webhooks)

HTTP POST webhook callbacks that notify your endpoint of payment and disbursement status changes in JSON, verified against your account signing secret.

- **Human URL:** [https://docs.fazz.com/docs/callbacks](https://docs.fazz.com/docs/callbacks)
- **Base URL:** `https://www.xfers.io/api/v4`

#### Tags

- Webhooks
- Callbacks
- Events

#### Properties

- [Documentation](https://docs.fazz.com/docs/callbacks)

## Common Properties

- [Agentic Access](agentic-access/fazz-agentic-access.yml)
- [Trust Center](security/fazz-trust-center.yml)
- [Vulnerability Disclosure](security/fazz-vulnerability-disclosure.yml)
- [Domain Security](security/fazz-domain-security.yml)
- [Authentication](authentication/fazz-authentication.yml)
- [GitHub Organization](https://github.com/xfers)
- [LinkedIn](https://www.linkedin.com/company/fazz-financial)
- [Website](https://fazz.com/)
- [Documentation](https://docs.fazz.com/)
- [Plans](plans/fazz-plans-pricing.yml)
- [Rate Limits](rate-limits/fazz-rate-limits.yml)
- [Fin Ops](finops/fazz-finops.yml)

## Authentication

HTTP Basic authentication — provide your API key as the Basic auth username and your secret key as the password (`curl -u API_KEY:SECRET_KEY`). Live keys start with `live_`; sandbox keys start with `test_`. All requests must be made over HTTPS. Keys are generated on the Developer Tools page of the Fazz Business dashboard.

## Notes

- **Rebrand / merger:** Fazz Financial Group was formed by the March 2021 merger of Indonesia's Payfazz and Singapore's Xfers. Xfers became Fazz Business, but the payment infrastructure and API hosts remain on `xfers.io` (`www.xfers.io` production, `sandbox.xfers.io` sandbox).
- **Disambiguation:** This repo documents the **Fazz Business** B2B Payments API, not the consumer-facing Payfazz agent app.
- **Regions:** Singapore Payments API (v4, SGD) and Indonesia Payments API (v4-ID, IDR).
- **Spec provenance:** No first-party OpenAPI/Swagger file is published by Fazz; `openapi/fazz-openapi.yml` was modeled by hand from the live developer reference at [docs.fazz.com](https://docs.fazz.com/).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
