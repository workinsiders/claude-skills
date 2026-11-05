---
name: campaign-launch-checklist
description: "Runs the pre-launch gates on a recruitment agency's cold email campaign (domains warm and authenticated, list verified and suppressed, copy and merge fields checked, schedule and limits set, opt outs working, legal flags closed) and passes or holds it, saving it paused for the recruiter to launch. Use when a recruiter asks \"is my campaign ready\", \"pre-launch checklist\", \"check my Instantly campaign before I launch\", \"what could go wrong at launch\", or \"go live checklist for cold email\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Campaign launch checklist

You check a cold email campaign before the recruiter launches it. The volume and bounce numbers below are practitioner rules of thumb, not published standards. A campaign passes only when every gate passes. One failed gate holds the launch, with the fix named.

If `references/agency-profile.md` exists, read it first, including the Cold email lines.

Ask for the campaign brief from cold-email-start-here if there is one. Otherwise ask for: sending domains and mailboxes, warmup start date, the list file or its stats, the sequence, the sequencer settings (daily limits, schedule, tracking, stop-on-reply), and the countries on the list.

## The gates

| # | Gate | Passes when |
|---|---|---|
| 1 | Domains | Sending domains are not the agency's main domain; SPF, DKIM, DMARC and MX pass on each |
| 2 | Warmup | Each mailbox warmed at least 14 days (ideally 21+), warmup still on, health score good in the sequencer |
| 3 | Limits | Daily cold limit per mailbox at the ramp level (about 10 per mailbox in week one and 20 in week two, never over 40), random gap between sends turned on |
| 4 | List | Verified within 30 days, expected bounces under 2%, catch-alls separated, suppression list applied, one or two people per company |
| 5 | Copy | Plain text, no links, website domains, email addresses or attachments in email 1 (signature included), open tracking off, within the word limit of the skill that wrote it (BD 50 to 90, MPC under 90, candidate database under 100, candidate cold under 120), one opt-out line only, passes the free cold email spam-word checker (workinsiders.com/free-tools/cold-email-spam-checker/) |
| 6 | Merge fields | Every field exists in the list; no empty values in the rows being sent; three filled-in samples read correctly |
| 7 | Variants | Spintax syntax correct for this sequencer; test variants split evenly if a test is running |
| 8 | Schedule | Weekdays, business hours in the readers' time zone, sequence steps and waits as approved, stop on reply on, stop for the whole company on reply if the tool has it |
| 9 | Opt out | Opt-out line in every email; unsubscribes and "no" replies go to a suppression list that every campaign reads; US emails carry the mailing address |
| 10 | Legal | cold-email-compliance-check run for every country on the list, every flag closed or answered by the adviser |
| 11 | Replies | Someone owns the reply inbox daily; cold-email-reply-handler ready; booking link ready for "yes" replies |
| 12 | Seed test | One test send to the recruiter's own Gmail and Outlook addresses, read on a phone, landed in the inbox |

## How to run it

Go gate by gate. For each, mark **pass**, **fail** (with the fix) or **unknown** (with the question to answer). Unknown counts as fail until answered.

Then:
- All pass: say "ready to launch", and remind the recruiter to launch it themselves and watch the first 48 hours (bounces, replies, any complaints).
- Any fail: say "hold", list the failed gates in the order to fix them, and which skill fixes each.

## If a sequencer connector is connected

If the recruiter asks and a sequencer connector (such as Instantly's) is available, you may create the campaign, add the sequence and leads, and apply the settings above, **saved as paused**. Then read the settings back and check them against the gates. You never activate a campaign or send an email.

## The first 48 hours

Give the recruiter this short watch list:
- Bounces: target under 2%. Over 2%: check the list. Over 3% on 100+ sends, or over 5% at any point after 50 sends: pause and run deliverability-check. Pausing is always safe; ignore a one-day spike on tiny numbers.
- Any spam complaint: read the email again and check the targeting.
- Replies: answer within one working day using cold-email-reply-handler.
- Out-of-office replies with a return date: set a reminder, do not count them as replies.
