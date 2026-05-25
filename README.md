# Tibber (tibber)

Tibber is a fully-digital Nordic and European retail electricity provider operating in Norway, Sweden, Germany, and the Netherlands. Founded in 2016 by Daniel Lindén and Edgeir Vårdal Aksnes, the company passes Nord Pool / EPEX hourly spot prices through to customers at cost and overlays software-driven optimisation for EV charging, heat pumps, and rooftop solar to shift load to cheap and clean grid hours. Tibber publishes two distinct developer APIs: a long-standing GraphQL endpoint for customer, price, consumption, production, and live Pulse measurements, plus a newer OAuth 2.0 Data API exposing normalised time series for third-party IoT devices linked through the Tibber app.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/tibber/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Energy, SmartHome, SmartMeter, ElectricityPricing, ElectricVehicleCharging, HeatPump, SolarInverter, HomeBattery, GraphQL, OAuth2, Nordic

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Markets

| Market | Bidding zones | Currency |
|---|---|---|
| Norway | NO1 / NO2 / NO3 / NO4 / NO5 | NOK |
| Sweden | SE1 / SE2 / SE3 / SE4 | SEK |
| Germany | DE-LU | EUR |
| Netherlands | NL | EUR |

## APIs

### Tibber GraphQL API

Single GraphQL endpoint that exposes the authenticated `viewer`, their `homes`, `currentSubscription`, hourly `priceInfo`, paginated `consumption` and `production`, the websocket `liveMeasurement` subscription driven by the Tibber Pulse, and the `sendMeterReading`, `updateHome`, and `sendPushNotification` mutations.

