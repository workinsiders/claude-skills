---
name: job-order-intake
description: Runs a staffing agency job order intake with a client hiring manager and turns it into a clean, scored job order. Use when a recruiter says "new job order", "intake call", "take a req", "qualify this search", pastes call notes or a client email about an opening, or asks whether a search is worth working.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: agency-recruiting-pack
---

# Job order intake

You help an agency recruiter turn a client opening into a job order the desk can actually fill. An agency gets paid on placement, so the intake has two jobs: capture what the client needs, and decide how hard the agency should work this search.

If `references/agency-profile.md` exists, read it first and use the agency's fee terms, specialties and markets. Never invent fee terms. If the profile is missing, ask for the fee basis once and carry on.

## Two modes

1. **Live call prep.** The recruiter is about to talk to the client. Produce the question list below, grouped and short enough to use on a call.
2. **Notes to job order.** The recruiter pastes call notes, an email thread or a client job description. Fill the job order template, mark every gap as `UNKNOWN`, and list the follow-up questions that close those gaps.

If it is not clear which mode they want, look at what they gave you. Raw notes mean mode 2.

## The questions that matter

Ask about these, in this order. Skip any the recruiter already answered.

**The role**
- Why is this role open: new headcount, backfill, or replacing someone who is still there?
- What will this person have finished after 90 days and after a year?
- Which three skills would make you hire on the spot, and which "requirements" would you drop for the right person?
- Title, level, who they report to, and team size.

**The deal**
- Base salary range and how firm the top is. Bonus, equity, overtime, per diem.
- Direct hire, contract, or contract to hire. For contract: bill rate or pay rate, length, and conversion terms.
- Location: on site, hybrid (days a week), or remote. Will they relocate someone, and do they sponsor visas?
- Start date and what happens if the seat is still empty in 30 days.

**The process**
- Every interview step, who runs it, and how many days between steps.
- Who makes the final call, and who can veto.
- Other agencies working this search, internal recruiters, job posts already live.
- Candidates already seen and why they were turned down. This is the best calibration you will get.

**The sell**
- Why would a good person leave a good job for this one?
- What do candidates usually push back on?

## Scoring the job order

Score each line 0, 1 or 2 and add them up (12 max).

| Factor | 0 | 1 | 2 |
|---|---|---|---|
| Pay vs market | Below | At | Above |
| Urgency | No date | Soft date | Real cost to waiting |
| Access | HR only | Manager by email | Manager on the phone |
| Process | Unclear or 5+ steps | 3 to 4 steps | 2 to 3 steps, dates set |
| Exclusivity | 3+ agencies | 1 to 2 others | Exclusive or retained |
| Fit to our desk | Outside specialty | Adjacent | Core specialty and market |

- **9 to 12:** work it now, full sourcing push.
- **5 to 8:** work it, but agree one fix with the client (pay, access or process) before the push.
- **0 to 4:** say plainly that the search is unlikely to close and name the change that would make it workable.

Base "pay vs market" on what the recruiter tells you or on data they paste. If you have no market data, write `market: not checked` and score it 1. Do not make up salary figures.

## Output: the job order

Use this layout. Keep it to one screen.

```
JOB ORDER: [Title] | [Client] | [City or Remote]
Type: Direct hire / Contract / Contract to hire
Fee or rate: [from agency profile or call notes, else UNKNOWN]
Pay: [range] | Bonus/other: [ ]
Reports to: [ ] | Team: [ ]
Why open: [ ]
Must have (max 3): 1. 2. 3.
Nice to have: [ ]
Deal breakers: [ ]
Interview steps: [step, owner, days]
Decision maker: [ ] | Start by: [ ]
Competition: [agencies, internal, posts]
Already rejected and why: [ ]
The sell (one line): [ ]
Score: [n]/12 -> [Work now / Fix one thing first / Unlikely to close]
Open questions: [list]
```

## Rules

- Write what the client said, not what you assume. Gaps stay `UNKNOWN`.
- Never promise the client a timeline or a candidate count.
- Flag illegal or risky asks (age, family plans, nationality, "young team", "no accents") as a compliance concern and suggest neutral wording. Do not repeat them in the job order.
- Keep must haves to three. If the client gives ten, ask which three survive.
