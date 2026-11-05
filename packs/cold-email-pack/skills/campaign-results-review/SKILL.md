---
name: campaign-results-review
description: "Reviews a recruitment agency's cold email campaign each week from its own numbers (sends, bounces, opt outs, replies, interested replies, calls and job orders per segment and mailbox), finds where the funnel breaks and names the one change to make next. Use when a recruiter asks \"how is my campaign doing\", \"review my Instantly stats\", \"why no job orders from cold email\", \"weekly cold email report\", \"which segment works\", or \"should I stop this campaign\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Campaign results review

You review a running cold email campaign from the recruiter's own numbers and turn them into one decision for next week. The goal of agency BD email is job orders, so the review follows the funnel all the way there, not just to replies.

For a few hand-written runs rather than a sequencer campaign, outreach-review in the Recruiter Outreach Pack is the better fit.

If `references/agency-profile.md` exists, read it first.

## Ask for the numbers

Per segment and, if possible, per mailbox, for the period:
- Contacts started, emails sent, hard bounces, opt outs, spam complaints if shown.
- Replies, split into interested (yes, send details, a fees question), not now, objections, negative.
- Calls booked, calls held, job orders or terms signed, and any placements traced to the campaign.

If the recruiter has only some of these, work with what there is and say what to start tracking.

## The funnel

Show it as a table per segment:

| Step | Count | Rate |
|---|---|---|
| Contacts started | | |
| Bounced | | of sent |
| Opted out | | of contacts |
| Replied | | of contacts |
| Interested replies | | of contacts |
| Calls held | | of interested |
| Job orders | | of calls |

Add the **interested rate**: interested replies / human replies (out-of-office and automatic replies left out). As a rough rule of thumb, not a benchmark, practitioners treat about 20% as great, 10% as good and under 5% as a sign the offer or the list is wrong; the recruiter's own past campaigns beat it.

Then find the first step where it breaks, using the recruiter's own past campaigns as the comparison. When they have no history, use these health lines, which are rules of thumb, not benchmarks:
- Bounces: target under 2%. Over 2%: check the list. Over 3% on 100+ sends, or over 5% at any point after 50 sends: pause and run deliverability-check. A steady rise week on week is a list problem; go to list-verification-gate.
- Opt outs much higher than interested replies: the wrong people or the wrong message for them. Go to recruitment-icp-builder.
- Clean deliverability and no interested replies after about 2,000 sends (or two full runs of the sequence on a small list): the offer or the reason to write is dead. Go to recruitment-offer-builder for a new angle; do not just send more.
- Replies but few interested: the ask or the angle. Test with ab-test-plan.
- Interested replies but few calls: reply speed or how replies are handled. Go to cold-email-reply-handler.
- Calls but no job orders: the first call or the terms. first-call-prep in the Recruiter Outreach Pack or fee-objection-replies in the Agency Growth Pack.

Open rates are left out on purpose: they are unreliable and a poor guide for cold email.

## Mailbox health

If per-mailbox numbers show one mailbox with more bounces or far fewer replies than the others on the same list, flag it for deliverability-check and suggest pausing it.

## The decision

End with one of:
- **Keep going** (what to watch).
- **Change one thing** (which, and the skill that does it).
- **Pause** (why, and what must be true to restart).
- **Stop this segment** (and what to try instead).

One decision. If several things are wrong, fix the earliest step in the funnel first.

## Rules

- No invented industry benchmarks or "average reply rates".
- Never count out-of-office or automated replies as replies.
- Attribute a job order to the campaign only if the recruiter confirms it started there.
