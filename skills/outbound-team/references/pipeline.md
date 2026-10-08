# Pipeline: the weekly review

Ten minutes, once a week. The goal is one decision, not a dashboard.

## Pull

1. `get_pipeline_status`: each account's last 7 days, and every Radar source with its 30-day found, surfaced, approved and accepted.
2. `get_campaign_performance`: the funnel per agent, enrolled to invites to accepts to replies.
3. `get_activity` with `days: 7`: the counts, and Lead Radar's own notes on what it learned and changed.
4. `check_usage`: credits and the monthly lead allowance, so nothing runs dry mid-week.

## Answer four questions

1. **Which source turns into accepted invites?** Rank sources by accepted, not by found. A source that finds 200 and gets 3 accepted is costing you.
2. **Where does the funnel leak?** Low acceptance points at targeting or the account. Low replies point at copy. Replies but no calls point at how replies are handled.
3. **Is any agent stuck?** `agent_progress` says what is holding each one back: a disconnected account, an empty list, nobody approved, a paused outreach, a send window.
4. **Is the queue rotting?** Pending leads older than two weeks are stale signals. Approve or dismiss them.

## Report

Five lines, plain:

- Calls booked this week, and from which source
- The one leak, with the number that shows it
- The one change to make (a source off, a targeting tweak, a copy change), and the tool that makes it
- Anything stuck
- Budget left

Propose the change. Make it only after the person says yes.
