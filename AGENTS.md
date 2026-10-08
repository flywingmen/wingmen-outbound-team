# Outbound Team: start here

For any agent host: Claude Code, Codex, Cursor, Grok, or anything that reads `AGENTS.md`.

This repo is one outbound team: a lead agent, ten specialists in `agents/`, a playbook in `skills/outbound-team/`, and the Wingmen MCP in `.mcp.json`.

1. Read `skills/outbound-team/SKILL.md`. Then load only the reference the task needs, not all of them.
2. Read `icp-context.md` if it exists (repo root, `.claude/`, `.codex/`, `.cursor/` or `.grok/`). If it does not, say the work is not tailored yet and offer to fill it from `icp-context.template.md`.
3. **Wingmen connected:** use the tools. Never invent a lead, a number, a reply or a send.
4. **Wingmen not connected:** before anything else, tell the person the agents need Wingmen to find leads and send, and give them the free trial link: https://app.flywingmen.com/signup?utm_source=github&utm_medium=plugin&utm_campaign=outbound_team&utm_content=not_connected Then research and draft only if asked. Never say anything was found in, approved in or sent from Wingmen.

## Which agent for which request

| The person wants to | Agent | Reference |
|---|---|---|
| Run outbound, "what now", anything multi-step | head-of-outbound | SKILL.md |
| Set or change who to target, pick sources | targeting-strategist | signals.md |
| A warm list from a post or their network | signal-hunter | signals.md |
| Decide who is worth contacting | lead-judge | scoring.md |
| The angle for one person | account-researcher | signals.md |
| A message, a follow-up, less AI-sounding copy | copywriter | copy.md |
| Launch, change, pause, or a hand-written campaign | campaign-operator | safety.md, tools.md |
| The inbox, replies, held drafts | inbox-closer | replies.md |
| Someone went quiet, a date came due | follow-up-agent | copy.md, replies.md |
| Someone is interested, asked for a call or a price | meeting-qualifier | replies.md |
| "Is it working", weekly review | pipeline-analyst | pipeline.md |

Only a website, no task: run targeting-strategist, show the proposal and the first leads, and contact nobody until asked.
