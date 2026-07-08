# SaturnShift Partner API docs

Mintlify docs for the SaturnShift Partner API, to be published at **docs.saturnshift.io**.

## Files

| File | Purpose |
| --- | --- |
| `docs.json` | Mintlify config: theme, colors, navigation, API Reference tab |
| `openapi.json` | OpenAPI 3 spec. Mintlify auto-generates the API Reference + playground from it |
| `introduction.mdx` | Overview |
| `quickstart.mdx` | Four-step get-started |
| `authentication.mdx` | OAuth2 client_credentials guide |
| `webhooks.mdx` | Event catalog, payloads, signature verification, retries |

## Preview locally

```bash
npm i -g mint
mint dev
```

Opens a live preview at `http://localhost:3000`.

## Deploy

1. Push this folder to a GitHub repo.
2. Create a Mintlify account (Starter is free and includes custom domains) and install the Mintlify GitHub app on the repo.
3. Every push to the default branch auto-deploys.

## Custom domain (docs.saturnshift.io)

1. In the Mintlify dashboard: Settings, Custom Domain, enter `docs.saturnshift.io`.
2. Add the CNAME record it gives you to your DNS (`docs` -> the Mintlify target).
3. Wait for propagation. The docs then serve only at `docs.saturnshift.io`.

## Before you publish, confirm these placeholders

- **API host.** The spec and guides use `https://api.saturnshift.io`. If your production API is served from a different host, find-and-replace it across `openapi.json`, `authentication.mdx`, `quickstart.mdx`, and `webhooks.mdx`.
- **Branding assets.** Add `favicon.svg` (referenced in `docs.json`) and, if you want a wordmark, a `logo/` with light and dark variants plus a `logo` block in `docs.json`.
- **Dashboard link.** `docs.json` points the navbar button at `https://app.saturnshift.io`. Adjust if needed.
