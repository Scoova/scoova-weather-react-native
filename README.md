# @scoova/weather-react-native

React Native build of the `@scoova/weather` client. Pure TypeScript — no native
modules, no `pod install`, just `fetch`. Works on iOS, Android, and React
Native Web.

```sh
npm install @scoova/weather-react-native
```

```ts
import { WeatherClient, decodeWeatherCode } from '@scoova/weather-react-native';

const client = new WeatherClient({
  baseUrl: 'https://api.scoo-va.info/v1/weather', // gateway
  apiKey:  'sk_live_…',                            // or 'demo'
  locale:  'fr',
});

const now = await client.current(30.04, 31.24);
const condition = decodeWeatherCode(now.current?.weather_code as number);
```

Per-call `locale` on the `forecast()` query overrides the client default.
API surface matches `@scoova/weather` 1:1 — see that package's README for full
docs.

```sh
npm test
```

License: Apache-2.0.
