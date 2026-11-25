# screen-history

Encrypted macOS `ascii-screen` history, synced every 5 minutes as GitHub Releases tagged `screen-history-YYYY-MM-DD`.

Each release contains:
- `HH00.gz.age` / `HH30.gz.age` — 30-minute slices of native `ascii-screen` gzip members
- `keyframes.gz.age` — 1 frame every 5 minutes (valid `YYYY-MM-DD.txt.gz`)
- `index.gz.age` — deduplicated per-minute inverted word index
- `manifest.json.age` — hourly frame counts and chunk list
