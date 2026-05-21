# Boris - your Instagram ads agent

Boris is a Claude Code agent that builds and runs Instagram follower ads for videographers and creatives.

He runs a 3-stage local funnel:
- Cold - win new followers in your area
- Retargeting - catch people who looked but didn't follow
- Warm funnel - turn followers into leads

He targets the local service-based businesses who hire videographers - not other videographers. He reads your own Instagram reels for ad ideas, watches your spend, and emails you a short daily report. He never spends money or changes a campaign without you saying yes.

## Install

Full step-by-step is in [INSTALL.md](INSTALL.md). Short version:

1. Make a Pipeboard account at [pipeboard.co](https://pipeboard.co)
2. Connect it to Claude Code:
   ```
   claude mcp add --transport http pipeboard-meta-ads https://meta-ads.mcp.pipeboard.co/
   ```
3. Drop Boris in:
   ```
   mkdir -p ~/.claude/agents && curl -s https://raw.githubusercontent.com/benlawton8/boris/main/boris.md -o ~/.claude/agents/boris.md
   ```
4. In Claude Code, type: `run Boris`

Boris walks you through the rest.

## What's in this repo

| File | What it is |
|---|---|
| `boris.md` | The agent. This is the file that goes in `~/.claude/agents/`. |
| `INSTALL.md` | Full setup guide for non-technical users. |
| `boris_config_template.md` | The settings file Boris writes on first run (for reference). |

## Requirements

- Claude Code
- A Meta Business account + ad account
- An Instagram business/creator account linked to a Facebook Page
- A Pipeboard account (free plan works to start)

## Built by

Ben Lawton / Self Made Creatives - for the videography coaching masterclass.