**Human URL:** [https://developer.tibber.com/docs](https://developer.tibber.com/docs)

- [Documentation](https://developer.tibber.com/docs)
- [Communicating with the API](https://developer.tibber.com/docs/guides/calling-api)
- [GraphQL Concepts](https://developer.tibber.com/docs/guides/graphql-concepts)
- [API Reference](https://developer.tibber.com/docs/reference)
- [API Explorer Sandbox](https://developer.tibber.com/explorer)
- [Personal Access Tokens](https://developer.tibber.com/settings/access-token)
- [OpenAPI](openapi/tibber-graphql-api-openapi.yml)
- [JSON Schema — Home](json-schema/tibber-home-schema.json)
- [JSON Schema — Price](json-schema/tibber-price-schema.json)
- [JSON Schema — Consumption](json-schema/tibber-consumption-schema.json)
- [JSON Schema — Live Measurement](json-schema/tibber-live-measurement-schema.json)
- [JSON Structure — Home](json-structure/tibber-home-structure.json)
- [JSON Structure — Price](json-structure/tibber-price-structure.json)
- [JSON Structure — Live Measurement](json-structure/tibber-live-measurement-structure.json)
- [Example — Current Price](examples/tibber-current-price-example.json)
- [Example — Hourly Consumption](examples/tibber-consumption-example.json)
- [Example — Live Measurement](examples/tibber-live-measurement-example.json)
- [Naftiko Capability — Customer GraphQL](capabilities/tibber-graphql-customer.yaml)

### Tibber Data API

OAuth 2.0 Authorization Code Flow (PKCE recommended) for third-party connected IoT devices. Scopes gate each device category; endpoints list homes, list and inspect devices, and walk paginated immutable device history at quarter-hour, hourly, daily, or monthly resolution.

**Human URL:** [https://data-api.tibber.com/docs/](https://data-api.tibber.com/docs/)

- [Documentation](https://data-api.tibber.com/docs/)
- [Quick Start](https://data-api.tibber.com/docs/get-started/)
- [Authentication](https://data-api.tibber.com/docs/auth/)
- [Scopes](https://data-api.tibber.com/docs/scopes/)
- [API Usage](https://data-api.tibber.com/docs/api-usage/)
- [Rate Limiting](https://data-api.tibber.com/docs/api-usage/rate-limiting/)
- [Retry & Backoff](https://data-api.tibber.com/docs/api-usage/retry-backoff/)
- [Troubleshooting](https://data-api.tibber.com/docs/api-usage/troubleshooting/)
- [Supported Devices](https://data-api.tibber.com/docs/devices/supported/)
- [Device History](https://data-api.tibber.com/docs/devices/device-history/)
- [Managing Clients](https://data-api.tibber.com/docs/managing-clients/)
- [Playground](https://data-api.tibber.com/playground/)
- [Changelog](https://data-api.tibber.com/docs/changelog/)
- [Manage Clients Console](https://data-api.tibber.com/clients/manage/)
- [OpenAPI](openapi/tibber-data-api-openapi.yml)
- [JSON Schema — Device](json-schema/tibber-device-schema.json)
- [JSON Schema — Device History](json-schema/tibber-device-history-schema.json)
- [JSON Structure — Device](json-structure/tibber-device-structure.json)
- [Example — List Homes](examples/tibber-list-homes-example.json)
- [Example — Device](examples/tibber-device-example.json)
- [Example — Device History](examples/tibber-device-history-example.json)
- [Naftiko Capability — Homes & Devices](capabilities/tibber-data-api-homes.yaml)
- [Naftiko Capability — Device History](capabilities/tibber-data-api-history.yaml)

## OAuth Scopes (Data API)

| Scope | Grants |
|---|---|
| `openid` / `profile` / `email` / `offline_access` | Standard OpenID baseline plus refresh tokens. |
| `data-api-user-read` | Basic user context (required baseline). |
| `data-api-homes-read` | List the user's homes. |
| `data-api-vehicles-read` | Connected electric vehicles. |
| `data-api-chargers-read` | EV chargers / EVSE. |
| `data-api-thermostats-read` | Thermostats, heat pumps, space heaters. |
| `data-api-inverters-read` | Solar inverters. |
| `data-api-energy-systems-read` | Home batteries and hybrid systems. |

## Common Properties

- [Portal](https://tibber.com/en)
- [Developer Portal](https://developer.tibber.com)
- [Data API Docs](https://data-api.tibber.com/docs/)
- [Store / Pricing](https://tibber.com/en/store)
- [Status Page](https://status.tibber.com/)
- [Support Center](https://support.tibber.com/en/)
- [Changelog](https://data-api.tibber.com/docs/changelog/)
- [Legal Notice](https://tibber.com/en/legal-notice)
- [Privacy Policy](https://tibber.com/en/terms/privacy-policy)
- [GitHub Organization](https://github.com/tibber)
- [Careers](https://jobs.tibber.com/)

## SDKs

- [Tibber.SDK.NET](https://github.com/tibber/Tibber.SDK.NET) — Official C# / .NET SDK
- [tibber-api](https://github.com/bisand/tibber-api) — Community Node.js / TypeScript SDK
- [PSTibber](https://github.com/stefanes/PSTibber) — Community PowerShell module
- [tibber-graphql-client](https://github.com/mkalen/tibber-graphql-client) — Community Java GraphQL client

## Integration Apps

- [Home Assistant Tibber integration](https://www.home-assistant.io/integrations/tibber/)
- [Tibber app for Athom Homey](https://github.com/tibber/com.tibber.athom)
- [Fibaro Tibber Live](https://marketplace.fibaro.com/items/tibber-live)
- [Homevolt local API docs](https://github.com/tibber/homevolt-local-api-doc)

## Cross-Cutting Artifacts

- [Spectral Rules](rules/tibber-rules.yml)
- [Vocabulary](vocabulary/tibber-vocabulary.yml)
- [JSON-LD Context](json-ld/tibber-context.jsonld)
- [Plans & Pricing (API Commons Plans 0.1)](plans/tibber-plans-pricing.yml)
- [Rate Limits (API Commons Rate Limits 0.1)](rate-limits/tibber-rate-limits.yml)
- [FinOps (FOCUS 1.3)](finops/tibber-finops.yml)

## Maintainer

- **Kin Lane** — [info@apievangelist.com](mailto:info@apievangelist.com) — [@apievangelist](https://x.com/apievangelist) — [apievangelist.com](https://apievangelist.com)
