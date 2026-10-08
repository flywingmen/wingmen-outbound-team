# Replies: where the money is

A reply is the only part of outbound that turns into revenue. Work it before you find one more lead.

## Daily order

1. `get_conversations` with `view: "your_move"`: the people waiting on you, oldest first, with how long each has waited. Start at the top.
2. `get_conversations` with `held: true`: drafts an agent wrote that Wingmen held for review, each with the reason. Fix or approve.
3. `get_conversations` with `view: "later"`: people who asked to be contacted on a date. Anyone whose date has come moves to today.

## Answering one thread

1. Read the whole thread first with `get_conversation`. Never answer from the inbox preview.
2. Name the sentiment honestly. A polite brush-off is not HOT.
3. Draft the reply:
   - Answer what they actually asked, in their words.
   - A yes gets the booking link and one line, nothing else.
   - A question gets a straight answer, then one question back.
   - "Not now" gets a thank-you, and their date if they named one.
   - Under 60 words, no em dashes, no pitch they did not ask for.
4. `reply_to_thread` without confirm: shows exactly what goes, from which account. Show it to the person.
5. Only after they say yes: the same call with `confirm: true` and the `send_signature`.

## Never

- Reply on someone's behalf without their yes on the exact words
- Invent a time or date the lead did not name
- Quote anything they did not write
- Share the calendar link in a cold message. It goes only after they show interest
