# Pipeline: the weekly review

Ten minutes, once a week. The goal is one decision, not a dashboard.

## Pull

1. `get_pipeline_status`: each account's last 7 days, and every Radar source with its 30-day found, surfaced, approved and accepted.
2. `get_campaign_performance`: the funnel per agent, enrolled to invites to accepts to replies.
3. `get_activity` with `days: 7`: the counts, and Lead Radar's own notes on what it learned and changed.
4. `check_usage`: credits and the monthly lead allowance, so nothing runs dry mid-week.

## Count calls honestly

Wingmen's "meetings booked" counts bookings it saw. Calls arranged inside a thread (a time agreed, a Zoom invite pasted) can be missing from it. Scan the last week's replies in `get_activity` for scheduling words and count those calls too, named, so the number is right.

## Answer four questions

1. **Which source turns into accepted invites?** Rank sources by accepted, not by found. A source that finds 200 and gets 3 accepted is costing you.
2. **Where does the funnel leak?** Low acceptance points at targeting or the account. Low replies point at copy. Replies but no calls point at how replies are handled.
3. **Is any agent stuck?** `agent_progress` says what is holding each one back: a disconnected account, an empty list, nobody approved, a paused outreach, a send window.
4. **Is the queue rotting?** Pending leads older than two weeks are stale signals. Approve or dismiss them.

## Report

Exactly five lines, one sentence each, no sub-bullets:

1. Calls: booked this week, named, with source (including calls agreed inside a thread)
2. Leak: the one stage that leaks, with the number that shows it
3. Change: one change (a source off, a targeting tweak, a copy change, the qualifier over open replies), and the agent that makes it
4. Stuck: the single biggest blocker, or "nothing"
5. Budget: the limit that bites first, or "fine"

A change that touches replies always goes through the meeting-qualifier. Never a blanket call ask.

Propose the change. Make it only after the person says yes.
