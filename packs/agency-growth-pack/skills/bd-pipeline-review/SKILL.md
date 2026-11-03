---
name: bd-pipeline-review
description: Reviews an agency's BD pipeline (prospects, proposals out, terms pending, new job orders) by evidence instead of hope: stages defined by what the client has actually done, a dated next step for every deal, stale deals named and closed or revived, and the gap to the 90-day goal. Use when a recruiter or owner says "pipeline review", "BD pipeline", "which deals are real", "forecast new clients", "my pipeline looks full but nothing moves", or pastes a CRM export.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: agency-growth-pack
---

# BD pipeline review

A pipeline full of "had a good call" is not a pipeline. You help a recruiter sort deals by what the client has done, and decide what to do with each this week.

If `references/agency-profile.md` exists, read the fee basis so the review can show potential fees as the recruiter's own estimate.

## Input

The recruiter's list of open BD opportunities: company, contact, last contact date, what happened, any proposal or terms sent, expected roles. A CRM export is fine.

## Stages by evidence

Place each deal by the last thing the client did, not by how the recruiter feels:

1. **Talking:** replied and agreed to a call.
2. **Need confirmed:** named a real open role or hiring plan.
3. **Terms sent:** asked for and received terms or a proposal.
4. **Terms agreed:** signed or accepted in writing.
5. **Job order live:** a role the desk is working.

## For each deal

- The evidence for its stage (quote or date).
- The next step, with a date, and who owns it.
- Days since the last client action. Over 21 days with no client action is **stale**: decide to revive with something new, or close it.

## Then

- **Gap to goal:** compare live and likely job orders with the recruiter's 90-day target if they give one (see bd-plan-90-day), using their own conversion history if they have it; otherwise ask, or show counts only.
- **This week:** the three deals to move, and the one to drop.

## Output

```
BD PIPELINE REVIEW | [date]
| Company | Stage | Evidence | Last client action | Next step, date, owner | Potential fee (recruiter's estimate) | Stale? |
Stale: revive [ ] / close [ ]
Gap to 90-day goal: [ ]
This week: move [3] | drop [1]
```

## Rules

- No stage without evidence. Unknown evidence drops the deal one stage.
- No invented win rates or forecasts. Use the recruiter's own history or show counts only.
- Judge deals by what happened, never by personal impressions of the people involved.
