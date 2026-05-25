# Changelog

All notable changes to `@scoova/weather-react-native` are documented here.

## 1.1.1 — 2026-05-25
- Default `baseUrl` switched from the retired `https://weather.scoo-va.info` subdomain to the central gateway at `https://api.scoo-va.info/api/v1/weather`. Callers who explicitly set `baseUrl` are unaffected. The old subdomain returns `ENDPOINT_RETIRED`.

## 1.1.0 — 2026-05-25

- **New:** built-in `locale` option (BCP-47 — `en`, `fr`, `es`, `de`, `it`,
  `pt-BR`, `nl`, `ar`, `ar-EG`, `ar-SA`, plus regional variants). Sent as
  `?locale=` and `Accept-Language`; per-call `locale` on `ForecastQuery`
  overrides the client default.
- **New:** built-in `apiKey` option for gateway-routed calls; adds
  `X-API-Key` automatically.
- Verified endpoint surface against the live gateway: `current()`,
  `hourly()`, `daily()`, `forecast()`, and `raw()` all hit
  `/v1/forecast`.
- License: switched from MIT to Apache-2.0 to match the rest of the
  Scoova platform SDKs.
- Repo: moved to `Scoova/scoova-weather-react-native`.

## 1.0.0 — 2026-04-12

- Initial release: API surface parity with `@scoova/weather`.
