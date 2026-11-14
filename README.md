# term0 releases

Signed release builds of term0. The app checks `latest.json` here at most once a day.

## Latest: 1.0.04

| | |
|---|---|
| File | [`releases/term0-1.0.04.apk`](releases/term0-1.0.04.apk) |
| SHA-256 | `98fc1165042b1cffabd5ff2e050f934b82dcee535e52962c9f8128b6f6b9e745` |
| Size | 5699784 bytes |
| Signing certificate SHA-256 | `f96442f355261c5c8701dfd94a8aeb06776bf5cc680f4567637ecdc8c81fb00b` |

Every release is signed with the same key. Android refuses to update an installed
term0 with an APK signed by any other key, and the certificate fingerprint above lets
you check a downloaded file yourself:

```
apksigner verify --print-certs term0-1.0.04.apk
```

`latest.json` is signed with a separate Ed25519 key (`latest.json.sig`); the app
ignores it unless the signature verifies.

### Changes

- first release signed with its own key
- the app checks for new versions and offers to download them
- capsules without a password, QR codes from the gallery, encryption and destruction animations
