# term0 releases

Signed release builds of term0. The app checks `latest.json` here at most once a day.

## Latest: 1.2.00

| | |
|---|---|
| File | [`releases/term0-1.2.00.apk`](releases/term0-1.2.00.apk) |
| SHA-256 | `211ca4a77165d5789b667600138a6665023569addc0eeb5cc1fd408da26bc396` |
| Size | 5708564 bytes |
| Signing certificate SHA-256 | `f96442f355261c5c8701dfd94a8aeb06776bf5cc680f4567637ecdc8c81fb00b` |

Every release is signed with the same key. Android refuses to update an installed
term0 with an APK signed by any other key, and the certificate fingerprint above lets
you check a downloaded file yourself:

```
apksigner verify --print-certs term0-1.2.00.apk
```

`latest.json` is signed with a separate Ed25519 key (`latest.json.sig`); the app
ignores it unless the signature verifies.

### Changes

- sender receipt: check later whether a capsule was opened, destroyed or expired
- proof of work: every attempt to open costs a little computing, slowing attacks on many capsules
- option to show a message only while holding a finger on it
- codes of capsules without a password no longer travel in kapsula:// links
- mandatory update: older versions do not work with the new server
