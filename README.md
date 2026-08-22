# Fazz (fazz)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
