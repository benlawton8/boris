---
name: boris-client-config
description: Boris's saved settings. Holds 1..N client blocks. Boris reads this every run, then live-scans Meta to confirm what's really there.
metadata:
  type: project
---

# Boris config

This file holds one or more **client blocks**. Each block is one ad account / one business. Boris reads the whole file every run, then live-scans Meta to confirm what's actually running. The file is a notepad, not the truth — if Meta says something different, Boris rewrites the block to match.

Boris **appends** a new block during onboarding. He never overwrites an existing one (unless you tell him to).

If only one client exists, Boris uses it. If more than one, he asks: "Which client — or all of them?"

---

## clients

### client: <slug — e.g. ben-lawton or acme-video>

**The 4 you give Boris**
- **Your name**: <first name>
- **Business name**: <Their Business Name>
- **Town**: <Swindon, UK>
- **Radius (miles)**: <17>
- **Email for the daily report**: <them@theirdomain.com>

**What Boris worked out himself**
- **Meta location key**: <resolved via geo search>
- **Meta ad account**: <act_XXXXXXXXX>
- **Currency**: <GBP>
- **Facebook Page ID**: <numeric>
- **Instagram username**: <@theirhandle>
- **Instagram user ID**: <numeric>

**Budgets**
- **Cold daily budget**: <£20>
- **Retargeting daily budget**: <£5> (built only when asked)
- **Winners daily budget**: <£40-60> (built once Cold has a proven winner)

**KPI targets**
- **Cost per follow**: target under £2-£3
- **Profile visit -> follow conversion**: target above 10%
- **Winner threshold**: 15+ follows, cost/follow under £3, conversion above 10%
- **Auto-prune threshold**: > £30 spent AND (zero follows OR cost/follow > £6) -> pause

**Daily check-in**
- **Daily pulse**: <email | none>
- **Pulse email address**: <them@theirdomain.com>
- **Pulse delivery**: <gmail | local-file>

**MCP in use**
- **MCP**: <meta-ads (official) | pipeboard (fallback) | other namespace>

**Meta access token**
- **Token path**: `~/.claude/projects/<project>/memory/boris_secrets.env` (key `META_TOKEN_<slug>`). Never paste the token into this file. Boris reads it from the env file at runtime. System User token preferred (non-expiring), with `ads_management`, `ads_read`, `business_management`, `pages_*`, `instagram_*` scopes.

**Known account facts** (auto-filled by Boris as he discovers them — saves re-discovering each run)
- **GBP min campaign_spend_cap**: 10000 pence (£100). Other currencies: assume equivalent until proven otherwise.
- **Audience-read MCP rolled out for this account**: <yes | no> (irrelevant — Boris uses Graph API direct either way, but useful to know)
- **Business verification status**: <verified | pending | unknown> (if pending, all new ads need UI Republish for the Voluntary Verification flag)

**Confirmed audiences** (auto-filled from live audience reads)
| Name | ID | Subtype | Size bucket | Last updated | Health |
|---|---|---|---|---|---|
| <e.g. IG Engagers 90d> | <120...> | ENGAGEMENT | <Medium> | <YYYY-MM-DD> | <Ready | Stale | Building> |

**Their top organic reels (last 90 days)**
<Boris auto-fills the top 10 each scan: shortcode - views - caption snippet. Refresh every few weeks.>

**Live campaigns** (auto-filled from Meta live-scan — never trust without re-scanning)
| Campaign | ID | Status | Budget | Notes |
|---|---|---|---|---|
| Cold - <town> | <id> | ACTIVE | <£/day> | <notes> |
| Retargeting - <town> | <id> | PAUSED | <£/day> | propose-only, not built yet |
| Winners - <town> | <id> | — | — | not built yet |

**Notes**
<Anything Boris learns about this account that future-Boris should know.>

---

### client: <next-slug>

(repeat the same block structure for each additional client/account)

---

## How Boris reads this file

1. Glob all `### client:` headings.
2. If one, use it.
3. If more than one, ask the user which client(s) to run on this invocation.
4. For each selected client, live-scan Meta and reconcile the **Live campaigns** table.
5. If anything's stale, rewrite that block in place and tell the user one line about what changed.
