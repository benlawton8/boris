# Boris - your local Instagram ads agent

Boris is a Claude Code agent that builds and runs Instagram follower ads for videographers - locally, in their own town.

He runs a simple local funnel:
- **Cold** - win new followers in your town (17-mile radius)
- **Retargeting** - stay in front of the warm pool (90-day engagers + existing followers)
- **Winners** - scale what's already working (built after Cold proves a winner)

He reads your own Instagram reels for ad ideas, watches your spend, and emails you a short daily report. The two numbers he watches: cost per follow under £2-£3, and profile visit → follow above 10%. He never spends money or changes a campaign without you saying yes - except a strict daily prune that pauses ads burning money with no follows.

## Install

Full step-by-step is in [INSTALL.md](INSTALL.md). Short version:

1. Install Meta's official MCP:
   ```
   claude mcp add --transport http meta-ads https://mcp.facebook.com/ads
   ```
2. Save a Meta access token so Boris can use Graph API direct (see INSTALL.md Step 2 — takes 2 mins).
3. Install the Gmail MCP (for the daily report):
   ```
   claude mcp add gmail npx -y @gongrzhe/server-gmail-autoauth-mcp
   ```
4. Drop Boris in:
   ```
   mkdir -p ~/.claude/agents && curl -s https://raw.githubusercontent.com/benlawton8/boris/main/boris.md -o ~/.claude/agents/boris.md
   ```
5. In Claude Code, type: `run Boris`

Boris asks 4 things (your name, business name, town, email) and works the rest out himself.

## What's in this repo

| File | What it is |
|---|---|
| `boris.md` | The agent. This is the file that goes in `~/.claude/agents/`. |
| `INSTALL.md` | Full setup guide for non-technical users. |
| `boris_config_template.md` | The settings file Boris writes on first run (for reference). |

## Requirements

- Claude Code
- A Meta Business account + ad account with a card on it
- An Instagram business/creator account linked to a Facebook Page
- Meta's official MCP installed (free, the proper path)
- A Meta System User access token (free, 2-min setup — needed for the Graph API gaps the MCP doesn't cover)
- The local Gmail MCP installed (free, for the daily report)

## Built by

Ben Lawton / Self Made Creatives - for the videography coaching masterclass.
