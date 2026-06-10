# Tibber GraphQL API

Tibber's long-standing GraphQL API. A single HTTPS endpoint serves the `viewer` query (with nested `homes`, `currentSubscription`, `priceInfo`, `consumption`, `production`, and `features`), the `liveMeasurement` websocket subscription that streams sub-second power, voltage, and current readings from a paired Tibber Pulse, and the `sendMeterReading`, `updateHome`, and `sendPushNotification` mutations. Authentication is a personal access token issued at developer.tibber.com.

**Endpoint:** https://api.tibber.com/v1-beta/gql

**Documentation:** https://developer.tibber.com/docs

**References:**

- Documentation: https://developer.tibber.com/docs
- Documentation: https://developer.tibber.com/docs/guides/calling-api
- Documentation: https://developer.tibber.com/docs/guides/graphql-concepts
