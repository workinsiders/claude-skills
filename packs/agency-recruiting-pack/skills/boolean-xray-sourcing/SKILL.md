---
name: boolean-xray-sourcing
description: Builds Boolean and Google X-ray search strings for finding candidates on LinkedIn, Google, GitHub, job board resume databases and an agency's own ATS. Use when a recruiter asks for a Boolean string, an X-ray search, "find me candidates for", "sourcing strings", or pastes a job order and wants a search plan.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: agency-recruiting-pack
---

# Boolean and X-ray sourcing

You build search strings a recruiter can paste and run. Every string must work on the platform it is written for, so check the platform rules below before you write it.

If `references/agency-profile.md` exists, read it for the agency's ATS and target markets.

## Step 1: get the inputs

From the job order or the recruiter's message, pull:
- Job titles, including the old and odd ones people really use (e.g. "Controls Engineer", "PLC Programmer", "Automation Engineer").
- Two to four must have skills or tools.
- Location: city plus nearby cities within commute, or "remote, US".
- Exclusions: wrong seniority, wrong industry, recruiters and staffing profiles.

If titles or skills are missing, ask once. Otherwise go.

## Step 2: build the synonym groups

Write each group as an OR list in parentheses. Keep groups to 8 terms or fewer, because long strings break on most platforms.

- Titles: `("controls engineer" OR "automation engineer" OR "plc programmer")`
- Skills: `(Allen-Bradley OR Rockwell OR Siemens OR "TIA Portal")`
- Location: `(Atlanta OR Marietta OR Alpharetta OR Kennesaw)`

## Step 3: write one string per platform

### LinkedIn (Recruiter, Sales Navigator or basic search)
- Operators AND, OR, NOT must be in capitals. Use quotes for phrases and parentheses for groups.
- No wildcards (`*`). No `site:` operator.
- Put titles in the title field and skills in the keyword field when the platform has separate fields. Say which string goes in which field.

### Google X-ray (LinkedIn public profiles)
- Start with `site:linkedin.com/in/`.
- Use `-` to exclude, not NOT. Example: `-recruiter -staffing -jobs`.
- Google ignores very long queries. Stay under about 32 words.
- Location: add the city name in quotes, plus the metro name.

### Google X-ray (GitHub and other sites)
- GitHub people: `site:github.com "followers" "location" + language or tool`.
- Resumes posted online: `(intitle:resume OR inurl:resume) -template -sample -jobs`.
- Conference speaker lists and association member directories for niche roles.

### Job board resume databases (Indeed, Dice, Monster, ZipRecruiter)
- Most support AND, OR, NOT, quotes and parentheses. Dice supports `title:` in some views; note it as "if your Dice view supports field search".
- Add a "last active" filter recommendation (30 or 60 days) rather than putting dates in the string.

### Agency ATS (Bullhorn, PCRecruiter, Loxo, Crelate, JobAdder and others)
- Your own database is the cheapest source. Always include an ATS string.
- Field names and operator support vary by ATS. Write a plain AND/OR/NOT string and tell the recruiter to check whether their ATS treats a space as AND.
- Suggest searching past candidates who reached interview or offer stage for similar roles first.

## Step 4: give a search plan

Output in this order:

1. **Start here** (the narrowest string, highest hit rate).
2. **Widen** (drop one skill or add adjacent titles).
3. **Different angle** (adjacent industry, competitor company names, or certifications).
4. **ATS string.**
5. **What to check in the results** (three quick signs a profile is a real fit).

Label every string with the platform and field it goes in. Put each string in its own code block so it copies cleanly.

## Rules

- Never write strings that target or exclude people by age, gender, race, religion, nationality, disability or any other protected trait, even indirectly (graduation years used to guess age, names used to guess ethnicity). If asked, decline that part and explain why in one line.
- Do not suggest scraping tools, fake profiles or anything that breaks a platform's terms. Manual searching and the platform's own features only.
- Do not claim how many results a string will return. You cannot run it.
- If a string is getting too long for its platform, split it into two searches instead of cutting terms silently.
