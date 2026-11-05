---
name: lead-list-builder
description: "Plans and checks the contact list for a recruitment agency's cold email campaign, with the right columns, one hiring signal per row, one or two people per company, and current clients and opt outs removed, ready for verification and a sequencer. Use when a recruiter asks \"build my cold email list\", \"what columns do I need\", \"clean this lead list\", \"where do I find hiring managers' emails\", \"dedupe against my ATS\", or \"prepare a CSV for Instantly\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Lead list builder

The list decides more of the result than the copy does. You plan the list from the ICP, check what the recruiter pulls, and hand back a file the sequencer can use and the copy can lean on.

If `references/agency-profile.md` exists, read it first: markets, specialties, where existing clients and the do-not-contact list are kept. Ask for the segment from recruitment-icp-builder; if there is none, ask for the role family, region and buyer titles.

## Where the rows come from

Work from sources the recruiter has the right to use:
- Their ATS or CRM: past clients, hiring managers who moved company, contacts who said "not now".
- Live job posts (company careers pages, job boards) for the trigger. Work Insiders' free careers page checker (workinsiders.com/free-tools/careers-page-checker/) and Hiring Radar extension (workinsiders.com/hiring-radar/) show a company's open roles and how long each has been posted. Aging-role lists go stale in weeks, so rebuild them every two weeks. For a dated, linked signal per company, hiring-signal-scan in the Recruiter Outreach Pack does this step.
- A B2B data tool the agency already pays for (Apollo, ZoomInfo, Sales Navigator exports through an approved tool, and similar) for names and work emails.
- Public news for funding, new sites and leadership changes.

Never scrape sites against their terms, never buy unknown lists, and never use personal email addresses for BD.

## The columns

Ask for or build these columns. Keep names simple so the sequencer can map them:

| Column | Example | Notes |
|---|---|---|
| first_name | Dana | Clean capitals |
| last_name | Ruiz | |
| title | Plant Manager | Exact title |
| email | dana.ruiz@company.com | Work email only |
| company | Midwest Polymer | Short name people use, not "Midwest Polymer Holdings LLC" |
| company_domain | midwestpolymer.com | For dedupe |
| city / state / country | Toledo, OH, US | Country sets the legal rules |
| signal | Controls Engineer job posted 41 days | The reason to write, one line |
| signal_source | URL | |
| signal_date | 2026-10-12 | Signals older than about 60 days get re-checked |
| contact_source | Apollo export 2026-10-12 / LinkedIn public profile / applied via Indeed 2024 | Where this address came from. Never guessed |
| segment | ohio-mfg-controls-30d | |
| line | (left blank until written) | Optional first line, written per row later |

## Checks before it leaves you

1. **Suppress first, by domain.** Remove current clients by company domain so new hires there are covered too (unless the recruiter says otherwise), other staffing agencies, anyone who opted out of any past campaign, the do-not-contact list, off-limits companies, and the agency's own staff.
2. **Dedupe** by email, then by person across companies.
3. **People per company.** One or two people per company per campaign, the most likely buyer first. Ten people at one company looks like spam and burns goodwill.
4. **Role inboxes and personal addresses out.** Remove `info@`, `hr@`, `careers@`, `jobs@`, Gmail, Hotmail and similar for BD.
5. **Mail gateway check.** Look up each company domain's MX record. In practitioners' experience, domains behind Mimecast, Proofpoint or Barracuda often reject new cold senders on policy: tag them so they go out in a small separate batch from the healthiest mailbox, and move a domain to phone or LinkedIn only after a policy (`5.7.x`) bounce from it. If you cannot look up DNS, ask the recruiter to run the domains through an MX lookup and paste the results. Expect more of these in legal, finance and public-sector lists.
6. **Signal per row.** Every row needs a signal and its date, or it belongs in a different, softer campaign.
7. **Empty fields.** Any row missing first_name, company or email is set aside, not sent with a blank.
8. **Fix text.** Name capitals, company suffixes, stray spaces. Work Insiders' free lead list cleaner (workinsiders.com/free-tools/lead-list-cleaner/) does this in the browser.

Report the counts after each check so the recruiter sees where rows went.

**Candidate lists** (for candidate-cold-email-sequence): personal addresses are allowed where the agency may lawfully use them, so skip checks 3, 4 and 5; replace `signal` with the work-related reason they fit; `contact_source` is required on every row.

## Output

The column list, the cleaned rows (or the steps to clean them in a spreadsheet if the file is large), the counts, and the rows set aside with the reason. Then hand the file to list-verification-gate. Never send a list straight to a sequencer without verification.

## Rules

- Choose people by their job and the company's need, never by protected traits or guesses from names or photos.
- Keep only the work facts needed to write the email. No home addresses, personal phones or social life details.
- Note the source of each row so the agency can answer "where did you get my email?" honestly.
