# term0 releases

Signed release builds of term0. The app checks `latest.json` here at most once a day.

## Latest: 1.5.00

| | |
|---|---|
| File | [`releases/term0-1.5.00.apk`](releases/term0-1.5.00.apk) |
| SHA-256 | `8def7d72cc891b80e586c4544178c144dcb9f2f48160b048ad5947a634296cb3` |
| Size | 5752344 bytes |
| Signing certificate SHA-256 | `f96442f355261c5c8701dfd94a8aeb06776bf5cc680f4567637ecdc8c81fb00b` |

Every release is signed with the same key. Android refuses to update an installed
term0 with an APK signed by any other key, and the certificate fingerprint above lets
you check a downloaded file yourself:

```
apksigner verify --print-certs term0-1.5.00.apk
```

`latest.json` is signed with a separate Ed25519 key (`latest.json.sig`); the app
ignores it unless the signature verifies.

### Changes

- decoy message: a password capsule can carry a second message under a second password, for a recipient who is forced to open it
- the decoy password shows the decoy and destroys the real message for good; nobody can prove a decoy exists
- the decoy password can be generated or typed in
- passwords can be selected and copied; copies are marked as sensitive
- the receipt shows whether the capsule was opened with the real or the decoy password
- the password QR code can be shared to another app
- mandatory update: older versions cannot open new capsules
