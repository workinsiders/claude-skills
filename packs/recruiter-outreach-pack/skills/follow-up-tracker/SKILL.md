---
name: follow-up-tracker
description: Keeps outreach threads from dying: replies the recruiter owes first, one useful follow-up per silent thread (never "just bumping this"), the date each thread closes, and calls to book. Use when a recruiter says "who do I follow up with", "my threads went cold", "follow-up list", pastes a list of sent messages, or at the start of each week.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Follow-up tracker

Most outreach is lost to silence on the recruiter's side, not the reader's. You help a recruiter see what they owe, what to send and what to close.

If `references/agency-profile.md` exists, read the sign-off and phone details for follow-up messages.

## Input

A list of threads from the recruiter: who, date of first message, channel, any reply and its date, last touch. A paste from their CRM, ATS or sequencing tool is fine.

## Sort the threads

1. **You owe a reply.** They answered and are waiting. These come first, today.
2. **Follow up.** No reply, last touch 3 to 7 days ago, fewer than three touches.
3. **Close.** Three touches with no reply, or 21+ days of silence. One polite close, then stop.
4. **Stop.** They said no, asked to be removed, or are on a do-not-contact list. Nothing more, and log it.

## Follow-ups that add something

Each follow-up brings one new, true thing: a new fact or signal, a blind candidate profile, a pay note the recruiter collected, or a different, easier ask. If there is nothing new, the next touch is the close.

## Output

```
FOLLOW-UP TRACKER | [date]
Reply today: [who, what they asked]
Follow up: [who, touch #, the new thing, channel, date]
Close: [who, close line]
Stopped: [who, reason; remove from all sequences]
Calls to book: [who, two times to offer]
```

Hand replies that need a full answer to candidate-reply-handler (candidates) or draft them for clients with the recruiter's voice guide.

## Rules

- Never keep messaging someone who opted out, and remind the recruiter to suppress them everywhere.
- No "just checking in", no fake deadlines, no guilt.
- Three touches is the default limit unless the recruiter sets another.
