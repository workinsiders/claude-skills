---
name: bd-cold-email-sequence
description: "Writes a sequencer-ready cold email sequence that sells a recruitment agency's services to hiring managers, HR leaders and founders. Short plain-text emails built on one hiring signal and one offer, with subject lines, merge fields, timing and one clean opt out. Use when a recruiter asks for a \"cold email sequence to win clients\", \"BD campaign for my agency\", \"email sequence for hiring managers\", \"Instantly sequence for recruitment\", \"follow-up steps for my BD sequence\", or \"rewrite my BD sequence\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# BD cold email sequence

You write the sequence a recruitment agency sends to win job orders. It must read like one sharp recruiter wrote it to one hiring manager, even when it goes to 300. For a single one-off email to one prospect, client-bd-outreach in the Agency Recruiting Pack is the better fit.

If `references/agency-profile.md` exists, read it first: specialties, markets, proof points, guarantee, sender name, mailing address, opt-out line, words never used. Never invent proof points, numbers or client names. Where a fact would help and you lack it, write `[add: ...]` for the recruiter.

## Inputs

Ask for, or take from the campaign brief:
- The segment (role family, buyer title, trigger) from recruitment-icp-builder.
- The offer and angles from recruitment-offer-builder.
- The merge fields in the list (from lead-list-builder), so you only use fields that exist.
- The sequencer, for merge-field syntax.

## The first email

- **Subject:** 2 to 4 words, lowercase, reads like an internal note: `controls engineer search`, `{{company}} hiring`, `still hiring for the controls role?`. No hype, no emojis, no "!", no fake "Re:" or "Fwd:".
- **Sentence 1, their world:** the first name inline, then the signal. "{{firstName}}, saw the controls engineer role at {{company}} has been open since September." Never "Hope you're well", "My name is", "I came across your profile" or "I wanted to reach out".
- **Sentence 2, the offer:** what you can hand them, as a statement. "I'm working with two controls engineers within 50 miles who are open to a move."
- **Sentence 3, proof:** one specific, true line. "We placed four controls engineers with plants around Toledo this year. All four are still there." Skip it if there is no real number.
- **The ask:** a pure interest check, and the only question in the email. "Want me to send the blind profiles?" or "Reply 'yes' and I'll send them across." Do not ask for a call, a meeting or "15 minutes" in a cold email; time asks belong in the reply thread.
- **Sign off:** first name, then agency name on the next line. Phone is fine. **No links, website domains or email addresses anywhere in the first email, signature included.**
- **ps (optional):** a second proof point. It is often the most-read line.
- **Opt out:** exactly one line, for example "If this isn't relevant, reply 'no' and I'll stop." Then the mailing address for US recipients. Check the sequencer is not adding a second one.

**If the offer is candidate profiles**, the candidates must exist today, have given written permission to be marketed to this segment, and have an approved blind profile: run Gates 1 and 2 of mpc-email-campaign first. If not, use a different offer (a shortlist by a date, a market snapshot).

**Length:** 50 to 90 words, one sentence per paragraph, read on a phone in ten seconds. More "you" than "we".

## The sequence

Default for most agency segments, counted in working days so a Friday start never lands two emails close together:

1. **Email 1:** the first email.
2. **+3 working days:** same thread, no new subject. Re-ask the same offer in different words in two or three sentences, or add the proof line if email 1 had none. Never "just following up" or "bumping this".
3. **+4 to 6 working days:** same thread. One useful question that also catches the wrong-person case: "Is the controls role still open, or is someone else running it?"
4. **Optional, about 4 weeks later:** a new thread with a new subject and a **different angle** from the offer builder (for example a market snapshot instead of profiles), with no reference to the first thread. Then one nudge 3 working days later in that thread.

Every step, same-thread follow-ups included, keeps the one opt-out line and (US) the mailing address.

Stop there. No more than five emails per person, and never email again after a "no". Aging-role lists go stale fast: rebuild them every two weeks, since roles get filled.

Send on weekdays, inside business hours in the reader's time zone.

## Warm segments

Past clients, hiring managers who moved company, placed candidates now in hiring roles and closed-lost deals are warmer than cold. Open with the real link instead of the signal ("We worked together on the plant manager search at Midwest Polymer in 2024"), leave out the proof line, and keep the same offer and ask. Only state a link that is in the agency's records.

## Merge fields

- Use only fields every row has. Rows with an empty `{{signal}}` go in a different campaign; never rely on a fallback syntax the recruiter has not confirmed.
- `{{company}}` is the short name people say, not the legal name.
- Never claim research you did not do for every row ("I looked at your careers page") unless it is true for each one.
- A personal first line (`{{line}}`) is optional and must link to the hiring need.

## Words and moves to avoid

"Just checking in", "touching base", "circling back", "partnership opportunity", "partner with you on your hiring needs", "top talent", "best-in-class", "exciting opportunity", "leverage", "synergy", "worth a chat?", "worth exploring?", "free" (write "no charge" or "on us"), "guaranteed" (write "replacement period"), guilt ("I never heard back"), exclamation marks, all caps, em dashes, more than one question per email, and anything in the profile's "Words we never use". No attachments ever.

## Output

For each email: day, subject (or "same thread"), body with merge fields, and a one-line note on why it is there. Then each email with sample values filled in, with the word count. Then hand it to email-variants-spintax and cold-email-compliance-check.

## Rules

- Never name or identify a candidate. Use mpc-email-campaign for candidate-led emails, with permission.
- Keep fees out of the sequence. If a prospect asks, cold-email-reply-handler answers from the profile.
- Never disparage the prospect's current agencies or internal team; frame a long-open role as a thin market, never as their recruiter failing.
- Honour every "no", every unsubscribe and every "wrong person" for good, across every campaign.
