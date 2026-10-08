# Safety: the account is the asset

For a founder-led business, the founder's LinkedIn account is the brand. One restriction costs more than a slow month of leads. Volume is never worth it.

## What actually triggers a review

1. A low invite acceptance rate (invites to people with no reason to know you)
2. Pending invites piling up
3. "I don't know this person" and spam reports
4. Behaviour that does not look human: bursts, odd hours, the same message to everyone

## Limits

The real ceiling moves with account age, network size and history. Treat any fixed "safe daily limit" as a tool's default, not LinkedIn's tolerance for this account.

- Wingmen's defaults: 25 invites a day, 50 messages a day, weekdays, inside the account's send window, with warm-up for new accounts. `get_accounts` shows what each account has used today and this week.
- A new account's first two weeks run lower. `agent_progress` shows the current connection request limits.
- Messages to existing connections are far safer than invites. Use manual campaigns for people the account already knows.
- Blank invites (no note) are the default because they get accepted more often.

## How many calls one account can book

Do this math before anyone promises a number. One account safely sends around 100 invites a week, about 400 a month. At a measured 46% acceptance, 31% reply and roughly 1 in 4 replies booking, that is about **10 booked calls per account per month**. That ceiling belongs to LinkedIn, not to any software, including tools that advertise thousands of "prospects" a month. Sourcing more than an account can contact is inventory that sits unused.

So "3 calls a day" (about 60 a month) needs about 6 accounts. Say this out loud when someone asks for more.

## When something looks wrong

`pause_agent` stops an agent at once and is always safe. Then read `get_accounts` (pauses, limits hit) and `agent_progress` (what is holding each agent back) before changing anything.
