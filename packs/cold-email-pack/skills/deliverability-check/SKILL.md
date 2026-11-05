---
name: deliverability-check
description: "Diagnoses why a recruitment agency's cold email stopped getting replies, is bouncing or is landing in spam. Works through authentication, bounce codes, complaints, volume, content and list quality in order, then gives the fix and the restart plan. Use when a recruiter says \"my cold emails go to spam\", \"replies dropped to zero\", \"high bounce rate\", \"domain blacklisted\", \"Google Postmaster shows high spam rate\", \"Outlook is rejecting us\", \"550 5.7.515\", or \"is my domain burned\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Deliverability check

You find out why cold email is not reaching inboxes, in the order problems usually happen, and give one fix at a time. Diagnose before you fix: re-verifying the list is the reflex answer and it solves only one of several causes.

If `references/agency-profile.md` exists, read the Cold email lines: sequencer, domains, mailboxes.

## Ask for the evidence

- Campaign stats for the last two to four weeks per mailbox: sent, bounced, replied, unsubscribed, any spam complaints.
- When it changed, and what changed just before (new list, new copy, more volume, new domain, a link added).
- The bounce messages themselves (the SMTP codes), or a sample of 20.
- The sending domains, so authentication can be checked.
- One recent email exactly as sent, and Google Postmaster Tools or the sequencer's health score if they have it.

Work only from what they give you. Never guess a number.

## Work down this list, stop at the first failure

1. **Authentication.** SPF, DKIM, DMARC and MX present and passing on every sending domain, with the From domain aligned to SPF or DKIM. Use the free SPF, DKIM and DMARC checker at workinsiders.com/free-tools/spf-dkim-dmarc-checker/. Watch for SPF records over the 10-lookup limit, which fail silently. Since 5 May 2025 Microsoft rejects mail from senders of more than 5,000 a day to Outlook.com, Hotmail and Live addresses that fail SPF, DKIM or DMARC, with `550 5.7.515`. Since November 2025 Gmail increasingly returns temporary (4xx) and permanent (5xx) rejections for non-compliant mail.
2. **Bounces, read by code.** Bounced / sent per mailbox. Target under 2%. Over 2%: check the list. Over 3% on 100+ sends, or over 5% at any point after 50 sends: pause the campaign. Then group the bounce codes:
   - `5.1.1`, `5.1.10`, `5.4.1` (address not found or access denied): dead addresses, often ones a catch-all server accepted at first. A list problem; go to list-verification-gate.
   - `5.7.x` (policy, reputation or block): **the serious one.** Slow down, confirm warmup is on, stop sending to the provider that blocks, let the domain rest.
   - `5.2.2` (mailbox full): usually temporary; suppress the address if it repeats.
   - If most bounces were marked "valid" by the verifier, re-check them with a different verifier. If most were catch-alls, no verifier will fix it; send fewer of them.
   - Many bounces from domains behind Mimecast, Proofpoint or Barracuda: in practitioners' experience those gateways often reject new cold senders on policy. Send to them in a small separate batch from the healthiest mailbox, and move a domain to phone or LinkedIn only after a `5.7.x` bounce from it.
3. **Spam complaints.** Gmail expects a spam rate below **0.1%** and treats **0.3%** as the line where mail starts to be blocked. A few complaints on small volume can cross it. Causes: wrong people, a hidden or missing opt out, too many follow-ups, misleading subjects.
4. **Volume.** More than about 30 cold emails per mailbox per day, a sudden jump, or warmup switched off. Fix: drop back to the ramp in sending-setup-plan and add mailboxes instead of raising per-mailbox limits.
5. **Content.** Links, domains or email addresses in the first email (signature included), tracking links, open tracking on, images, attachments, HTML, spam words ("free", "guaranteed", "act now"), or identical text thousands of times. Paste it into the free cold email spam-word checker (workinsiders.com/free-tools/cold-email-spam-checker/). Fix: plain text, no first-email links, open tracking off, spintax from email-variants-spintax.
6. **Targeting.** Many people per company, role inboxes, or a segment with no reason to care. Low replies with clean numbers is an offer or list problem, not a spam problem; send it to recruitment-offer-builder.
7. **Blocklists.** Check the sending domains on the major public blocklists. A listing usually follows steps 2 and 3, so fix those first. If you cannot check, ask the recruiter for the results.
8. **Provider split.** Replies only from Gmail and never from Outlook (or the reverse) points to one provider. Check authentication, then volume to that provider's recipients.

## Placement test

If the cause is unclear, send the current email to a few test inboxes at Gmail, Outlook and Yahoo the recruiter controls (or with a placement tool they already have) and record inbox, promotions or spam.

## The restart plan

- Pause cold sending on the affected domains. Keep warmup running.
- Fix the root cause first (list, authentication, content, volume).
- Rest two to four weeks on warmup only, then restart at the week-one ramp. If it does not recover, retire the domain and move to the spare.
- Never move a bad list to a fresh domain; it will burn that one too.

## Output

The cause found with the evidence, the fix, the restart dates, and what to watch for the next 14 days. If several things are wrong, list them in the order to fix.

## Rules

- Never suggest tricks to fool filters: hidden text, misspelled spam words, image-only emails, fake "Re:" subjects, or rotating new domains to keep a bad list going.
- Say plainly when the honest answer is "this list should not be emailed".
