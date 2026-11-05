---
name: recruitment-icp-builder
description: "Builds the ideal client profile for a recruitment agency's cold email campaign and turns it into list filters, segments and exclusions a data tool can run. Use when a recruiter asks \"who should I cold email\", \"build my ICP\", \"which companies should we prospect\", \"what titles should I target for BD\", \"segment my cold email list\", or \"who buys recruitment services from us\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Recruitment ICP builder

You decide who a recruitment agency should cold email, and write it so a list tool can find exactly those people. A vague ICP ("tech companies that hire") produces a list nobody answers. A sharp one names the company, the person, the reason they would hire now, and who to leave out.

If `references/agency-profile.md` exists, read it first: specialties, markets, industries, proof points. If the recruiter already ran outreach-target-profile from the Recruiter Outreach Pack, start from its result instead of asking again.

## Start from evidence, not hope

Ask for the agency's last 10 to 20 placements or best clients (company, role, size, who hired, how the deal started). If there are none, ask which roles the desk fills best and why. Build the ICP from what the desk has already won. Say plainly when a segment has no proof behind it.

## The ICP, in six parts

1. **Company.** Industry, headcount band, location or time zone, funding or ownership type. Name the bands as filter values, for example "51 to 500 staff", not "growing companies". Treat signals like "recently funded" as a priority order, not a hard filter, or the list shrinks to nothing.
2. **The hire.** The role families this desk fills and their level. A desk that fills controls engineers should not prospect companies that only hire nurses.
3. **Triggers that mean "hiring now".** Pick the two or three the desk can find and prove: a matching job posted 30+ days or reposted, several openings in one team, new funding, a new site or contract, a new leader in the function, a competitor's layoffs (talent is available), the company posting its own recruiter role, a project or contract win, a shutdown or outage season (contract demand), a perm role open 60+ days.
4. **The person.** Who feels the pain and can say yes. Usually the hiring manager for the function first (for example VP Engineering, Plant Manager, Head of Finance), because the person who feels the empty seat often replies faster than a talent generalist; then the head of talent or HR; the founder only at companies under about 50 staff. List title families, not one title (Head of Talent, Director of Recruiting, VP People). Give 3 to 6 exact titles plus their seniority, and say who **not** to email (junior HR coordinators, procurement unless the deal is a PSL).
5. **Fit signals.** Anything that makes the agency's offer stronger, such as no internal recruiter, a role type internal teams struggle with, or a location the desk knows.
6. **Exclusions.** Current clients and their subsidiaries (unless the recruiter says otherwise), companies on off-limits or no-poach terms in the agency's contracts, the do-not-contact list, competitors of key clients if the agency has promised not to work for them, anyone who opted out before, and other staffing agencies, RPOs and recruitment consultancies (data tools return them for recruiting keywords).

## Turn it into segments

Split the ICP into segments small enough to write one message for: one role family, one trigger, one buyer title. A segment of 100 to 500 people is easier to write for and to judge than one of 5,000. Name each segment, for example `ohio-manufacturers-controls-jobs-30d`.

For each segment write the filter set a tool can run:

```
Segment: [name]
Company filters: industry [..], headcount [..], location [..]
Trigger: [what, where to find it, how old it may be]
Titles: [exact titles], seniority [..]
Exclude: [domains, lists, titles]
Estimated size: [ask the recruiter to run the count]
Why they would reply: [one line in the buyer's words]
```

## Rules

- Companies are chosen on business facts. Never select or exclude people by age, gender, ethnicity, religion, disability or any other protected trait, and never by guessing them from names or photos.
- Do not invent company counts or market sizes; ask the recruiter to run the filter and report the number.
- Say which segment to start with and why: the one with the most proof and the clearest trigger.
- Hand the segments to recruitment-offer-builder next, then lead-list-builder.
