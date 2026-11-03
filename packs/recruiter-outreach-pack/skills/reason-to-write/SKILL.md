---
name: reason-to-write
description: Finds one honest reason to write to a client or candidate that serves them, built on a sourced fact or signal, and tests it so it is not a pitch in disguise. Then hands it to the drafting skill. Use when a recruiter says "what do I say", "give me an angle", "personalize this", "why would they reply", or every opening they think of turns into "let me tell you what we do".
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Reason to write

People reply when a message is about them. You help a recruiter pick a single reason to write that is true, specific and useful to the reader, before any message is drafted.

If `references/agency-profile.md` exists, read it for proof points and specialties. Never invent placements, candidates or market data.

## Input

- The company fact sheet, hiring signal scan or contact brief (for BD), or the candidate's public profile and the job order (for candidate outreach).
- What the recruiter actually has to offer: a candidate in hand, market pay data they collected, a placement at a similar company, an introduction.

## Find candidate reasons

Write two to four possible reasons. Each must rest on one numbered fact or signal and name what is in it for the reader:

- "Your controls engineer role has been open 45 days (signal 1). We placed two controls engineers in Gwinnett this year and have a third interviewing."
- "You led the move to SAP at [company] (public post). This role is the same project, two years earlier."

## The pitch test

Reject a reason if any of these are true:
- It would read the same sent to any company or person.
- The fact is only there to lead into "we are an agency that...".
- It relies on something private, personal or guessed.
- The offer is vague ("we have great candidates").

## Output

```
REASON TO WRITE: [Company or candidate] | [date]
Options:
1. [reason] | rests on: [fact/signal #, link] | in it for them: [one line] | pitch test: pass / fail
...
Recommended: [one], because [one line]
Talking points (2 to 3, sourced): [list]
Hand to: client-bd-outreach (BD) or candidate-outreach (candidates)
```

## Rules

- One reason per message. If nothing passes the test, say "no reason yet" and suggest what to watch.
- Every talking point keeps its source so the recruiter can check it before sending.
- Never use personal information (family, health, beliefs, personal social posts) as a hook.
