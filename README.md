# Ordergroove (ordergroove)

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

Ordergroove is an enterprise subscription and relationship-commerce platform that lets retailers and DTC brands run recurring purchases, autoship, memberships, bundles, prepaid, and rotating/curation subscriptions on top of their existing eCommerce store. It exposes a documented public REST API at `restapi.ordergroove.com` organized around a four-object data model - Customer, Subscription, Item, and Order - plus supporting resources for Products, Offers and Incentives, Payments, Addresses, and Entitlements, and outbound Webhooks for order, item, subscription, and subscriber events. A GraphQL API for subscription and order data is in Early Access.

**Access model:** Ordergroove is an enterprise, closed-source SaaS product sold through its sales team - there is no public self-serve signup or published price list, and calling the API requires a contracted merchant account with API keys. However, the developer documentation and API reference at [developer.ordergroove.com](https://developer.ordergroove.com) are **publicly readable**, and the endpoint paths, data model, authentication, and rate limits in this catalog are drawn from that public reference. The OpenAPI here models a representative subset of the 100+ documented operations.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ordergroove/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ordergroove/refs/heads/main/apis.yml)

## Authentication

- **Application API scope** - server-to-server requests using an `x-api-key` header (one of ten keys available per store). Optional Bulk Operations permission enables multi-customer data retrieval.
- **Storefront API scope** - client-side, HMAC-SHA256-signed requests scoped to a single customer (sign `customer_id|timestamp`, Base64-encoded, valid two hours).
- HTTPS only. Base URL `https://restapi.ordergroove.com` (staging `https://staging.restapi.ordergroove.com`).

## Tags

- Subscriptions
- Recurring Commerce
- Relationship Commerce
- eCommerce
- Autoship
- DTC
- Retail
- Subscription Management

## Timestamps

- **Created:** 2026-07-10
- **Modified:** 2026-07-10

## APIs

### Ordergroove Subscriptions API

List, retrieve, create, update, cancel, and reactivate recurring subscriptions, and change their frequency, quantity, product, payment, shipping address, email reminder, and next order date. Covers prepaid, rotating, and bundle subscription variants.

- **Human URL:** [https://developer.ordergroove.com/reference/subscriptions-list](https://developer.ordergroove.com/reference/subscriptions-list)
- **Base URL:** `https://restapi.ordergroove.com`

### Ordergroove Customers API

Manage the central customer profile that ties together subscriptions, orders, addresses, and payment methods - list, retrieve, create, update, and set contact details.

- **Human URL:** [https://developer.ordergroove.com/reference/customers-list](https://developer.ordergroove.com/reference/customers-list)
- **Base URL:** `https://restapi.ordergroove.com`

### Ordergroove Orders API

Work with the recurring orders that subscriptions generate before they are sent to the merchant platform - list, retrieve, cancel, send now, skip, and change shipping address, payment, and place date.

- **Human URL:** [https://developer.ordergroove.com/reference/orders-list](https://developer.ordergroove.com/reference/orders-list)
- **Base URL:** `https://restapi.ordergroove.com`

### Ordergroove Items API

Manage the individual products within an order or tied to a subscription - list, retrieve, create, delete, change quantity and price, and swap product. Items may be recurring or one-time additions.

- **Human URL:** [https://developer.ordergroove.com/reference/items-list](https://developer.ordergroove.com/reference/items-list)
- **Base URL:** `https://restapi.ordergroove.com`

### Ordergroove Products API

Manage the product catalog that subscriptions and items reference - list, retrieve, update, bulk create/update, check group membership, and manage relationships and product groups.

- **Human URL:** [https://developer.ordergroove.com/reference/products-list](https://developer.ordergroove.com/reference/products-list)
- **Base URL:** `https://restapi.ordergroove.com`

### Ordergroove Offers and Incentives API

Retrieve offer profiles and incentive logic, manage one-time discounts (OTD), list cancellation reasons, and list, modify, and void entitlements attached to a customer.

- **Human URL:** [https://developer.ordergroove.com/reference/offer-profile-list](https://developer.ordergroove.com/reference/offer-profile-list)
- **Base URL:** `https://restapi.ordergroove.com`

### Ordergroove Webhooks API

Subscribe to and receive outbound event notifications for order, item, subscription, subscriber, entitlement, and workflow events. Delivered as server-to-endpoint HTTP POST callbacks - not a WebSocket stream.

- **Human URL:** [https://developer.ordergroove.com/reference/webhooks-overview](https://developer.ordergroove.com/reference/webhooks-overview)
- **Base URL:** `https://restapi.ordergroove.com`

### Ordergroove GraphQL API (Early Access)

A GraphQL surface over subscription and order data, announced in Early Access and positioned for AI agents to explore the schema and fetch exactly what they need. The public schema and endpoint detail are not yet fully documented - this entry is modeled and unconfirmed pending general availability.

- **Human URL:** [https://www.ordergroove.com/blog/how-ordergroove-is-using-graphql-to-build-ai-ready-subscription-infrastructure/](https://www.ordergroove.com/blog/how-ordergroove-is-using-graphql-to-build-ai-ready-subscription-infrastructure/)
- **Base URL:** `https://restapi.ordergroove.com`

## Common Properties

- [GitHub Organization](https://github.com/ordergroove)
- [LinkedIn](https://www.linkedin.com/company/ordergroove)
- [Website](https://www.ordergroove.com)
- [Documentation](https://developer.ordergroove.com)
- [Sign Up](https://www.ordergroove.com/get-started)
- [Plans](plans/ordergroove-plans-pricing.yml)
- [Rate Limits](rate-limits/ordergroove-rate-limits.yml)
- [Fin Ops](finops/ordergroove-finops.yml)
- [Blog](https://www.ordergroove.com/blog/)

## Rate Limits

All REST endpoints are limited to **6,000 requests per IP address per minute**. Over-limit requests return `429 Too Many Requests`, documented as safe to retry. Large data sets are traversed with cursor-based pagination.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
