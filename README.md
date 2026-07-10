# Ordergroove (ordergroove)

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
