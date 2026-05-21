# Meet Boris — your Instagram ads agent 🤖

Boris is a robot that runs your Instagram follower ads for you.

He builds your campaigns, watches your spend, and tells you what's working — all inside Claude Code. He talks plain English. He never spends your money without asking first.

He already knows everything we learned the hard way: the Meta bugs, the dead ends, the exact settings that win. You skip all the pain.

---

## What Boris does

- **Cold campaign** — wins you brand new followers in your local area
- **Retargeting** — catches people who watched your stuff but didn't follow
- **Warm funnel** — turns followers into leads (free guide, YouTube, "comment to get it")
- **Daily report** — a short morning email on how it's all going

He reads your own Instagram reels to build the ads. Your best organic content becomes your best ads.

---

## Before you start — you need 3 things

1. **Claude Code** installed on your computer. (If you're reading this in Claude Code, you've got it.)
2. **A Meta Business account** with an ad account — the thing you'd use to boost a post.
3. **An Instagram business or creator account** linked to a Facebook Page.

That's it. Don't have an ad account? Make one free at business.facebook.com first.

---

## Setup — 4 steps, about 10 minutes

### Step 1 — Get Pipeboard

Boris talks to Meta through a tool called **Pipeboard**. Think of it as the phone line between Boris and your ad account.

1. Go to **pipeboard.co**
2. Make an account. The **free plan** is fine to start (30 actions a week). Pro is ~$30/mo if you want more.

### Step 2 — Connect Pipeboard to Claude Code

In your terminal, paste this one line and press enter:

```
claude mcp add --transport http pipeboard-meta-ads https://meta-ads.mcp.pipeboard.co/
```

A window pops up to log in with Facebook. Say yes. Done.

### Step 3 — Drop Boris in

Boris is one file. Put it where Claude Code keeps its agents.

**The easy way:**
1. Make a new file at `~/.claude/agents/boris.md`
2. Open the `boris.md` from this pack (or copy it from the box below / from GitHub)
3. Paste it all in. Save.

**The techy way** (if you know git):
```
mkdir -p ~/.claude/agents && curl -s https://raw.githubusercontent.com/benlawton8/boris/main/boris.md -o ~/.claude/agents/boris.md
```

### Step 4 — Run Boris

Open Claude Code and type:

```
run Boris
```

That's it. Boris takes over from here.

---

## What happens on your first run

Boris asks you a few quick questions:

- What town do you cover, and how far out (25 / 50 / 100 miles)
- Your Meta ad account number (`act_...`)
- Your Facebook Page and Instagram handle
- Your business name
- Your daily budget (most start at £20)
- Do you want a daily report email

Then Boris:
1. Looks at your best Instagram reels from the last 90 days
2. Shows you a plan for a **cold follower campaign** — local area, £20/day
3. You say yes — he builds it **paused** so you can check it
4. You flip it on when you're happy
5. He shows you the retargeting and warm funnel plans, ready when you want them

He saves all your details. He never asks twice.

---

## What Boris's daily report looks like

Here's a sample morning report, so you know what to expect:

```
Boris — your ads, yesterday (Tue 3 Jun)

Spent: £19.40 (Cold £19.40, Retargeting not on yet)
Best ad: "Wedding film teaser" — 31p a profile visit. Cheap. Good.
Broken: nothing.
Do this: nothing — let it run. Too early to judge, only 2 days in.
```

Short. Honest. Tells you what to do, or tells you to do nothing. That's the whole point.

*(Bonus: ask Ben to show you a real one from his own account on the call.)*

---

## Common questions

**How much will the ads cost me?**
Whatever budget you set. Boris suggests £20/day for cold + £5/day each for retargeting and warm. That's ~£30/day total. You control it. Boris will never go over without asking.

**Will Boris spend my money on its own?**
No. Never. Boris shows you a plan, you say yes, then he builds it — usually paused first so you double-check. Changing budgets always needs your yes.

**Why is my first ad showing an error?**
Normal. If Meta hasn't verified your business yet, new ads show a warning. Open Meta Ads Manager, click "Republish" on each new ad once. Fixed. It stops once Meta verifies you.

**It says "Pipeboard not connected"?**
You skipped Step 2. Go back and run the `claude mcp add` line.

**Do I need to be techy?**
No. Boris does the technical bit. You just answer his questions and say yes or no.

---

## Need help?

Ask in the masterclass group. Or just tell Boris what's wrong — he's good at explaining.

Now go run Boris. 🚀
