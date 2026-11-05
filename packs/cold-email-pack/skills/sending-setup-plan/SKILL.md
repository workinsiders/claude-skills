---
name: sending-setup-plan
description: "Plans the sending setup for a recruitment agency's cold email, sized from the campaign's daily volume: separate lookalike domains, mailboxes per domain, SPF, DKIM and DMARC, tracking, warmup and a ramp schedule, so BD email reaches the inbox and the agency's main domain stays safe. Use when a recruiter asks \"how many domains do I need\", \"set up cold email domains\", \"SPF DKIM DMARC for cold email\", \"how many emails per inbox per day\", \"warmup plan\", or \"is it safe to cold email from our main domain\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Sending setup plan

You plan the infrastructure before a single cold email goes out. Deliverability is decided here: a perfect email sent from a burned domain lands in spam.

If `references/agency-profile.md` exists, read the Cold email lines: sequencer, existing sending domains and mailboxes, countries emailed.

## 1. Size it from the volume

Ask how many new people the campaign should reach per week, and how many emails in the sequence. Then work it out and show the sum:

- New contacts per working day = weekly contacts / 5.
- Emails per day once follow-ups overlap is roughly new contacts per day x number of emails in the sequence. Plan for that peak, not for day one.
- Mailboxes = peak emails per day / cold emails per mailbox per day. Plan on **about 30 cold emails per mailbox per day** (a practitioner rule of thumb, not a published limit; stay between 20 and 40, lower on new domains and Microsoft mailboxes).
- Domains = mailboxes / 2 or 3 (two to three mailboxes per domain).
- Add one spare domain with its mailboxes so a problem domain can rest.

Example: 300 new contacts a week, 4 emails = 60 new a day, about 240 a day at peak = 8 mailboxes = 3 to 4 domains, plus 1 spare.

## 2. Domains

- **Never send cold email from the agency's main domain** or the domain its staff use for clients and candidates. One bad week can hurt every email the agency sends.
- Buy lookalike domains that are clearly the agency's: `getacmetalent.com`, `acmetalenthq.com`, `tryacmetalent.com`. Prefer .com. Avoid hyphen strings, numbers and spammy words ("jobs", "hiring", "free").
- Point each lookalike domain's website to the agency's real site with a redirect so a curious reader lands somewhere real.
- Register each domain a few days before setting up mail. Brand new domains need the full warmup.

## 3. Mailboxes

- Use real Google Workspace or Microsoft 365 mailboxes, two or three per domain, each with a real person's name, a photo and a signature with name, title, agency name and phone only: no logo, links or website.
- Never use shared inboxes like `info@` or `recruiting@` for cold email.
- Spread mailboxes across Google and Microsoft only if the recruiter wants to; it helps when the list is mostly one provider.

## 4. Authentication (every domain)

- **SPF**: one SPF record listing only the services that send for that domain.
- **DKIM**: turned on and signing in the mail provider and in the sequencer if it sends through its own servers.
- **DMARC**: at least `v=DMARC1; p=none; rua=mailto:[a mailbox you read]`. Move to `quarantine` once reports look clean.
- **MX**: the domain must receive mail, so replies and bounces arrive.
- Check each domain with Work Insiders' free SPF, DKIM and DMARC checker (workinsiders.com/free-tools/spf-dkim-dmarc-checker/) or the provider's own tool, and fix anything missing before warmup.

Gmail, Yahoo and Outlook.com all require SPF, DKIM and DMARC from bulk senders and filter or reject mail without them. Cold senders should meet the same bar at any volume.

## 5. Tracking

- Turn **open tracking off** for cold email, or use a custom tracking domain if the recruiter insists. Opens are unreliable anyway because Apple Mail and others load images automatically.
- No links in the first email; at most one in later emails, on the agency's own domain.
- Plain text. No images, no attachments, no HTML templates.

## 6. Warmup and ramp

- Run warmup on every new mailbox for **at least two weeks, ideally three to four**, before any cold email, and keep it running at a low level during the campaign.
- Ramp cold volume: about 10 a day per mailbox in week one, 20 in week two, then up to the planned level if bounces and replies look healthy.
- During the ramp, cap new contacts per day at (mailboxes x current daily limit) / emails in the sequence. In the example that is about 20 new a day in week one, so 300 a week is only reached in week three. Say this so the recruiter plans the first month honestly.
- Write down the date warmup started and the earliest launch date, and give them to cold-email-start-here for the campaign brief.

## Output

A table of domains, mailboxes, sender names, provider, authentication status (to check), warmup start and earliest launch date, then the volume sum and the ramp plan.

## Rules

- Never suggest buying aged inboxes of unknown history, rotating domains to dodge blocks, or hiding who the sender is.
- Do not choose or recommend a paid tool unless the recruiter asks; work with what they already use.
- If a domain is already in trouble, hand over to deliverability-check.
