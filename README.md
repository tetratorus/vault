# vault

Extensible `age`-encrypted personal vault backed by GitHub Releases and live GitHub Environment approval (`unlock`).

- Encrypted data lives in GitHub Releases (`<namespace>-<id>`), keeping this Git tree tiny.
- Each scope `<namespace>/<id>` uses an independent `age` key derived via `HMAC-SHA256(MASTER_KEY, scope)`.
- Unlocking any scope triggers `.github/workflows/unlock.yml`, pauses for required-reviewer approval on GitHub Mobile, and wraps only that scope's key to a one-time ephemeral `age` public key.

## Namespaces

- `screen-history/` — macOS `ascii-screen` history (`screen-history-YYYY-MM-DD` releases).
