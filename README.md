# SellOnLLM Analytics MCP (GA4 + GSC) — Hosted Connector

Use your **Google Analytics 4** and **Google Search Console** data inside AI assistants via a **hosted** MCP server.

- **No Vercel required**
- **No database required**
- **Just connect in Claude** (OAuth + read-only scopes)

## Quick start (Claude)

1. Open `claude.ai` → **Settings** → **Connectors**
2. Click **Add custom connector**
3. Paste this **Server URL**:
   - `https://www.sellonllm.com/api/mcp`
4. Click **Connect**, then sign in with Google and approve read-only access

That’s it—Claude will discover tools automatically.

## What this is

This repository documents the **SellOnLLM-hosted MCP server**. The server is operated by SellOnLLM and exposes read-only tools for GA4 and Search Console analysis (SEO / AEO / GEO workflows).

- **Hosted MCP server URL**: `https://www.sellonllm.com/api/mcp`
- **Website setup guide**: `https://www.sellonllm.com/google-analytics-mcp-claude.html`

## Copy/paste prompts

See `docs/PROMPTS.md`.

## Tools available

See `docs/TOOLS.md`.

## Security model (high-level)

- OAuth sign-in with Google (we never see your Google password)
- Read-only Google scopes (Analytics + Search Console)
- Claude receives **SellOnLLM access tokens**; Google refresh tokens stay server-side and encrypted

Details: `docs/SECURITY.md`

## Troubleshooting

See `docs/TROUBLESHOOTING.md`.

## Discoverability (GitHub Topics to add)

On GitHub, add topics like:

`mcp`, `model-context-protocol`, `claude`, `ga4`, `google-analytics`, `google-search-console`, `search-console`, `seo`, `aeo`, `geo`, `oauth2`

## Support

- Open an issue in this repo with: what client (Claude Desktop / Claude Web / Cursor), timestamp, and what you tried.
- If you have access to SellOnLLM support, include your SellOnLLM account email.

