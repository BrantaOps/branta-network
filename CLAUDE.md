# Branta Network

This repo is a data-only registry. It backs the partner directory at https://www.branta.pro/network and accepts PRs from integrators that want to be listed.

## Contents
- `data.json` — the entire registry. Two top-level arrays:
  - `wallets` — `{ name, logo, website_url, block_height }`. `block_height` is the Bitcoin block at which the integration shipped.
  - `btcpay` — BTCPay Server instances that run the Branta plugin: `{ name, logo, website_url }` (no block_height).
- `README.md` — documents the entry format users should follow when opening a PR.
- `.github/workflows/lint.yml` — CI runs `jsonlint` over every `*.json` in the repo on push and PR to `main`.

## When editing
- Adding a partner = appending one object to the matching array in `data.json`. Keep keys in the order shown in the README (`name`, `logo`, `website_url`, then `block_height` for wallets).
- `logo` URLs are remote; do not commit binary assets.
- The file must stay valid JSON — CI fails the PR otherwise. Avoid trailing commas.
- There is no build step, no package manifest, and no application code here. Do not introduce one without an explicit reason.
