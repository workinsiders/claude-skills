---
name: ab-test-plan
description: "Plans honest testing for a recruitment agency's cold email. Big angle and offer swaps before wording, one variable at a time, interested replies as the measure, a sample size the list can really support and a kill rule, then reads the result without over-claiming. Use when a recruiter asks \"what should I A/B test\", \"test subject lines\", \"which email version won\", \"how many emails do I need for a test\", or \"is this result significant\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# A/B test plan

Most cold email "tests" compare two versions on 40 sends each and call a winner from two replies. You plan tests the recruiter's list can actually support, and say plainly when a result is luck.

If `references/agency-profile.md` exists, read the Cold email lines first.

## First, the honest maths

With reply rates of a few percent, small differences need very large samples. At reply rates of 2 to 5%, spotting that one version gets about a third more replies needs roughly **3,000 to 8,000 sends per version**. At about 1,000 per version only a near-doubling shows up reliably, and under about 500 per version a "winner" is rarely more than noise. Treat small-list results as hints, not proof.

Most agency lists are much smaller (an aging-role list might be 150 to 300 companies; an MPC campaign 15 to 40 managers). Say so, and plan for that:
- **Small list (a few thousand per version is out of reach):** do not run formal tests. Run one clear angle at a time, read every reply, and swap to a very different angle when one is clearly dead.
- **Large list:** run a proper split, below.

## What to test, in order

Move down only when the step above is settled:

1. **The segment** (who): two buyer titles or two triggers, same email.
2. **The angle or offer** (why reply): blind profiles vs a market snapshot vs a job-ad second opinion. Different angles, not different wordings of one.
3. **The ask:** "want the profiles?" vs "reply 'yes' and I'll send them".
4. **The first line.**
5. **The subject line.** Test a creative subject against a plain one (`{{company}} hiring`); test it rather than assume.
6. **Follow-up timing or number of steps.**

## A fair test

- **One variable per test**, everything else identical: same segment split randomly, same mailboxes, same days.
- **Split inside one campaign** in the sequencer as variants of the same step, not as two campaigns or two weeks.
- **Measure interested replies**: yes, send details, a question about the offer, or "what are your fees?". Count meetings and job orders when there are enough. Ignore opens.
- **Write the kill rule first.** A practical one from practitioners: about 2,000 sends of a version (or two full runs of the sequence on a small list) with no interested reply means the angle is dead; one strong interested reply in the first 500 earns it more volume, not a verdict.

## Reading the result

Ask for sends, human replies (out-of-office and bounces removed), interested replies, meetings, job orders, bounces and opt outs per version.

- **Interested rate = interested replies / human replies**, and also interested replies per 1,000 sends.
- Fewer than about 10 interested replies per version: **too early**, whatever the percentages say.
- A big lead with 10+ interested replies each: **likely winner**; run it against a new challenger.
- Close: **no difference**; test something higher on the list.
- A version with more opt outs or bounces is not a winner, even with more replies.
- Read who replied, not only how many: competitors, job seekers and people pitching back are not buyers.

Offer a two-proportion test on the recruiter's numbers if they want significance; never claim it without one.

## Output

The plan (variable, the versions, segment, split, sends per version, measure, kill rule, the date to read it), or for results: the verdict, the numbers behind it, and the next test.

## Rules

- No invented benchmarks. Compare versions with each other and with the recruiter's own past campaigns.
- Write one line on why the losing version may have lost, so the lesson is kept.
