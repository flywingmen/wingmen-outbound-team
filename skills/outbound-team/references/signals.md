# Signals: who is ready to buy right now

Score the signal, not the title. "VP of Sales at a 50-person company" describes 10,000 people. A signal describes one person, this month.

## The six signals, strongest first

1. **Pain language.** They describe the problem you solve in their own words. "Our SDR left and I'm back to doing outreach myself." Quote it or it did not happen.
2. **Hiring for the adjacent role.** A job post for the role your product replaces or supports. Budget and pain, both visible.
3. **Funding or growth, last 90 days.** New money, new market, new office. Pressure to show pipeline.
4. **New in role, 1 to 3 months.** New leaders change tools early, before habits set.
5. **Engaging with a competitor.** Comments on or reactions to a competitor's posts. In market, comparing.
6. **Community questions.** Asking about the topic in a group, a thread, a post. Weakest alone, strong stacked.

## Where Wingmen finds them

Lead Radar runs these as sources, per LinkedIn account. `get_pipeline_status` shows each source with its last 30 days (found, surfaced, approved, accepted). Turn sources on or off with `set_source`:

niche post engagers, topic post engagers, competitor post engagers, pain-language posts, hiring posts, funding posts, job changes, fund closings, follower pool, cold search, lookalike search.

Cold search is the backstop: it stays on when every warm source is off, so Radar never goes dry.

## Warm pools you build by hand

- **A post your buyers comment on.** `get_post_engagement` on any LinkedIn post returns the commenters (with their words) and the reactors. Save the right ones with `save_post_engagers_to_list`: the post, its topic and each person's own comment travel with them, so the first message can reference it honestly.
- **Your own network.** `list_my_connections` with a query like "founder agency". Messaging existing connections is far safer than sending invites, and it is the most underused lane in outbound.

## Decay

A hiring post from February is not a signal in August. It is a fact about the past. Halve anything older than 90 days, drop anything older than 180. Most lists rot because nobody ages them out.
