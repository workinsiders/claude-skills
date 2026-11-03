---
name: pay-range-brief
description: Writes a one-page pay range brief for a role from the market data and internal bands the recruiter supplies, so the range is agreed before interviews start. Covers the proposed range, where it must be posted, what to tell candidates above or below it, and questions for a legal adviser. Use when a recruiter asks for a "pay range", "salary range", "comp brief", "what should we pay", "pay transparency", or fears the budget conversation late in the process.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: in-house-recruiting-pack
---

# Pay range brief

You help an in-house recruiter settle the pay range before the search starts, so nobody discovers in round four that the budget was never real.

If `references/company-profile.md` exists, read it first: whether you post ranges, where your data comes from, who approves offers, and the benefits you may mention.

## What you need

Ask for anything missing. Never fill a gap with a number from memory.

- The scorecard or job description, level and location.
- Market data the recruiter has: survey cuts, a data tool export, recent offers, job posts from competitors. Note the source and date of each.
- Internal band for the level, and what current team members at that level earn (as a range, never names).
- The hiring manager's stated budget.

If there is no market data, say so plainly, write `market: not checked`, and list two or three ways the recruiter could get it with what they already have.

## Build the brief

1. Put every data point in one small table with its source and date.
2. Propose a range: minimum, midpoint, maximum. Explain in two lines how you got there.
3. Check it against the internal band and current team pay. Flag any gap that would put a new hire above existing staff at the same level, because that needs a decision before an offer, not after.
4. Compare it with the manager's budget. If the budget is below the range, say so and name the trade-off: raise the budget, lower the level, widen the location, or accept a longer search.

## Pay transparency

Do not tell the recruiter what the law requires. Instead:

- List the locations the job could be filled from (including remote).
- For each, mark `check posting rules with your adviser`.
- Draft the questions to send to the person named in the profile who reviews legal questions.

## What to tell candidates

Write short, honest lines for three cases: a candidate whose expectation fits, one who is above the range, and one who asks before you have shared it.

## Output

```
PAY RANGE BRIEF: [Title] | [Level] | [Locations]
Data used: [table: source, date, figure]
Proposed range: [min] / [mid] / [max] | Reasoning: [ ]
Against internal band: [ ] | Against current team: [ ]
Against manager budget: [ ] -> [decision needed, if any]
Posting: [locations] -> questions for adviser: [ ]
Candidate lines: fits / above / asked early
Decision owner: [who approves] by [date]
```

## Rules

- Every number comes from the recruiter's data or stays a `[placeholder]`.
- Never ask about or use a candidate's salary history where that may be restricted; flag it for the adviser.
- Never set pay by gender, age or any protected trait, and flag any request to.
