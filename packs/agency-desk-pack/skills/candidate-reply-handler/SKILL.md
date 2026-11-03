---
name: candidate-reply-handler
description: Drafts the recruiter's answer to any candidate reply to outreach, from "interested" to "not now", "what's the pay?", "who's the client?", "send me the JD", angry replies and opt outs. Use when a recruiter pastes a candidate's reply, asks "how do I answer this", or wants a batch of replies sorted and answered.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: agency-desk-pack
---

# Candidate reply handler

A reply is the most valuable moment in outreach and the easiest one to waste. Your job: read what the candidate actually said, sort it, and draft an answer that moves to a call, or closes the loop cleanly and keeps the door open.

If `references/agency-profile.md` exists, read it first. Follow its rules on naming the client, texting candidates and sharing pay. Never invent pay, client names, benefits or interview dates. If a fact is missing, leave a [bracket] for the recruiter to fill.

## Input

- The candidate's reply.
- The original message, if the recruiter has it.
- The job order, or a few lines about the role.

For a batch, handle each reply in turn and finish with a one-line summary per candidate.

## Step 1: sort the reply

Put it in exactly one bucket. If two fit, pick the one that needs action first.

| Bucket | Sounds like | Goal of your answer |
|---|---|---|
| Yes | "Sure, let's talk", "tell me more" | Book the call in this reply |
| Question first | pay, client, location, remote, title | Answer what you can, then book |
| Send details | "send me the JD" | Send a short summary, not just a file, and ask for 15 minutes |
| Not now | "happy where I am", "maybe in six months" | Respect it, ask one light question, set a follow-up date |
| Wrong fit | wrong level, skill or location | Thank them, ask what would interest them, ask for a referral once |
| Referral | "not me, but try my colleague" | Thank them, ask permission to use their name |
| Upset | "how did you get my number", "stop spamming me" | Apologise briefly, say how you found them, offer removal |
| Opt out | "remove me", "unsubscribe" | Confirm removal in one line. Nothing else. |
| Out of office | auto-reply | No answer. Note the return date. |

## Step 2: draft the answer

Rules for every answer:

- Match their channel and length. A one-line text gets a short text back, not an email.
- Answer their question in the first sentence. Do not dodge pay. If the agency profile allows sharing pay, give the range. If it does not, give a straight reason and the band the recruiter supplied, if any.
- Client name: follow the profile. If the client stays confidential, describe it truthfully (industry, size, location, why people like working there) and say when you can share the name, usually on the call.
- One ask per message. For a call, offer two specific times or the booking link from the profile.
- No pressure tactics, fake deadlines or "other candidates are moving fast" unless the recruiter says it is true.
- Under 90 words for email and InMail, under 40 for texts.

## Step 3: the hard ones

- **Pay before anything else:** answer it. People who ask about pay first are often the most serious.
- **Pay too low for them:** thank them for being direct, ask their number, and say honestly whether the client might get close. Never promise the client will move.
- **"Who's the client?" when you cannot say:** explain that the client asked for confidentiality, give the details that matter, and say plainly that you will never submit them anywhere without their OK.
- **"Is this a real job?":** give your full name, agency, and a phone number or link from the profile.
- **Upset:** no arguing and no defending the sequence. Two sentences, then remove them if they ask.

## Step 4: notes for the recruiter

End every output with:

```
Bucket: [ ]
Next step and date: [for example "follow up Mar 3" for Not now]
Log in the ATS: [status, reason, new facts such as pay needed or notice period]
```

For every opt out, remind the recruiter to suppress the contact in all sequences and the ATS today.

## Never

- Never write anything the candidate could read as a promise of an interview or an offer.
- Never ask about age, family, health, religion, nationality or other protected traits, even if the candidate brings them up. Steer back to the role.
- Never keep messaging someone who opted out.
