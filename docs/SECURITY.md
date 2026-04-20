# Security & privacy (hosted MCP)

This repository documents a **hosted** MCP server operated by SellOnLLM:

- `https://www.sellonllm.com/api/mcp`

## What the assistant can access

After you connect and approve Google OAuth, the server can read:

- Google Analytics 4 (GA4) reporting data
- Google Search Console (GSC) performance data

The intended posture is **read-only** (no mutations to GA/GSC settings).

## OAuth and tokens (high level)

- You authenticate with Google via OAuth in your browser.
- The assistant (e.g., Claude) calls the MCP server using **SellOnLLM-issued access tokens**.
- Google refresh tokens remain **server-side** and are stored **encrypted** to allow ongoing access without repeated logins.

## What we do not see

- We do not see your Google password (Google handles authentication).

## What to do if you want to revoke access

- Remove the connector from your AI client (Claude/Cursor).
- Revoke SellOnLLM access in your Google account’s third-party app permissions.

## Responsible usage

AI outputs should be treated as **draft analysis**. Verify important decisions (content changes, technical SEO changes) directly in GA/GSC and your CMS before shipping.

