# Ordergroove

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

Ordergroove is an enterprise subscription and relationship-commerce platform that lets retailers and DTC brands offer recurring purchases, autoship, memberships, bundles, prepaid, and rotating/curation subscriptions on top of their existing eCommerce store. It exposes a documented public REST API at restapi.ordergroove.com organized around a four-object data model - Customer, Subscription, Item, and Order - plus supporting resources for Products, Offers and Incentives, Payments, Addresses, and Entitlements, along with outbound Webhooks for order, item, subscription, and subscriber events. Requests use an Application API scope (x-api-key header, server-to-server) or a Storefront API scope (HMAC-SHA256-signed, single-customer context). A GraphQL API for subscription and order data is in Early Access. The platform itself is enterprise and sold through sales, but the developer documentation and API reference are publicly readable.

**Areas:** Subscription · Recurring Commerce · Relationship Commerce · E-Commerce · Autoship · Direct to Consumer · Retail · Subscription Management

## Ordergroove on APIs.io

Everything profiled for Ordergroove is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/ordergroove/](https://apis.io/providers/ordergroove/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [Ordergroove GraphQL API (Early Access)](https://apis.io/apis/ordergroove/ordergroove-graphql-api/) — A GraphQL surface over Ordergroove subscription and order data, announced in Early Access and positioned for AI agents to explore the schema and fetch…
- [Ordergroove Customers API](https://apis.io/apis/ordergroove/ordergroove-customers-api/) — Central customer profiles.
- [Ordergroove Items API](https://apis.io/apis/ordergroove/ordergroove-items-api/) — Line items within orders and subscriptions.
- [Ordergroove Offers API](https://apis.io/apis/ordergroove/ordergroove-offers-api/) — Offers, incentives, discounts, and entitlements.
- [Ordergroove Orders API](https://apis.io/apis/ordergroove/ordergroove-orders-api/) — Recurring orders generated by subscriptions.
- [Ordergroove Products API](https://apis.io/apis/ordergroove/ordergroove-products-api/) — Product catalog and product groups.
- [Ordergroove Subscriptions API](https://apis.io/apis/ordergroove/ordergroove-subscriptions-api/) — Recurring subscription agreements.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [ordergroove](https://apis.io/servers/ordergroove/ordergroove/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Ordergroove Agentic Access](https://apis.io/agentic-access/ordergroove/ordergroove-agentic-access/)

#### Collections (7)

Postman and Open Collection request collections.

- [Ordergroove REST API](https://apis.io/collections/ordergroove/open-ordergroove/)
- [Ordergroove REST Customers API](https://apis.io/collections/ordergroove/open-ordergroove-customers-api/)
- [Ordergroove REST Customers Items API](https://apis.io/collections/ordergroove/open-ordergroove-items-api/)
- [Ordergroove REST Customers Offers API](https://apis.io/collections/ordergroove/open-ordergroove-offers-api/)
- [Ordergroove REST Customers Orders API](https://apis.io/collections/ordergroove/open-ordergroove-orders-api/)
- [Ordergroove REST Customers Products API](https://apis.io/collections/ordergroove/open-ordergroove-products-api/)
- [Ordergroove REST Customers Subscriptions API](https://apis.io/collections/ordergroove/open-ordergroove-subscriptions-api/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Ordergroove Authentication](https://apis.io/security/ordergroove/ordergroove-authentication/)
- [Ordergroove Domain Security](https://apis.io/security/ordergroove/ordergroove-domain-security/)
- [Ordergroove Trust Center](https://apis.io/security/ordergroove/ordergroove-trust-center/)
- [Ordergroove Vulnerability Disclosure](https://apis.io/security/ordergroove/ordergroove-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Ordergroove Plans Pricing](https://apis.io/plans/ordergroove/ordergroove-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Ordergroove Rate Limits](https://apis.io/rate-limits/ordergroove/ordergroove-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Ordergroove Finops](https://apis.io/finops/ordergroove/ordergroove-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.ordergroove.com)
- [Documentation](https://developer.ordergroove.com)
- [Sign up](https://www.ordergroove.com/get-started)
- [Blog](https://www.ordergroove.com/blog/)
- [GitHub](https://github.com/ordergroove)

## API Evangelist rating

**Kin Score 28.4** — thin · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 68.3 |
| Contract quality | 44.1 |
| Contract governance | 0.0 |
| Operational transparency | 21.1 |
| Developer ergonomics | 23.8 |
| Access clarity | 13.2 |

**Agent readiness 37.6** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 22.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/ordergroove/](https://apis.io/providers/ordergroove/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Ordergroove: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/ordergroove/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
