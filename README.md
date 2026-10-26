# Tibber (tibber)

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

Tibber is a fully-digital Nordic and European retail electricity provider operating in Norway, Sweden, Germany, and the Netherlands. Founded in 2016 by Daniel Lindén and Edgeir Vårdal Aksnes, the company passes Nord Pool / EPEX hourly spot prices through to customers at cost and overlays software-driven optimisation for EV charging, heat pumps, and rooftop solar to shift load to cheap and clean grid hours. Tibber publishes two distinct developer APIs: the long-standing GraphQL endpoint at api.tibber.com/v1-beta/gql for customer, subscription, price, consumption, production, and real-time `liveMeasurement` data streamed from the Tibber Pulse; and the newer OAuth 2.0 Data API at data-api.tibber.com that exposes normalised time series for third-party IoT devices (vehicles, chargers, thermostats / heat pumps, inverters, home batteries) linked through the Tibber mobile app.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/tibber/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tibber/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consuming

## Tags

- Energy
- SmartHome
- SmartMeter
- ElectricityPricing
- ElectricVehicleCharging
- HeatPump
- SolarInverter
- HomeBattery
- GraphQL
- OAuth2
- Nordic

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Tibber GraphQL API

Tibber's long-standing GraphQL API. A single HTTPS endpoint serves the `viewer` query (with nested `homes`, `currentSubscription`, `priceInfo`, `consumption`, `production`, and `features`), the `liveMeasurement` websocket subscription that streams sub-second power, voltage, and current readings from a paired Tibber Pulse, and the `sendMeterReading`, `updateHome`, and `sendPushNotification` mutations. Authentication is a personal access token issued at developer.tibber.com.

- **Human URL:** [https://developer.tibber.com/docs](https://developer.tibber.com/docs)
- **Base URL:** `https://api.tibber.com/v1-beta/gql`

#### Tags

- Energy
- GraphQL
- LiveMeasurement
- ElectricityPricing
- SmartMeter

#### Properties

- [Documentation](https://developer.tibber.com/docs)
- [Documentation](https://developer.tibber.com/docs/guides/calling-api)
- [Documentation](https://developer.tibber.com/docs/guides/graphql-concepts)
- [API Reference](https://developer.tibber.com/docs/reference)
- [Sandbox](https://developer.tibber.com/explorer)
- [Authentication](https://developer.tibber.com/settings/access-token)
- [OpenAPI](openapi/tibber-graphql-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tibber-graphql-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tibber-graphql-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/tibber-home-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tibber-price-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tibber-consumption-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tibber-live-measurement-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/tibber-home-structure.json)
- [JSON Structure](json-structure/tibber-price-structure.json)
- [JSON Structure](json-structure/tibber-live-measurement-structure.json)
- [Example](examples/tibber-current-price-example.json)
- [Example](examples/tibber-consumption-example.json)
- [Example](examples/tibber-live-measurement-example.json)

### Tibber Data API

Tibber's modern REST API for third-party connected IoT devices. OAuth 2.0 Authorization Code Flow with PKCE; scopes gate each device category (`data-api-vehicles-read`, `data-api-chargers-read`, `data-api-thermostats-read`, `data-api-inverters-read`, `data-api-energy-systems-read`). Endpoints list homes, list and inspect devices, and walk paginated immutable device history at quarter-hour, hour, day, or month resolution. Tibber Pulse live streaming, pricing, and proprietary optimisation logic are explicitly out of scope and remain on the legacy GraphQL API.

- **Human URL:** [https://data-api.tibber.com/docs/](https://data-api.tibber.com/docs/)
- **Base URL:** `https://data-api.tibber.com/v1`

#### Tags

- Energy
- REST
- OAuth2
- IoT
- ElectricVehicle
- HeatPump
- SolarInverter
- HomeBattery

#### Properties

- [Documentation](https://data-api.tibber.com/docs/)
- [Documentation](https://data-api.tibber.com/docs/get-started/)
- [Documentation](https://data-api.tibber.com/docs/api-usage/)
- [Documentation](https://data-api.tibber.com/docs/api-usage/rate-limiting/)
- [Documentation](https://data-api.tibber.com/docs/api-usage/retry-backoff/)
- [Documentation](https://data-api.tibber.com/docs/api-usage/troubleshooting/)
- [Authentication](https://data-api.tibber.com/docs/auth/)
- [Scopes](https://data-api.tibber.com/docs/scopes/)
- [Sandbox](https://data-api.tibber.com/playground/)
- [Changelog](https://data-api.tibber.com/docs/changelog/)
- [F A Q](https://data-api.tibber.com/docs/further-reading/faq/)
- [Documentation](https://data-api.tibber.com/docs/devices/supported/)
- [Documentation](https://data-api.tibber.com/docs/devices/device-history/)
- [Documentation](https://data-api.tibber.com/docs/managing-clients/)
- [Console](https://data-api.tibber.com/clients/manage/)
- [OpenAPI](openapi/tibber-data-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tibber-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tibber-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/tibber-device-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tibber-device-history-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/tibber-device-structure.json)
- [Example](examples/tibber-list-homes-example.json)
- [Example](examples/tibber-device-example.json)
- [Example](examples/tibber-device-history-example.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://tibber.com/en)
- [Documentation](https://developer.tibber.com)
- [Documentation](https://data-api.tibber.com/docs/)
- [Sign Up](https://tibber.com/en)
- [Store](https://tibber.com/en/store)
- [Pricing](https://tibber.com/en/store)
- [Status Page](https://status.tibber.com/)
- [Support](https://support.tibber.com/en/)
- [Changelog](https://data-api.tibber.com/docs/changelog/)
- [Terms of Service](https://tibber.com/en/legal-notice)
- [Privacy Policy](https://tibber.com/en/terms/privacy-policy)
- [GitHub Organization](https://github.com/tibber)
- [GitHub Repository](https://github.com/tibber/Tibber.SDK.NET)
- [GitHub Repository](https://github.com/tibber/com.tibber.athom)
- [GitHub Repository](https://github.com/tibber/homevolt-local-api-doc)
- [GitHub Repository](https://github.com/tibber/tibber-httpclient)
- [GitHub Repository](https://github.com/tibber/tibber-express-utils)
- [GitHub Repository](https://github.com/tibber/tibber-aws)
- [SDK](https://github.com/tibber/Tibber.SDK.NET)
- [SDK](https://github.com/bisand/tibber-api)
- [SDK](https://github.com/stefanes/PSTibber)
- [SDK](https://github.com/mkalen/tibber-graphql-client)
- [Plugins](https://www.home-assistant.io/integrations/tibber/)
- [Plugins](https://marketplace.fibaro.com/items/tibber-live)
- [Careers](https://jobs.tibber.com/)
- [Forum](https://www.facebook.com/groups/tibbergebruikers/)
- [Spectral Rules](rules/tibber-rules.yml)
- [Vocabulary](vocabulary/tibber-vocabulary.yml)
- [JSON-LD](json-ld/tibber-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Plans](plans/tibber-plans-pricing.yml)
- [Rate Limits](rate-limits/tibber-rate-limits.yml)
- [Fin Ops](finops/tibber-finops.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
