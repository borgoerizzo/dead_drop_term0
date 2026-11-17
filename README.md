# term0 releases

Signed release builds of term0. The app checks `latest.json` here at most once a day.

## Latest: 1.3.00

| | |
|---|---|
| File | [`releases/term0-1.3.00.apk`](releases/term0-1.3.00.apk) |
| SHA-256 | `2f33cd35178289d8f708c5e79cd815414b2fe78f5719a4245ef088f3ceb9baaf` |
| Size | 5712048 bytes |
| Signing certificate SHA-256 | `f96442f355261c5c8701dfd94a8aeb06776bf5cc680f4567637ecdc8c81fb00b` |

Every release is signed with the same key. Android refuses to update an installed
term0 with an APK signed by any other key, and the certificate fingerprint above lets
you check a downloaded file yourself:

```
apksigner verify --print-certs term0-1.3.00.apk
```

`latest.json` is signed with a separate Ed25519 key (`latest.json.sig`); the app
ignores it unless the signature verifies.

### Changes

- Tor mode: settings can send all traffic through Orbot, so the server does not see your IP address
- in Tor mode the phone makes no DNS lookups and never falls back to a direct connection if Orbot is down
- the uplink line in settings shows whether Orbot is running
