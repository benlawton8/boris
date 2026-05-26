---
name: boris-client-config
description: Boris's saved settings for this account. Boris reads this every time he runs.
metadata:
  type: project
---

# Boris config

Boris fills this in during the first-run wizard (3 questions + auto-detect). After that he reads it every time and never asks again. Edit by hand only if something changes (new town, new business name, different budget).

## The 4 you give Boris
- **Your name**: <first name>
- **Business name**: <Their Business Name>
- **Town**: <Swindon, UK>
- **Radius (miles)**: <17>
- **Email for the daily report**: <them@theirdomain.com>

## What Boris worked out himself
- **Meta location key**: <resolved via Meta MCP geo search>
- **Meta ad account**: <act_XXXXXXXXX>
- **Currency**: <GBP>
- **Facebook Page ID**: <numeric>
- **Instagram username**: <@theirhandle>
- **Instagram user ID**: <numeric>

## Budgets
- **Cold daily budget**: <£20>
- **Retargeting daily budget**: <£5> (built only when you ask)
- **Winners daily budget**: <£40-60> (built once Cold has a proven winner)

## KPI targets (the two numbers Boris watches)
- **Cost per follow**: target under £2-£3
- **Profile visit -> follow conversion**: target above 10%
- **Winner threshold**: 15+ follows of data, cost/follow under £3, conversion above 10%
- **Auto-prune threshold**: > £30 spent AND (zero follows OR cost/follow > £6) -> pause

## Daily check-in
- **Daily pulse**: <email | none>
- **Pulse email address**: <them@theirdomain.com>
- **Pulse delivery**: <gmail | local-file>

## MCP in use
- **MCP**: <meta-ads (official) | pipeboard (fallback)>

## Their top organic reels (last 90 days)
<Boris auto-fills the top 10 each scan: shortcode - views - caption snippet. Refresh every few weeks.>

## Live campaigns
<Boris auto-fills as he builds: campaign name - ID - status - budget.>

## Notes
<Anything Boris learns about this account that future-Boris should know.>
