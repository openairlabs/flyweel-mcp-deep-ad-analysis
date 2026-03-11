# Flyweel MCP Ad Analysis

A Claude Code skill for analysing Google Ads and Meta Ads performance using the [Flyweel](https://flyweel.co) MCP server.

Turns your live ad data into actionable media buying insights. Optimises MCP tool usage by batching queries, checking data freshness, and structuring results like a senior performance marketer.

## What It Does

- **Orients automatically** — checks setup status, connection state, and data freshness before querying
- **Batches queries efficiently** — combines up to 5 queries per `query_metrics` call to minimise round trips
- **Covers the full funnel** — ads metrics (spend, CPC, CTR, conversions) plus CRM metrics (deals, revenue, win rate) when available
- **Delivers analysis, not data dumps** — every response includes headline findings, trend direction, and specific recommendations
- **Handles edge cases** — guides users through connection, account selection, and sync when data is missing

## Included Playbooks

| Playbook | Purpose |
|---|---|
| Performance Overview | Weekly check-in with WoW comparisons |
| Budget Efficiency Audit | Find wasted spend and optimisation opportunities |
| Channel Comparison | Google vs Meta head-to-head with reallocation recs |
| Campaign Deep Dive | Daily-level analysis with fatigue and learning phase detection |
| Full Funnel | Connect ad spend to CRM pipeline and real revenue |

## Prerequisites

- A [Flyweel](https://flyweel.co) account with at least one ad platform connected (Google Ads and/or Meta Ads)
- The Flyweel MCP server configured in your Claude Code, ChatGPT, or MCP client

## Installation

```bash
# Via skill.fish
claude skill install flyweel/flyweel-mcp-ad-analysis-by-flyweel.co

# Manual
git clone https://github.com/flyweel/flyweel-mcp-ad-analysis-by-flyweel.co.git ~/.claude/skills/flyweel-mcp-ad-analysis-by-flyweel.co
```

## Usage

The skill activates when you ask about ad performance with the Flyweel MCP connected:

```
"How are my Google Ads performing this month?"
"Compare Google and Meta spend efficiency over the last 90 days"
"Which campaigns should I pause?"
"Give me a full funnel analysis — ads through to CRM revenue"
```

## Available Metrics

**Ads:** spend, impressions, clicks, conversions, reach, CTR, CPC, CPM, conversion rate, cost per conversion

**CRM:** deals created/won/lost/open, revenue, pipeline value, avg deal size, win rate, velocity days

**Dimensions:** channel, account, campaign, status, currency, date/week/month, stage, lead source, deal status

## Built by Flyweel

Originally built by [Flyweel](https://flyweel.co) — we're building the layer connecting spend, revenue, and capital with agentic finance.

## License

MIT
