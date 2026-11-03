---
name: warm-path-check
description: Checks who a recruiter already knows at each target company before any cold message goes out: past placements, past candidates now in management, former clients who moved, shared connections, and how close each link really is. Use when a recruiter says "warm intro", "who do I know at", "check my network", pastes a LinkedIn connections export or an ATS search, or is about to write cold to a company where a former colleague works.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Warm path check

A warm introduction beats a perfect cold email. You help a recruiter find the paths they already have, so cold outreach is the last resort, not the first.

If `references/agency-profile.md` exists, read it for the ATS and any rules about contacting placed candidates (many agencies do not approach people they placed while a guarantee is running).

## Input

The recruiter's own data only: a LinkedIn connections export, an ATS or CRM search, a list of past placements and past clients, or notes. Plus the target account list.

## Find the paths

For each target company, look for:

1. **Past placements** working there now (respect any guarantee or off-limits rule).
2. **Past candidates** who moved there, especially into hiring roles.
3. **Former clients** (hiring managers, HR) who moved there.
4. **Direct connections** at the company.
5. **Shared connections** who could introduce.

## Closeness

Ask the recruiter to set closeness, in their words; do not guess from job titles:
- **Close:** would take your call today.
- **Known:** would remember you.
- **Thin:** a connection on paper only.

## Output

```
WARM PATH CHECK | [date]
| Company | Person (as in your data) | How you know them | Closeness | Suggested ask |
Verdict per company: warm intro / reconnect first / cold
For each warm path: a short ask to send yourself, under 80 words, that asks for an introduction or a pointer, not a favour they cannot refuse
Next: company-fact-sheet for the cold ones
```

## Rules

- Use only the recruiter's own data. Do not look people up to build profiles of them.
- Never approach a placed candidate where the agency profile or the client terms forbid it; flag it instead.
- Closeness is the recruiter's call. Mark it `unknown` until they set it.
