---
name: candidate-database-campaign
description: "Plans and writes an email campaign to candidates already in a recruitment agency's ATS or CRM about a new job, choosing who to include from their recorded work history, checking consent and data age first, and writing a short, honest email that brings old candidates back. Use when a recruiter asks to \"email my database about a new job\", \"mine the ATS\", \"re-engage old candidates\", \"database campaign\", \"who in my database fits this role\", or \"email blast for a new job order\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Candidate database campaign

An agency's own database is its warmest candidate list, and the one most often wasted on a mass blast. You turn it into a short, targeted campaign: the right people, a real role, a reason they are hearing from you, and their data handled properly.

If `references/agency-profile.md` exists, read it first: ATS, whether to name the client, opt-out line, mailing address, countries emailed.

## Step 1: who to include

Ask for the job order and an export of matching candidates (or the search the recruiter ran). Include people on work facts only:
- Their recorded skills, titles and experience fit the role's must-haves.
- Their location or stated relocation stance fits.
- Their last known pay expectation is not far from the range (if recorded).

Exclude:
- Anyone who opted out of email, asked not to be contacted, or was marked do-not-contact.
- Anyone placed by the agency in the last 12 months, or the period the agency's guarantee or ethics rule sets, unless the recruiter says otherwise.
- Anyone currently working at a client where the agency has off-limits terms.
- Anyone whose record is older than the agency's data retention period, or whose consent or notice cannot be shown where the law needs it.

Never include or exclude anyone by age, gender, ethnicity, nationality, disability, family status or any other protected trait, or by guesses from names or photos. Report the counts at each step.

## Step 2: check the data first

- Records older than about 12 months: verify emails with list-verification-gate before sending; old databases bounce.
- Note how each person entered the database (applied, referred, sourced) and when they last heard from the agency. That sets the opening line.
- In the UK, EU and other places with data laws, the agency needs a lawful basis to email and must honour objections. cold-email-compliance-check lists what to confirm with the adviser.

## Step 3: the email

Group the list by how recent the contact was, and write one opening per group:
- Spoke in the last 6 months: "We spoke in [month] about [their area]. A role came in that fits what you said you wanted."
- Older contact: "You were in touch with us back in [year]. Not sure where things stand now, but this role made me think of your background."

Then, in under 100 words: the role title, location and pattern, pay range, the one thing that sets it apart, and one small ask ("Interested, or should I take you off this kind of role?"). Sign off, one opt-out line, and the mailing address for US recipients.

Offer a second short email 5 working days later only to those who did not reply, then stop.

## Step 4: update the records

Ask the recruiter to log every reply in the ATS: interested, not now (with a date to come back), not interested in this kind of role, opt out. Opt outs are permanent across every campaign.

## Output

The inclusion and exclusion counts, the groups, the email for each group with merge fields, the follow-up, and the ATS update notes.

## Rules

- Never send one email to the whole database "in case". Target by fit.
- Never reveal other candidates, clients the person did not apply to, or why a past application did not progress.
- Never imply a role is exclusive or closing soon unless the recruiter confirms it.
