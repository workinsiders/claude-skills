---
name: target-account-list
description: Turns a target profile and a rough list of companies into a short, checked account list: each company tested against the profile as yes, no or unknown with a source, a hiring signal noted, a warm path flagged, and a count the desk can actually work this week. Use when a recruiter says "build my target list", "which companies should I call", "account list", "prospect list", or pastes 40 logos with no reason to write to any of them.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Target account list

Forty logos with no reason to write is not a list. You help a recruiter cut a rough list down to the accounts worth a message this week, with the reason written next to each.

If `references/agency-profile.md` exists, read it for specialties, markets and any clients or companies the agency must not approach (current clients' competitors under exclusivity, off-limits agreements).

## Input

- The outreach target profile, or the recruiter's two-line brief ("mid-size manufacturers in Georgia hiring controls engineers").
- The rough list: company names, an export from their CRM or ATS, or a list they built themselves.
- Any signals already found.

## Check each company

For every company, mark each line yes, no or unknown, and give the source (a link, or "your notes"):

- Fits the profile (industry, size, location).
- Hires the roles the desk fills.
- Has a current hiring signal.
- Is not off limits (existing client conflict, do-not-contact, competitor under exclusivity).
- Has a warm path (someone the recruiter knows), if known.

Unknown is a fine answer. Never turn unknown into yes.

## Output

```
TARGET ACCOUNT LIST | [brief] | [date]
Work this week (max 10):
| Company | Fit | Signal (date, link) | Warm path | Why now, in one line |
Next week (fits, no signal yet): [companies + the page to watch]
Dropped: [company: reason]
Unknowns to check: [list]
Next: warm-path-check, then company-fact-sheet for the top 3
```

## Rules

- Rank companies by fit and signal, never by guesses about the people who work there.
- Do not buy, scrape or invent data. Work only from what the recruiter supplies or public pages.
- Respect do-not-contact and opt-out lists the recruiter gives you. A company or person on them stays off.
