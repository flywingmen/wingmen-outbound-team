# Outbound Team for Claude

**Your outbound team, inside Claude.** Eleven agents that find buyers showing real intent, score every lead with a written reason, write from the signal, and run LinkedIn outreach for you. Nothing sends until you say yes.

Built for founders who are still their own best salesperson and have no time left to prospect.

## The team

| Agent | Job |
|---|---|
| **Head of Outbound** | Reads your workspace, picks the next move, routes the work, enforces the approval rule |
| **Targeting Strategist** | Turns your website into who to hunt, and fixes it when the leads look wrong |
| **Signal Hunter** | Builds warm lists from the people commenting on a post, or from your own network |
| **Lead Judge** | Approves the real leads with a reason a stranger could check, dismisses the rest |
| **Account Researcher** | Finds one honest angle per person: why them, why now. Says "no fresh trigger" instead of inventing one |
| **Copywriter** | Writes from the signal, under 80 words, and strips the AI tells |
| **Campaign Operator** | Creates agents, switches them on after your yes, runs hand-written campaigns, pauses anything at once |
| **Inbox Closer** | Works everyone waiting on you, drafts every reply, sends only what you approve |
| **Follow-up Agent** | Keeps warm threads alive: one nudge with something new, one close-out, then stops |
| **Meeting Qualifier** | Protects your calendar: book, ask one question, or pass |
| **Pipeline Analyst** | A five-line weekly review: what booked calls, where it leaks, the one change to make |

## How the work flows

```
Your website
   ↓  Targeting Strategist sets who to hunt
Lead Radar finds and scores people daily
   ↓  Lead Judge approves the real ones, each with a written reason
Approved list
   ↓  Campaign Operator creates a paused agent, you say yes, it goes live
Replies
   ↓  Inbox Closer drafts the answer, you approve, it sends
   ↓  Interested → Meeting Qualifier. Warm but quiet → Follow-up Agent
Every Friday
   ↓  Pipeline Analyst tells you which source turns into calls
```

## Three rules every agent follows

1. **Nothing goes out without your yes.** Every send, launch, approval or targeting change is two calls: a preview with a signature, then the real thing only after you approve that exact preview.
2. **No signal, no message.** A job title is a filter, not a reason. If the agent cannot quote what the person said or did, the lead waits.
3. **Every score has a written reason.** "8: posted 6 days ago that their SDR left, also hiring a BD role." Never "8: good fit."

## Commands

| Command | Does |
|---|---|
| `/outbound-setup [website]` | Targeting from your site, shown before anything is saved |
| `/leads` | Work the queue: approve or dismiss, with reasons |
| `/warm-list [post link or description]` | A warm list from a post's commenters or your connections |
| `/launch [list]` | An agent on an approved list, previewed, then switched on |
| `/inbox` | Who is waiting on you, with replies drafted |
| `/pipeline` | The weekly five-line review |

## Install

**Claude Code**

```
/plugin marketplace add flywingmen/wingmen-outbound-team
/plugin install outbound-team@wingmen
```

The plugin connects the Wingmen MCP for you. Sign in with your Wingmen account when Claude asks.

**Claude desktop or claude.ai**

Settings → Connectors → Add custom connector → `https://app.flywingmen.com/api/mcp`. Then add the files in `skills/outbound-team/` as a skill, or paste `SKILL.md` into a project.

**Codex, Cursor, Grok and other agent hosts**

Clone the repo into your project. `AGENTS.md` is the entry point: it routes every request to the right agent. Connect the Wingmen MCP from `.mcp.json` in your host's MCP settings. Grok users can install it as a plugin from `.grok-plugin/`.

**Then**

Copy `icp-context.template.md` to `icp-context.md`, fill it in, and run `/outbound-setup yourwebsite.com`.

## What is open and what is not

Everything in this repo is free and MIT licensed: the agents, the playbook, the scoring rubric, the copy rules, the commands. Read it, fork it, change it, use the playbook without us.

The agents do their work through the **Wingmen MCP**, which is a paid product: Lead Radar (finding and scoring people daily), the LinkedIn sending engine with its safety limits, the inbox and the copy checks. You need a Wingmen account for the agents to act. There is a free trial at [flywingmen.com](https://www.flywingmen.com).

## Why it works this way

The founder's LinkedIn account is the brand. One restriction costs more than a slow month. So the team runs on LinkedIn's real limits (about 100 invites a week per account), messages from signals instead of volume, and never takes an action you did not see first. The math in `skills/outbound-team/references/safety.md` shows what one account can honestly book in a month.

## Contributing

Issues and pull requests welcome, especially new signals, sharper copy rules and better weekly reviews. Keep the three rules.

---

MIT © Nemanja Milic · [Wingmen](https://www.flywingmen.com)
