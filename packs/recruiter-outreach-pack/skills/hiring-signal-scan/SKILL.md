---
name: hiring-signal-scan
description: Finds a real, dated, public reason to contact a company now: job posts open 30+ days or reposted, funding, a new site or contract, a new leader building a team, layoffs nearby that free up talent. Every signal carries a link and a date, and stale or private ones are set aside. Use when a recruiter asks for "hiring signals", "trigger events", "who is hiring", "why reach out now", or wants a reason better than "just checking in".
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Hiring signal scan

The best BD message answers "why now" with something true. You help a recruiter collect signals that are public, recent and sourced, and say plainly when there is none.

If `references/agency-profile.md` exists, read it for specialties and markets so you only keep signals the desk can act on.

## Input

- A company, a short list of companies, or the target profile.
- Any pages the recruiter pastes or links: careers page, job posts, press releases, news, the company's LinkedIn posts. If you can browse, read only public pages; if you cannot, work from what was pasted and say so.

## Signals worth keeping

| Signal | Why it matters | What to record |
|---|---|---|
| Role open 30+ days, or reposted | Internal search is struggling | Title, location, first seen date, link |
| Several similar roles at once | A team is being built | Titles, count, link |
| Funding round or big contract | Hiring usually follows | Amount if stated, date, link |
| New site, plant or office | Local hiring wave | Location, opening date, link |
| New leader in the function | New leaders build teams | Name and title as published, start date, link |
| Layoffs at a competitor | Talent is available | Company, date, link (candidate runs) |

## Set aside

- Anything older than about 90 days, unless the role is still open.
- Anything private, guessed or second-hand ("I heard they're hiring").
- Personal news about individuals (health, family, personal posts). Never use it.

## Output

```
SIGNAL SCAN: [Company] | scanned [date]
1. [Signal] | [date] | [link] | strength: strong / medium / weak
2. ...
Set aside: [signal, reason]
Best reason to write now: [one line, or "no reason yet: watch [page] and check again on [date]"]
Next: company-fact-sheet, then reason-to-write
```

## Rules

- No link and date, no signal. A weak result stays weak; do not pad it.
- Never claim a role is "hard to fill" or "urgent" unless the company said so. Write what you saw: "posted 47 days ago, reposted twice".
- Do not scrape, log in, or use anything that breaks a site's terms.
