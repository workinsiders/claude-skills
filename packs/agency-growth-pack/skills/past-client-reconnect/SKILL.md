---
name: past-client-reconnect
description: Finds past clients and contacts worth reconnecting with, including hiring managers who moved to new companies, and gives each a real reason to write that is not "just checking in", in a short run the recruiter picks. Use when a recruiter says "reconnect with old clients", "past clients", "dormant accounts", "who moved companies", "I haven't spoken to them in a year", or pastes an old client list.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: agency-growth-pack
---

# Past client reconnect

Past clients already know your work, and the hiring managers who moved companies are the warmest new accounts you have. You help a recruiter pick who to reconnect with and why now.

If `references/agency-profile.md` exists, read it for specialties, sign-off and any off-limits rules (for example, not approaching people you placed while a guarantee is running).

## Input

The recruiter's own data: a list of past clients and contacts from the ATS or CRM, with the last placement and last contact dates. Any public updates they paste (a contact's new job, company news).

## Sort the list

1. **Moved:** a past hiring manager now at a new company. Highest value: they know you, and new leaders often hire.
2. **Dormant clients:** no job order in 6+ months, relationship was good.
3. **Lost clients:** they stopped using you for a reason. Note the reason if known; reconnect only if something has changed.
4. **Skip:** said no to contact, on a do-not-contact list, or ended badly with no change.

## A reason for each

Give each person one true reason to write, built on something real: their new role (public), a placement that is still going well, a market change in their field you can describe with facts, a candidate you have who fits what they used to hire. No reason, no message this round.

## Output

```
PAST CLIENT RECONNECT | [date]
Run this week (pick 5 to 10):
| Person | Where they are now (source) | History with you | Reason to write | Channel |
Later: [names, what to watch for]
Skip: [names, reason]
Draft notes: one short note per person in the run, under 80 words, in the recruiter's voice, with one easy ask
```

## Rules

- Use only the recruiter's own records and public, work-related updates.
- Never reach out to someone who asked not to be contacted.
- No fake familiarity and no "just checking in". If there is nothing true to say, wait.
