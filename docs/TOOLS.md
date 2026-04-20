# Tools (SellOnLLM Analytics MCP)

This MCP server is hosted by SellOnLLM:

- `https://www.sellonllm.com/api/mcp`

Exact tool names can evolve, but the connector is designed around these categories:

## Discovery

- **List GA4 properties**: enumerate GA4 properties the signed-in Google account can access.
- **List Search Console sites**: enumerate verified GSC sites the account can access.

## GA4 reporting

- **Flexible GA4 query**: request metrics/dimensions over a date range, often with filtering and sorting.
- **Traffic deltas**: compare last N days vs previous N days by landing page (usually organic).

## Search Console reporting

- **Flexible GSC query**: query clicks, impressions, CTR, position by query/page/device/country/date.
- **CTR opportunities**: find high-impression queries/pages with low CTR.
- **Ranking opportunities**: find pages/queries in the “close to page 1” range (e.g., position 4–15).

## Combined SEO snapshot

- **SEO snapshot**: a combined, opinionated summary (GA4 + GSC) intended for quick briefings and weekly/monthly reviews.

