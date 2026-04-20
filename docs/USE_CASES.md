# Use cases & playbooks (GA4 + GSC MCP)

All examples assume the hosted server is connected:

- Server URL: `https://www.sellonllm.com/api/mcp`

Ask Claude to **list GA4 properties and GSC sites first** if you have more than one.

---

## 1. Weekly organic health check (15 min)

**Goal:** Catch regressions early without building a new Looker Studio dashboard every week.

**Prompt idea:**

```text
Weekly organic health check for the last 7 days vs the prior 7 days:

1) GA4: organic sessions, engaged sessions, engagement rate, top 15 landing pages by sessions with % change
2) GSC: clicks, impressions, avg CTR, avg position — same periods
3) Top 20 queries by impression change (winners and losers)
4) Flag anything that moved more than 15% week-over-week and hypothesize why (seasonality, SERP layout, deployment, tracking)

End with 5 prioritized actions for this week.
```

---

## 2. CTR rescue after a rewrite or migration

**Goal:** Find URLs where impressions held but CTR collapsed (snippet, intent mismatch, or SERP feature shift).

**Prompt idea:**

```text
For the last 28 days vs the previous 28 days, find pages where impressions were stable (±10%) but CTR dropped by more than 0.3 percentage points (or >20% relative drop).

For each page:
- show top queries, impressions, CTR, position for both periods
- propose 2 title variants and 2 meta description variants
- note if branded vs non-branded mix likely changed

Summarize sitewide patterns.
```

---

## 3. “Almost page one” content sprint

**Goal:** Prioritize pages ranking ~4–15 with meaningful impressions.

**Prompt idea:**

```text
Using Search Console for the last 90 days, find URLs with average position between 4 and 15 and impressions > 500.

For the top 12 URLs:
- list top 8 queries each
- recommend H2/H3 outline additions, FAQ schema where appropriate, and internal links from 3 existing URLs each
- estimate effort (S/M/L) and expected impact (H/M/L)

Produce a 2-week execution order.
```

---

## 4. Post-release engineering verification

**Goal:** Tie a deploy or template change to measurable organic deltas.

**Prompt idea:**

```text
We deployed on [DATE]. Compare GA4 organic landing pages and GSC page performance for the 7 days before vs the 7 days after.

Highlight URL patterns (e.g. /blog/, /docs/, /product/) that moved. Separate likely tracking issues from real demand/CTR/position changes.
```

---

## 5. Stakeholder narrative (non-technical)

**Goal:** One email your CEO can read.

**Prompt idea:**

```text
Write a 250-word email to a non-SEO executive summarizing last month’s organic search performance.

Use bullets only in the middle. Include: overall trend, top win, top risk, one technical follow-up, one content follow-up. Tone: confident, cautious, no jargon without definitions.

Base everything strictly on our GA4 + GSC data for the last 28 days vs prior 28 days.
```

---

## 6. Agency: client onboarding snapshot

**Goal:** First-week deliverable without manual export gymnastics.

**Prompt idea:**

```text
Create a client onboarding SEO snapshot for the last 28 days:

1) Property + site confirmation (list if ambiguous)
2) Top 15 queries and top 15 landing pages
3) CTR opportunity table (top 10)
4) Ranking opportunity table (positions 4–15, top 10)
5) Three quick wins and three strategic bets for the next 90 days

Assume the reader is the client’s marketing lead, not an SEO specialist.
```

---

## More copy/paste blocks

See also [`PROMPTS.md`](PROMPTS.md) on this repo and the [SellOnLLM MCP page](https://www.sellonllm.com/google-analytics-mcp-claude.html).
