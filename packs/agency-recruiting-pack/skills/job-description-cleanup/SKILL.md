---
name: job-description-cleanup
description: Rewrites a client's job description into a job post candidates will read and apply to, with honest requirements, pay transparency where the law requires it, and inclusive wording. Use when a recruiter pastes a job description and asks to "clean up", "rewrite", "make this post better", "write a job ad", "turn this req into a posting", or check a post for biased or risky language.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: agency-recruiting-pack
---

# Job description cleanup

Clients hand agencies long, internal job descriptions full of duties nobody reads. You turn them into a post that sells the role and screens honestly.

If `references/agency-profile.md` exists, read it for how the agency posts (confidential client or named, where it posts, EEO line, apply instructions).

## Inputs

- The client job description or job order.
- Pay range and work location (city, hybrid days, or remote). If missing, ask; see the pay rules below.
- Whether the client name can appear.

## Output: the post

```
[Job title]: plain, searchable, no internal codes ("Senior Mechanical Engineer", not "ME III - Grade 7")
[City, State] | [On site / Hybrid n days / Remote (US)] | [Direct hire / Contract n months / Contract to hire]
Pay: [$min to $max per year or per hour] [+ bonus or other pay if known]

What you'll do
- 4 to 6 bullets, outcomes first ("Design fixtures for a new EV battery line"), not duty lists.

What you need
- 3 to 5 true requirements.

Nice to have
- 2 to 4 items.

Why this role
- 3 bullets: the real reasons someone would move (team, project, schedule, growth, benefits).

How to apply
- [Agency apply instructions]

[EEO statement from agency profile]
```

Target 250 to 400 words.

## What to fix

- **Requirement inflation.** Move anything the client called "required" but said was trainable or a preference into Nice to have. Flag every requirement you moved.
- **Years of experience.** Replace "10+ years" with the skill it stands for where you can ("has led a full design cycle from concept to production"). Keep a years figure only if the client insists.
- **Degree requirements.** If the work does not need a specific degree, suggest "or equivalent experience" and flag it.
- **Exclusionary wording.** Replace words like "rockstar", "ninja", "young", "energetic", "digital native", "native English speaker", "recent graduate" (unless it is a graduate program), and physical requirements that the job does not truly need. Keep real physical requirements but state them as the task ("lifts 40 lb parts several times a shift").
- **Internal jargon.** Spell out acronyms on first use unless candidates in the field all know them.

## Pay transparency

A growing number of US states and cities require a pay range in the posting itself (for example California, Colorado, New York and Washington), each with its own size thresholds and rules. Laws change, so:
- If the role is in, or open to remote workers in, a place with a posting law and there is no range, stop and tell the recruiter the post likely needs one before it goes up.
- Never invent a range.
- Say "check current rules for [state]" rather than giving legal advice.

## Rules

- Do not add duties, perks or benefits the client did not mention.
- Keep the client's name out if the agency profile or the recruiter says the search is confidential. Describe the company instead.
- After the post, list every change that a client might push back on (moved requirements, removed wording, missing pay range) so the recruiter can clear them with the client.
