# Revel Systems (revel-systems)
Revel Systems is a cloud iPad-based POS for restaurants and retailers. The Revel Open API exposes products, orders, customers, employees, inventory, schedules, and reporting via a REST interface for partner integrations. The API follows Django Tastypie conventions (objects/meta list envelope, field-lookup filtering) and is complemented by an HMAC-signed webhook channel.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/revel-systems/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - POS, Restaurant, Retail, iPad

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-06-03

## APIs

### Revel Open API
REST API for the Revel POS platform. Exposes products, orders, order items, customers, establishments, employees, schedules, inventory, and reports. Authenticated via API key/secret per Revel establishment using the API-AUTHENTICATION header. Built on Django Tastypie conventions.

**Human URL:** [https://developer.revelsystems.com/revelsystems/reference/welcome](https://developer.revelsystems.com/revelsystems/reference/welcome)

**Base URL:** `https://yoursubdomain.revelup.com/resources`

#### Tags:

 - REST, POS

#### Properties

- [Documentation](https://developer.revelsystems.com/revelsystems/reference/welcome)
- [APIReference](https://developer.revelsystems.com/revelsystems/reference)
- [GettingStarted](https://developer.revelsystems.com/revelsystems/docs/how-to-make-an-api-call)
- [Authentication](https://developer.revelsystems.com/revelsystems/docs/how-to-make-an-api-call)
- [ChangeLog](https://developer.revelsystems.com/revelsystems/changelog/welcome-to-revelsystems)
- [OpenAPI](openapi/revel-open-api-openapi.yml)
- [JSONSchema — Order](json-schema/revel-open-api-order-schema.json)
- [JSONSchema — Product](json-schema/revel-open-api-product-schema.json)
- [JSONSchema — Customer](json-schema/revel-open-api-customer-schema.json)
- [JSONSchema — Establishment](json-schema/revel-open-api-establishment-schema.json)
- [JSONSchema — TimeSchedule](json-schema/revel-open-api-time-schedule-schema.json)
- [JSONStructure — Order](json-structure/revel-open-api-order-structure.json)
- [JSONStructure — Product](json-structure/revel-open-api-product-structure.json)
- [JSONStructure — Customer](json-structure/revel-open-api-customer-structure.json)
- [JSON-LD](json-ld/revel-open-api-context.jsonld)
- [Example — Order](examples/revel-open-api-order-example.json)
- [Example — Product](examples/revel-open-api-product-example.json)
- [Example — Customer](examples/revel-open-api-customer-example.json)
- [NaftikoCapability — Orders](capabilities/revel-open-api-orders.yaml)
- [NaftikoCapability — Products](capabilities/revel-open-api-products.yaml)
- [NaftikoCapability — Customers](capabilities/revel-open-api-customers.yaml)
- [NaftikoCapability — Establishments](capabilities/revel-open-api-establishments.yaml)
- [NaftikoCapability — Scheduling](capabilities/revel-open-api-scheduling.yaml)
- [Plans](plans/revel-systems-plans-pricing.yml)
- [RateLimits](rate-limits/revel-systems-rate-limits.yml)
- [FinOps](finops/revel-systems-finops.yml)

### Revel Webhooks
Event-driven webhook channel that delivers POS events (order finalized, customer created/updated, stock changes, menu updates, timesheet changes, integration changes, reward cards, and ping) to partner HTTPS endpoints via POST. Payloads are signed with an HMAC-SHA1 X-Revel-Signature header.

**Human URL:** [https://developer.revelsystems.com/revelsystems/docs/webhooks](https://developer.revelsystems.com/revelsystems/docs/webhooks)

#### Tags:

 - Webhooks, Events, POS

#### Properties

- [Documentation](https://developer.revelsystems.com/revelsystems/docs/webhooks)
- [AsyncAPI](asyncapi/revel-webhooks-asyncapi.yml)
- [JSONSchema — Order Finalized Payload](json-schema/revel-webhooks-order-finalized-payload-schema.json)
- [JSONSchema — Customer Event Payload](json-schema/revel-webhooks-customer-event-payload-schema.json)
- [JSONSchema — Stock Status Payload](json-schema/revel-webhooks-stock-status-payload-schema.json)
- [JSON-LD](json-ld/revel-webhooks-context.jsonld)
- [Example — Order Finalized](examples/revel-webhooks-order-finalized-payload-example.json)

## Common Properties

- [GitHubOrganization](https://github.com/RevelSystems)
- [LinkedIn](https://www.linkedin.com/company/revel-systems)
- [Website](https://revelsystems.com/)
- [Developer](https://developer.revelsystems.com/)
- [FAQ](https://developer.revelsystems.com/revelsystems/docs/frequently-asked-questions)
- [SpectralRules](rules/revel-systems-rules.yml)
- [Vocabulary](vocabulary/revel-systems-vocabulary.yml)
- [Plans](plans/revel-systems-plans-pricing.yml) — per-terminal monthly SaaS (reconciled: false)
- [RateLimits](rate-limits/revel-systems-rate-limits.yml) — 429 backoff + webhook retry policy (reconciled: false)
- [FinOps](finops/revel-systems-finops.yml) — FOCUS-aligned per-terminal SaaS (reconciled: false)

## Features

| Name | Description |
|------|-------------|
| Tastypie REST Conventions | List endpoints return an objects array with a meta pagination envelope (total_count, limit, offset, next, previous). |
| Field-Lookup Filtering | Filter resources with Django-style lookups (e.g. id__lt, created_date__range, name__icontains). |
| Field Selection and Expansion | Use the fields parameter to limit returned attributes and expand to inline one level of foreign-key relationships. |
| Batch Retrieval | Retrieve multiple records by ID in a single call using the set/id1;id2;id3 path form. |
| Signed Webhooks | Real-time event delivery secured with HMAC-SHA1 signatures and per-event-type endpoint registration. |

## Use Cases

| Name | Description |
|------|-------------|
| Order Synchronization | Sync finalized orders into accounting, ERP, or analytics systems via the Order resource and order.finalized webhook. |
| Catalog Management | Create and maintain products, modifiers, and combo sets across establishments. |
| Customer and Loyalty | Sync customer profiles and loyalty/reward data with marketing and CRM platforms. |
| Labor and Scheduling | Read and write employee shifts and timesheets via TimeSchedule, TimeScheduleRule, and TimeSheetEntry. |
| Inventory Monitoring | React to stock-status changes in real time via the inout.stock webhook. |

## Integrations

| Name | Description |
|------|-------------|
| Accounting and ERP | Push order and sales data into accounting and ERP systems. |
| Payments | Establishment-level payment configuration including ACH for US establishments. |
| Marketing and CRM | Sync customer and loyalty data with marketing platforms. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Revel Open API](openapi/revel-open-api-openapi.yml)

### AsyncAPI

- [Revel Webhooks](asyncapi/revel-webhooks-asyncapi.yml)

### JSON Schema

10 schema files in [json-schema/](json-schema/) covering Order, Product, Customer, Establishment, TimeSchedule (and list envelopes) plus the eight webhook event payloads.

### JSON Structure

10 structure files in [json-structure/](json-structure/) (JSON Structure core v0).

### JSON-LD

- [Revel Open API Context](json-ld/revel-open-api-context.jsonld)
- [Revel Webhooks Context](json-ld/revel-webhooks-context.jsonld)

### Examples

18 example payloads in [examples/](examples/), one per JSON Schema.

## Capabilities

Naftiko capabilities, one self-contained file per Revel business surface, each exposing both a REST and an MCP adapter routed through its own inline consumes block.

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Orders](capabilities/revel-open-api-orders.yaml) | Revel Open API | 4 | Integration Developer / Operations Analyst |
| [Products](capabilities/revel-open-api-products.yaml) | Revel Open API | 3 | Integration Developer / Menu Manager |
| [Customers](capabilities/revel-open-api-customers.yaml) | Revel Open API | 3 | Integration Developer / Marketing Analyst |
| [Establishments](capabilities/revel-open-api-establishments.yaml) | Revel Open API | 1 | Integration Developer |
| [Scheduling](capabilities/revel-open-api-scheduling.yaml) | Revel Open API | 2 | Integration Developer / Store Manager |

## Vocabulary

- [Revel Systems Vocabulary](vocabulary/revel-systems-vocabulary.yml) — Unified taxonomy mapping 5 resources, 4 actions, 5 workflows, and 5 personas across operational (OpenAPI) and capability (Naftiko) dimensions.

## Rules

- [Revel Systems Rules](rules/revel-systems-rules.yml) — 34 Spectral rules enforcing Revel's Tastypie conventions (PascalCase resource paths, snake_case fields, camelCase operationIds, Title Case tags, API-AUTHENTICATION header auth).

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
