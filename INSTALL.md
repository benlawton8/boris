# Meet Boris - your local Instagram ads agent

Boris is a robot that runs your Instagram follower ads in your local town.

He builds your campaigns, watches your spend, and tells you what's working - all inside Claude Code. He talks plain English. He never spends your money without asking first.

He already knows everything we learned the hard way: the Meta bugs, the dead ends, the exact settings that win. You skip all the pain.

---

## What Boris does

- **Cold campaign** - wins you brand new followers from your town (17-mile radius around you)
- **Retargeting** - catches people who watched your stuff but didn't follow (ready when you ask)
- **Warm funnel** - turns followers into leads (ready when you ask)
- **Daily report** - a short morning email on how it's all going

He reads your own Instagram reels to build the ads. Your best organic content becomes your best ads. He targets local people in your town - the kind of service-based business owners who hire videographers.

---

## Before you start - you need 3 things

1. Claude Code installed on your computer. (If you're reading this in Claude Code, you've got it.)
2. A Meta Business account with an ad account - the thing you'd use to boost a post. Card on file.
3. An Instagram business or creator account linked to a Facebook Page.

That's it. Don't have an ad account? Make one free at business.facebook.com first.

---

## Setup - 3 steps, about 5 minutes

### Step 1 - Install Meta's official MCP

Meta released its own free MCP in April 2026. It's the proper, official way for Boris to talk to your ad account. In your terminal, paste this one line and press enter:

```
claude mcp add --transport http meta-ads https://mcp.facebook.com/ads
```

A window pops up to log in with Facebook. Use the account that owns your business. Say yes. Done.

That's the same Meta system you log into at business.facebook.com - just connected to Claude Code now.

### Step 2 - Drop Boris in

Boris is one file. Copy this one line, paste it in your terminal, press enter:

```
mkdir -p ~/.claude/agents && curl -s https://raw.githubusercontent.com/benlawton8/boris/main/boris.md -o ~/.claude/agents/boris.md
```

No files to make, no copy-pasting big blocks of text. One line and Boris is in.

### Step 3 - Run Boris

Open Claude Code and type:

```
run Boris
```

Boris takes over from here.

---

## What happens on your first run

Boris only asks you **three things**:

1. **Your first name** (he uses it in the daily report)
2. **Your business name** (Meta puts it on the ad's legal small print)
3. **What town you cover** (he runs the ads in a 17-mile radius around it)

Everything else - your ad account, your Facebook Page, your Instagram, your currency, the budget - he checks himself and tells you what he found.

He'll also ask Claude Code for permission to use the Meta MCP. Say yes - that's how he reaches your ad account.

Then Boris:
1. Pulls your top 10 best-viewed reels from the last 90 days
2. Shows you the list - you cross out any you don't want
3. Builds a cold follower campaign, paused, for you to check (20/day default, 17-mile radius around your town)
4. Tells you exactly what to click in Meta Ads Manager to turn it on

He saves all your details. He never asks twice.

---

## What Boris's daily report looks like

Here's a sample morning report, so you know what to expect:

```
Boris - your ads, yesterday (Tue 3 Jun)

Spent: 19.40
Best ad: "Behind the scenes shoot" - 78p a follower. Solid.
Paused: "Comment 50" - £32 spent, 0 follows. Killed it.
Do this: nothing - let it run. Too early to judge the rest.
```

Short. Honest. Tells you what to do, or tells you to do nothing. That's the whole point.

---

## Common questions

How much will the ads cost me?
Whatever budget you set. Boris suggests 20/day for cold + 5/day each for retargeting and warm. That's about 30/day total. You control it. Boris will never go over without asking.

Will Boris spend my money on its own?
No. He shows you a plan, you say yes, then he builds it - paused, so you double-check. The one exception is the daily prune: if an ad has spent more than £30 and got zero follows, he pauses it and tells you. That's it.

Why is my first ad showing an error?
Normal. If Meta hasn't fully verified your business, new ads show a warning. Open Meta Ads Manager, click "Republish" on each new ad once. Fixed. It stops once Meta verifies you.

It says "MCP not connected"?
You skipped Step 1. Go back and run the `claude mcp add` line.

Do I need to be techy?
No. Boris does the technical bit. You just answer his three questions and say yes or no.

Why broad targeting only my town?
The town is the qualifier. Your future customers are local business owners IN your area. Layering interests on top of a small geo kills reach. Geo + your reels does the work.

---

## Need help?

Ask in the masterclass group. Or just tell Boris what's wrong - he's good at explaining.

Now go run Boris.
