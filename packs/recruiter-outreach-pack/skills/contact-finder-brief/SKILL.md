---
name: contact-finder-brief
description: Works out who at a company actually owns the hire the recruiter can help with, from public sources: the hiring manager, the function leader, HR or TA, and which one or two to contact first, with an identity check so a namesake is never messaged by mistake. Use when a recruiter says "who should I contact", "find the hiring manager", "who owns this req", "decision maker", or the search returns three people with the same name.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Contact finder brief

Writing to the wrong person wastes the best signal. You help a recruiter pick who to contact, and confirm it is the right person, using only public, work-related information.

If `references/agency-profile.md` exists, read it for the agency's rules on contacting HR versus hiring managers directly.

## Input

- The company fact sheet or the company name.
- The role or function the outreach is about.
- Any public pages the recruiter pastes or links: the job post (which often names the team), company team pages, press releases, conference speaker pages, public professional profiles.

## Step 1: who owns the hire

List the roles that usually decide and influence this hire at a company this size:
- **Owns it:** the hiring manager for the team.
- **Funds or approves it:** the function leader.
- **Runs the process:** HR or TA.

Then match people who are publicly named in those roles, each with the source.

## Step 2: identity check

For every person you name, test each source for the same name and the same company and role. If sources disagree (a namesake at another company, an old title), set them aside. Mark each person `confirmed` or `not confirmed`.

## Step 3: pick one or two

Recommend who to contact first and why, and whether a warm path exists (from the warm-path-check).

## Output

```
CONTACT BRIEF: [Company] | [function] | [date]
| Role | Person as published | Source | Confirmed? |
Contact first: [name, why] | Then: [name, why]
Warm path: [yes, via ... / none]
Not found: [roles with no public name]
Next: reason-to-write
```

## Rules

- Work-related public information only. Never collect home addresses, personal phone numbers, family details or anything from personal social accounts.
- Do not guess email addresses or say a person "probably" holds a role. Unconfirmed stays unconfirmed.
- Never score or rank people. You are matching roles to names, not judging anyone.
