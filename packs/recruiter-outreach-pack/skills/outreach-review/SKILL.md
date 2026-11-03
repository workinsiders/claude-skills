---
name: outreach-review
description: Reviews a few runs of outreach using only the recruiter's own counts: replies and calls by reason, channel and warm versus cold, what worked against what was expected, and one change to test on the next run, so the desk learns instead of changing five things at once. Use when a recruiter says "what's working", "review my outreach", "reply rates", "my BD isn't working", or after three or four runs.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Outreach review

You cannot improve outreach you do not count. You help a recruiter read their own numbers honestly and pick one thing to change.

## Input

The recruiter's own log for the last three or more runs: who was contacted, the reason used, channel, warm or cold, reply (yes, no, positive, negative), call booked, job order or candidate submitted. An export from their CRM, ATS or sequencing tool is fine.

## Count

Using only their data:

- Messages sent, replies, positive replies, calls booked, job orders or submittals.
- Split by reason type (open role signal, funding, candidate in hand, warm intro, other), by channel, and by warm versus cold.
- Note small numbers plainly: "3 replies from 12 is not a pattern yet".

## Read it

1. **What worked better than expected,** and the likely reason, as a guess to test, not a fact.
2. **What worked worse.**
3. **What you cannot tell yet** because the numbers are too small.

## One change

Pick one change for the next run: a reason type, a channel, a time of day, more warm intros, shorter messages. Say what you expect, what to count, and how many runs before looking again. Keep everything else the same.

## Output

```
OUTREACH REVIEW | runs [dates] | [n] messages
| Split | Sent | Replies | Positive | Calls | Job orders / submittals |
Better than expected: [ ]
Worse than expected: [ ]
Too early to tell: [ ]
Next run test: change [one thing]; expect [ ]; count [ ]; review after [n] runs
```

## Rules

- No industry benchmarks, invented averages or "typical reply rates". Use only the recruiter's own numbers.
- Never judge individual people who did not reply. Count messages, not persons.
- One change at a time.
