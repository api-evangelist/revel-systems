# Revel Systems (revel-systems)

Revel Systems is a cloud iPad-based POS for restaurants and retailers. The Revel Open API exposes products, orders, customers, employees, inventory, schedules, and reporting via a REST interface for partner integrations. The API follows Django Tastypie conventions (objects/meta list envelope, field-lookup filtering) and is complemented by an HMAC-signed webhook channel.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/revel-systems/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/revel-systems/refs/heads/main/apis.yml)

## Tags

- POS
- Restaurant
- Retail
- iPad

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-06-03

## APIs

### Revel Open API

REST API for the Revel POS platform. Exposes products, orders, order items, customers, establishments, employees, schedules, inventory, and reports. Authenticated via API key/secret per Revel establishment using the API-AUTHENTICATION header. Built on Django Tastypie conventions.

- **Human URL:** [https://developer.revelsystems.com/revelsystems/reference/welcome](https://developer.revelsystems.com/revelsystems/reference/welcome)
- **Base URL:** `https://yoursubdomain.revelup.com/resources`

#### Tags

- REST
- POS

#### Properties

- [Documentation](https://developer.revelsystems.com/revelsystems/reference/welcome)
- [API Reference](https://developer.revelsystems.com/revelsystems/reference)
- [Getting Started](https://developer.revelsystems.com/revelsystems/docs/how-to-make-an-api-call)
- [Authentication](https://developer.revelsystems.com/revelsystems/docs/how-to-make-an-api-call)
- [Changelog](https://developer.revelsystems.com/revelsystems/changelog/welcome-to-revelsystems)
- [OpenAPI](openapi/revel-open-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/revel-open-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/revel-open-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/revel-open-api-order-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/revel-open-api-product-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/revel-open-api-customer-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/revel-open-api-establishment-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/revel-open-api-time-schedule-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/revel-open-api-order-structure.json)
- [JSON Structure](json-structure/revel-open-api-product-structure.json)
- [JSON Structure](json-structure/revel-open-api-customer-structure.json)
- [J S O N- L D](json-ld/revel-open-api-context.jsonld)
- [Example](examples/revel-open-api-order-example.json)
- [Example](examples/revel-open-api-product-example.json)
- [Example](examples/revel-open-api-customer-example.json)
- [Plans](plans/revel-systems-plans-pricing.yml)
- [Rate Limits](rate-limits/revel-systems-rate-limits.yml)
- [Fin Ops](finops/revel-systems-finops.yml)

### Revel Webhooks

Event-driven webhook channel that delivers POS events (order finalized, customer created/updated, stock changes, menu updates, timesheet changes, integration changes, reward cards, and ping) to partner HTTPS endpoints via POST. Payloads are signed with an HMAC-SHA1 X-Revel-Signature header.

- **Human URL:** [https://developer.revelsystems.com/revelsystems/docs/webhooks](https://developer.revelsystems.com/revelsystems/docs/webhooks)

#### Tags

- Webhooks
- Events
- POS

#### Properties

- [Documentation](https://developer.revelsystems.com/revelsystems/docs/webhooks)
- [AsyncAPI](asyncapi/revel-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Schema](json-schema/revel-webhooks-order-finalized-payload-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/revel-webhooks-customer-event-payload-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/revel-webhooks-stock-status-payload-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [J S O N- L D](json-ld/revel-webhooks-context.jsonld)
- [Example](examples/revel-webhooks-order-finalized-payload-example.json)
- [Postman Collection](collections/revel-open-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/revel-open-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/RevelSystems)
- [LinkedIn](https://www.linkedin.com/company/revel-systems)
- [Website](https://revelsystems.com/)
- [Developer](https://developer.revelsystems.com/)
- [F A Q](https://developer.revelsystems.com/revelsystems/docs/frequently-asked-questions)
- [Spectral Rules](rules/revel-systems-rules.yml)
- [Vocabulary](vocabulary/revel-systems-vocabulary.yml)
- [Plans](plans/revel-systems-plans-pricing.yml)
- [Rate Limits](rate-limits/revel-systems-rate-limits.yml)
- [Fin Ops](finops/revel-systems-finops.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
