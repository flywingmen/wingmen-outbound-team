# Wingmen MCP tool map

Server: `https://app.flywingmen.com/api/mcp` (docs: flywingmen.com/docs/mcp). Sign in once with your Wingmen account when Claude asks.

Three kinds of tool. Know which one you are calling before you call it.

## Reads (free, change nothing)

| Tool | Use it for |
|---|---|
| `get_pipeline_status` | The whole workspace at a glance: leads by status, each LinkedIn account with its id, last 7 days, Lead Radar sources and their 30-day results. Start most sessions here. |
| `view_icp` | The targeting Lead Radar runs on, field by field |
| `find_leads` | What Radar is working on and the leads waiting. With no targeting yet it proposes one (saves nothing) |
| `list_pending_leads` | The queue, highest score first. Also the low-confidence, approved and removed tabs |
| `get_lead` | One lead in full: score and why, the signal and source, lists, agent stage, conversation id |
| `search_contacts` | Find a person in the workspace by name, company or email |
| `list_lists` | Contact lists, who is on them, which agent works them |
| `get_conversations` | The inbox. `view: "your_move"` = people waiting on you. `held: true` = drafts held for review |
| `get_conversation` | One thread in full, before you reply |
| `get_campaign_performance` | Funnel per agent: enrolled, invites, accepts, replies |
| `agent_progress` | Where each agent is now and when its next step can really go out |
| `get_activity` | The activity feed, plus Lead Radar's own notes on what is working |
| `get_accounts` | Each connected account: limits used today, pauses, searches left |
| `check_usage` | Plan, credits, monthly lead allowance |
| `get_workspace_settings`, `list_automations`, `list_media`, `get_manual_campaign` | Settings, automations, voice notes and media, manual campaign status |
| `list_my_connections` | Search the account's own 1st-degree connections (local cache) |

## Spends budget, sends nothing

| Tool | What it spends |
|---|---|
| `generate_targeting` | One AI analysis and a few LinkedIn searches. Returns a proposal, saves nothing |
| `propose_targeting_change` | Returns a before/after proposal, saves nothing |
| `get_post_engagement` | One comment-fetch unit per page of 50, from the daily discovery budget |
| `sync_my_connections` | The daily connection-fetch budget |
| `save_post_engagers_to_list`, `save_connections_to_list` | Nothing. Creates a list. A list is only worked after a person points an agent at it |
| `create_agent` | One AI generation. The agent is created PAUSED |
| `set_source` | Nothing. Switches one Radar source on or off at once |

## Two calls, a person in between

The first call is a dry run that returns a preview and a signature. Show the preview. The second call, with `confirm: true` and the signature, only after the person says yes. If anything changed in between (someone replied), the signature fails and nothing happens: check again.

| Tool | What the second call does |
|---|---|
| `confirm_targeting` | Saves targeting and starts a Radar run (spends searches and AI credits) |
| `approve_leads` | Approves the listed leads into their list (sends nothing yet) |
| `activate_agent` | Switches an agent on. This is the step that starts real outreach |
| `update_agent` | Saves changes to an agent |
| `create_manual_campaign`, `add_manual_touch`, `edit_manual_message`, `remove_from_manual_campaign` | Creates or changes a hand-written campaign to people you already talk to |
| `reply_to_thread` | Sends one reply into an existing thread |
| `send_message` | Sends one message to a connection or an existing thread |

Single-call actions that are always safe or reversible: `approve_lead` (one lead, sends nothing now), `dismiss_lead` (restorable), `pause_agent` (stopping is always safe), `change_manual_campaign` (pause, resume or cancel, only when asked), `assign_lead`.

## Wingmen's copy checks run on every send

Messages are refused, with every reason returned, if they invent times, quote words the lead never wrote, count your own attempts, remark on someone going quiet, claim an attachment that is not there, or leave a placeholder in. Rewrite and try again. Do not argue with the check.
