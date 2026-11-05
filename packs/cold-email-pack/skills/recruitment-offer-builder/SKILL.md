---
name: recruitment-offer-builder
description: "Turns \"we are a recruitment agency\" into a specific cold email offer a hiring manager wants to reply to, such as a blind candidate profile, a pay snapshot, a shortlist by a date or a risk reversal from the agency's own guarantee, plus up to three message angles per segment. Use when a recruiter asks \"what should I offer in cold email\", \"our BD emails get no replies\", \"how do I stand out from other agencies\", \"lead magnet for recruitment\", \"offer for hiring managers\", or \"angles for my cold email campaign\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Recruitment offer builder

Hiring managers get emails from agencies every week, and nearly all say the same thing: "we are a specialist agency, can we help with your hiring?" The offer is the part that makes one worth answering. Copy cannot rescue a weak offer, and more volume will not either.

If `references/agency-profile.md` exists, read it first: specialties, guarantee, fees, proof points, exclusive options. Use only those terms. Never invent a guarantee, a time to fill or a placement count.

## Offer types that work for agencies

Pick the ones the agency can actually deliver for this segment:

1. **The candidate.** A strong, available person who fits roles the company hires for (an MPC email). Highest reply potential, but only with the candidate's permission and a blind profile. Use mpc-email-campaign to write it.
2. **The shortlist.** "Three screened [role] profiles in [n] days if it's useful." Only promise a number of days the recruiter confirms.
3. **The market snapshot.** A short note, at no charge, the recruiter can really produce: pay ranges they are seeing for the role in that city, how many similar roles are open nearby, or where the people they want work now. Never invent figures; the recruiter supplies them.
4. **The risk reversal.** The agency's real guarantee or terms said plainly: "no fee unless you hire", "replacement at no charge within [the profile's replacement period]". Only what is in the profile.
5. **The peer proof.** "We filled [role] for two [industry] companies in [region] this year." Only with real, shareable facts.
6. **The second opinion.** For roles open a long time: "happy to tell you what I'd change in the job ad, no strings." Use when the agency can genuinely help.
7. **Contract cover.** A contractor available to start within [n] days to cover the gap while a perm hire is found (rate on request). Only with a real, available contractor.

Dead offers: "free consultation", "free audit", "do you have any roles?". Readers know a sales call in disguise. Whatever you offer must be something you send in the reply, not a reason to book a meeting.

In the email itself write "no charge" or "on us", not "free", and "replacement period", not "guarantee"; both words trip spam filters.

A generic resource (salary guide, hiring checklist) is a softer offer. It gets more replies from people with no live need and fewer job orders. Say this when the recruiter picks it.

## Test the offer

For each candidate offer, answer in one line each:
- Would a busy hiring manager with this trigger care this week?
- Can the agency deliver it to every person who says yes?
- Is it specific (a role, a number, a date) or could any agency say it?
- What does the reader have to do to get it? It should be a one-word reply.

Drop any offer that fails the second question.

## Angles

An angle is the reason this email exists for this reader now. Write up to three per segment, each tied to a different trigger or pain:

```
Angle A: [trigger] -> [pain in their words] -> [offer] -> [one-line ask]
Angle B: ...
Angle C: ...
```

Examples for a manufacturing engineering desk:
- Role open 45 days -> line still short-handed -> two available controls engineers within 50 miles -> "want the blind profiles?"
- New plant announced -> 20+ hires coming -> a one-page hiring plan for the first 90 days, no charge -> "want me to send it over?"
- Competitor layoffs nearby -> good people on the market now -> a short list of who is open to move -> "would that be useful?"

Mark which angle to lead with and which to save for the follow-ups or the A/B test.

## Rules

- Never quote fees in the offer unless the recruiter asks; terms belong on a call or in a proposal.
- Never promise exclusivity, discounts or guarantees that are not in the profile.
- Never imply a candidate is available, or a client is hiring, without evidence.
- Hand the approved offer and angles to bd-cold-email-sequence or mpc-email-campaign.
