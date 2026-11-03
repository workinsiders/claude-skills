---
name: company-fact-sheet
description: Builds a short, sourced fact sheet on one company before outreach or a call: up to twelve numbered facts, each with a link and a date, the hiring picture, unknowns written as unknown, and questions to ask instead of guesses. Use when a recruiter says "research this company", "account research", "what do I need to know before I call", or has twenty minutes and refuses to write from a guess.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Company fact sheet

A message that gets one fact wrong loses the reader. You help a recruiter learn what is true about a company in twenty minutes, with a source for every line.

If `references/agency-profile.md` exists, read it for the desk's specialties so the hiring picture focuses on roles the desk fills.

## Input

- The company name and website.
- Any pages the recruiter pastes or links: careers page, job posts, press releases, news articles, annual report, LinkedIn company page. If you can browse, read only public pages and list which ones you read; if you cannot, work only from what was pasted.

## Build it

1. **Facts.** Up to twelve, numbered. Each one: the fact in plain words, the date, the link. If two sources disagree, record both.
2. **Hiring picture.** Open roles the desk could fill (title, location, date first seen), recent hiring announcements, the size of the function if published.
3. **Unknowns.** What you looked for and could not find. Write it as unknown.
4. **Questions.** Turn every guess you were tempted to make into a question for the first call.

## Output

```
COMPANY FACT SHEET: [Company] | [date] | sources read: [n]
Facts:
1. [fact] ([date], [link])
...
Hiring picture: [roles, dates, links]
Unknowns: [list]
Questions to ask, not assume: [list]
Next: contact-finder-brief, then reason-to-write
```

## Rules

- No source, no fact. Drop anything you cannot link; never soften it into "reportedly".
- Do not invent revenue, headcount, funding or growth figures.
- Company facts only. Nothing about individuals' private lives.
- A thin result stays thin. Say "only three facts found" rather than padding.
