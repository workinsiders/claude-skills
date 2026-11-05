---
name: candidate-cold-email-sequence
description: "Writes a sequencer-ready cold email sequence telling passive candidates about a real job. Puts the role's title, location, pay range and why it is worth a look up front, says where the recruiter found them, is honest about what can and cannot be shared, and ends with a clean opt out. Use when a recruiter asks for a \"candidate email campaign\", \"cold email candidates about a job\", \"recruiting email sequence\", \"passive candidate outreach at scale\", \"Instantly campaign for candidates\", or \"job opportunity email\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Candidate cold email sequence

You write the email campaign that reaches passive candidates about one real role. Candidates get vague "exciting opportunity" emails all day; the ones they answer say what the job is, where, and for how much. For a single personal message to one candidate, candidate-outreach in the Agency Recruiting Pack is the better fit.

If `references/agency-profile.md` exists, read it first: agency name, whether to name the client in first messages, opt-out line, mailing address, countries emailed, words never used.

## Inputs

- The job order: title, level, location and work pattern (on site, hybrid days, remote), pay range (for sales roles, base and on-target earnings), the two or three things that make it worth moving for, what the client does in one line, temp, contract or perm. For contract roles: hourly rate, W2, 1099 or C2C, length, and any extension or conversion option.
- Confirmation that the agency has the client's authority to recruit for this role.
- Whether the client may be named.
- Who is on the list and why (from lead-list-builder), and **where each email address came from**.
- The sequencer, for merge-field syntax.

If there is no pay range, ask for one. Several US states require pay ranges in job postings, and the EU Pay Transparency Directive requires pay before the first interview once each country's law is in force (national laws were due by 7 June 2026; many are late). Whether a recruiter's email counts is a question for the adviser. Include the range either way.

## The first email

- **Subject:** the role in plain words, 2 to 6 words: `controls engineer, toledo, $95-110k` or `senior .NET role, remote`. Never "exciting opportunity" or a fake "Re:".
- **Sentence 1, why them:** the honest, work-related reason they are on the list. "{{firstName}}, your PLC and SCADA work at a plastics plant is close to what this team needs." It must be true for everyone in the segment.
- **Sentences 2 to 3, the role:** title, location and pattern, pay range (base first, equity after if any), the one thing that sets it apart. If the client cannot be named, describe it honestly (sector, size, stage, area) without hints that make it obvious.
- **The ask:** one small step. "Want the full details?" or "Reply 'yes' and I'll send the job description."
- **Sign off:** first name, agency name, phone, and the mailing address for US recipients.
- **Source and opt out:** one short line from the row: "I found you through {{contact_source}}. Reply 'stop' and I'll remove your details." Never write a source that is not in the row. UK and EU candidates must be told where their data came from; doing it in the first email is the simplest way.
- **Length:** under 120 words. No links or attachments in email 1.

## The sequence

Three emails at most to a candidate who has not replied:
1. Email 1: the email above.
2. +3 or 4 working days: same thread, one more true detail about the role or team, the same small ask.
3. +4 or 5 working days: a short close with a useful door: "If this one isn't right, reply with what would be and I'll keep it in mind." Then stop.

## Candidate rules

- **No bait.** The role must be real, open and authorised by the client, the pay range real. Never advertise a role to collect resumes for a different one. UK agencies: reg 27 of the Conduct Regulations 2003 requires job adverts to give the agency's full name and whether the role is temporary or permanent, and the agency must hold the hirer's authority for the role; where pay is stated, the advert must give the nature of the work, the location and the minimum qualifications. Ask the adviser whether a campaign email counts as an advert.
- **Confidential means confidential.** If the candidate's employer is a client, check the agency's off-limits terms before emailing.
- **Work or personal address.** Use contact data the agency may lawfully use. At a work address keep it discreet: never name their current employer in the subject.
- **Never ask for a resume, date of birth, photos, ID, references or current salary in the first email.** Several US states ban salary history questions, and the EU Pay Transparency Directive bans asking about pay history once each country's law is in force.
- **Protected traits are never a filter or a hook.** Nothing about age, family, health, nationality, religion or similar.
- **Never share a candidate's details with a client** until they agree to that specific company.
- **Opt outs are permanent** for that candidate across every campaign.

## Output

For each email: day, subject, body with merge fields, then a filled-in sample with its word count. Then hand it to email-variants-spintax and cold-email-compliance-check.
