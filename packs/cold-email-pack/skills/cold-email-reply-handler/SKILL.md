---
name: cold-email-reply-handler
description: "Sorts the replies to a recruitment agency's BD cold email campaign (interested, send details, fees question, referral, objection, not now, out of office, opt out) and drafts the right answer for each, aimed at a call or a signed job order, with the CRM update and next date. Use when a recruiter pastes cold email replies and asks \"how do I reply\", \"sort my Instantly replies\", \"they said we use other agencies\", \"they asked for our fees\", \"they said send resumes\", or \"they referred me to someone else\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Cold email reply handler

A reply is the point of the whole campaign, and the reply most often fumbled. You sort each one, draft an answer the recruiter can send in a minute, and say what to log. Speed matters: a good reply within the hour beats a perfect one tomorrow. For candidate replies, use candidate-reply-handler in the Agency Desk Pack.

If `references/agency-profile.md` exists, read it first: sender details, proof points, fees and guarantee, booking link.

## Sort first

Put every reply in one group. If a reply fits two, use the one higher on this list:

1. **Opt out.** "Remove me", "stop", "please don't contact me", "how did you get my email". Read generously.
2. **Interested.** "Yes", "send them", "what candidates do you have?", "what are your fees?", a question about the offer.
3. **Referral.** "Not me, talk to Sam", or a forwarded thread.
4. **Objection.** "We use other agencies", "we only use our PSL", "we hire in-house", "your fees are too high", "AI does our sourcing", "no roles right now".
5. **Not now.** "Try in Q2", "hiring freeze", "role filled".
6. **Out of office or automatic.** Auto-replies, "no longer works here", ticket systems.
7. **Wrong fit.** They do not hire this kind of role.

## Answers by group

1. **Opt out:** "Done, you won't hear from me again." If they asked where their email came from, answer truthfully from the row's source (UK and EU readers have a right to know). Add them to the suppression list for every campaign today. "Please don't send speculative profiles" covers their whole company.
2. **Interested:** deliver what the email promised **in the reply itself**: the blind profiles, the market snapshot, the job ad note. Never "let's get on a call and I'll walk you through it" when you offered to send something. Then one question that qualifies the need ("Is the role approved, and who else decides?"), then either two exact times with a time zone or the booking link on natural words, not both. Under 100 words.
   - **"What are your fees?"** is a buying question. Answer plainly from the profile (fee basis, when it is payable, replacement period), then one line on what they get for it, then the times or the booking link. Never invent or discount a fee. For pushback, use fee-objection-replies in the Agency Growth Pack.
   - **Protect the introduction.** Before or with the first blind profile, send the agency's terms of business and ask for them to be accepted as the agency's process requires. Log the date and time each profile went to each company, because the introduction period runs from then. Before naming any candidate, ask the candidate whether they have applied to, or been sent to, that company in the last 12 months; if so, do not introduce them.
   - **Hard roles:** if the role has been open 60+ days or is hard to fill and the profile lists exclusive or retained terms, propose them on the call, not in email.
   - **"Send resumes first":** send blind summaries. Full resumes and identities only after the candidate agrees to that company and the terms are in place as the agency's process requires.
3. **Referral:** thank them, then write a new short email to the named person: "Dana suggested I get in touch about...". Check Dana is happy to be named if it is not clear. Remove Dana from the sequence. Do not count a referral as interested.
4. **Objection:** acknowledge, ask one sharp question, offer one small next step, give an honest out. Never trash the incumbent.
   - Other agencies or PSL: "Makes sense. Is there a role type they find hardest? And when does the supplier list come up for review?"
   - In-house team: "Good to hear. We usually help in-house teams on the roles that sit open longest. Is [role] one of those?"
   - "Go through HR or TA" / "we don't accept agency approaches to managers": thank them, ask for the right talent contact, and flag the company in the CRM as TA-only for every campaign.
   - No roles now: offer something useful for later (a talent map or pay snapshot the recruiter can really produce) and ask when hiring usually picks up.
5. **Not now:** agree, ask when to check back, log the date and reason. One line.
6. **Out of office:** no reply. Log the return date and pause that contact until then. If it names a new contact, treat it as a referral; if the person left, find their replacement.
7. **Wrong fit:** thank them, ask who hires this role there, remove them.

## Measure

Interested rate = interested replies / human replies (out-of-office, bounces and automatic replies left out). Pass the count to campaign-results-review.

## Output

For each reply: the group, the draft answer, the CRM or sequencer update (status, next date, remove from sequence yes or no), and anything the recruiter must decide. Opt outs and interested replies first.

## Rules

- Every human reply gets an answer within one working day, interested replies first.
- Remove anyone who replied from the automated sequence, whatever they said.
- Never quote fees, guarantees or candidate details that are not in the profile or the recruiter's notes.
- After a "no", send only the one-line confirmation, then stop. You draft; the recruiter sends.
