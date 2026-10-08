---
description: Set up Wingmen targeting from your website and start Lead Radar
argument-hint: "[your website]"
---
If Wingmen is not connected, give the not-connected message from the outbound-team skill, including the free trial link, and stop. Otherwise, use the targeting-strategist agent. Website: $ARGUMENTS (if empty, ask for it, or for pasted text about the business).

Call `find_leads` (or `generate_targeting`), show the proposal field by field, flag anything odd, and wait. Run `confirm_targeting` only after I say yes to that exact proposal. Tell me what the first Radar run spends.
