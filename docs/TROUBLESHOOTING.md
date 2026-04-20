# Troubleshooting

Hosted MCP server:

- `https://www.sellonllm.com/api/mcp`

## “Authorization failed” but I think it connected

Some clients show a UI error even when tools work. Try asking a concrete question like:

> “List my GA4 properties.”

If the assistant calls tools and returns properties/sites, you’re connected.

## I can’t see any tools

1. Confirm the connector is added and **enabled**.
2. Remove the connector and re-add it using the exact server URL.
3. Ensure you signed into the correct Google account (the one with GA4/GSC access).

## Google consent screen blocks me (Testing mode)

If the Google OAuth app is still in **Testing**, only approved **test users** can connect. For a public launch, the OAuth app must be configured for production and scopes may require Google verification.

## I have multiple GA4 properties / GSC sites

Ask the assistant to list options first, then specify the one you want:

> “Use GA4 property X and GSC site Y for the rest of this conversation.”

## Getting help

When filing an issue, include:

- Which client: Claude Web / Claude Desktop / Cursor
- The approximate timestamp
- What you expected vs what happened
- A redacted screenshot of the error (avoid sharing secrets)

