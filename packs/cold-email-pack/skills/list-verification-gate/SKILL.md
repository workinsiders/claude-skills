---
name: list-verification-gate
description: "Sets and checks the verification gate a recruitment agency's cold email list must pass before sending, reading the verifier's results, deciding what to do with valid, risky, catch-all and invalid addresses, and estimating bounce risk. Use when a recruiter asks \"do I need to verify my list\", \"what do I do with catch-all emails\", \"my verifier says risky\", \"is this list safe to send\", \"bounce rate too high\", or \"how old can verification be\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# List verification gate

No list is sent until it passes this gate. The thresholds are practitioner rules of thumb, not published standards. Bounces are the fastest way to damage a sending domain, and even "verified" addresses from data tools bounce once people change jobs, which in recruiting is the whole point.

If `references/agency-profile.md` exists, read the Cold email lines first.

## The gate

A list passes when:
- Every address was verified within the **last 30 days**, either by an email verifier the agency already uses or by a data tool that verifies at export (say which; there is no need to pay twice).
- Expected hard bounce rate is **under 2%**, and never above 3%.
- Suppressions from lead-list-builder are applied.

## Reading verifier results

Ask the recruiter to export the verifier's result column. Then sort every row:

| Result | What to do |
|---|---|
| Valid / deliverable / safe | Send |
| Invalid / undeliverable | Remove. Never retry |
| Disposable, role-based, spam trap, abuse | Remove |
| Catch-all / accept-all | The server accepts everything, so the verifier cannot tell. Hold back. Options below |
| Unknown / risky / timeout | Re-verify once. If still unknown, treat as catch-all |

## Catch-all addresses

Many company domains are catch-all, so dropping them all can cut a recruiting list sharply. Choose one:
1. Run them through a verifier that checks catch-alls specifically, if the agency has one, and keep only those it marks valid.
2. Send them as a separate, small campaign from one healthy mailbox, a few a day, and stop at the first sign of bounces.
3. Leave them out and find another contact at that company.

Never mix unchecked catch-alls into the main campaign.

## Read the list's health from the results

- As a rough rule of thumb, catch-alls around 10 to 25% of a B2B list is normal; 25 to 50% suggests a stale or scraped source; over 50% means the source is poor.
- Invalid over about 30% means stop and question where the list came from, not just clean it.

## Estimate the bounce risk

Show the sum: (invalid not removed + expected bounces from catch-alls and unknowns kept) / rows to send. If it is over 2%, say which group to cut to get under it.

## Before every send, not once

- Re-verify if more than 30 days pass before the rows are sent.
- Pull hard bounces from every campaign weekly and add them to the suppression list.
- Live bounces: target under 2%. Over 2%: check the list. Over 3% on 100+ sends, or over 5% at any point after 50 sends: pause and run deliverability-check.

Work Insiders' free email verification cost calculator (workinsiders.com/free-tools/email-verification-cost-calculator/) shows what a list size costs with each verifier.

## Output

The counts by result, the rows to send, the rows held back and why, the bounce estimate with the sum, and a pass or fail. If it fails, the one change that would make it pass.

## Rules

- Never call a list verified because a data tool says so, unless that tool checked each address at export within the last 30 days.
- Never suggest sending an invalid address "to see what happens".
- Verifying an address only confirms it exists; it does not make it legal or wise to email. That is cold-email-compliance-check's job.
