---
name: candidate-submittal
description: Writes the candidate submittal an agency recruiter sends to a client hiring manager, matched against the job order, plus a blind (anonymized) profile when needed. Use when a recruiter says "write a submittal", "submit this candidate", "candidate summary for the client", "blind profile", "why this candidate", or pastes a resume and screening notes with a job order.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: agency-recruiting-pack
---

# Candidate submittal

A submittal is the agency's pitch to the hiring manager. Managers read the first few lines and decide. Your job is to make those lines answer "why this person, for this job, now" with facts from the resume and the recruiter's screen.

If `references/agency-profile.md` exists, read it for the agency's submittal rules (for example "always include the candidate's pay expectation" or "blind profiles only for new clients").

## Inputs

- The job order (or at least the must haves, pay range, location and interview steps).
- The resume.
- The recruiter's screening notes: motivation, pay expectation, notice period, availability, location and work authorization as the candidate stated it, other interviews in play.

If screening notes are missing, ask for: why they would move, pay expectation, notice period, and availability to interview. Do not send a submittal without pay expectation unless the recruiter says to.

## Output: the submittal

```
Subject: [Candidate first name] for [Job title] - [one-line hook]

[First name] is a [current title] at [company type or name] with [n] years in [core area]. [One sentence on why they fit this search.]

Why they fit
- [Must have 1]: [evidence from resume or screen, with a number if there is one]
- [Must have 2]: [evidence]
- [Must have 3]: [evidence]

Gaps and how they cover them
- [Gap]: [honest note, or what they said about it]

The details
- Pay expectation: [ ]
- Notice / start: [ ]
- Location / work setup: [ ]
- Work authorization: [as the candidate stated it]
- Why they would move: [their words, short]
- Other activity: [interviewing elsewhere? offers pending?]

Available to interview: [days/times]
```

Keep it under 200 words above "The details". Put the strongest proof first.

## Blind profile

When the recruiter asks for a blind profile, remove: name, current and past employer names (replace with a description like "Tier 1 automotive supplier, 2,000 staff"), school names if they identify the person, email, phone, street address, and LinkedIn URL. Keep city or metro, titles, years, skills and achievements. Label the top `BLIND PROFILE: [Title] candidate, [Metro]`.

## Rules

- Only use facts from the resume or the recruiter's notes. If something is not there, leave it out or mark it `ask candidate`.
- Never include age, date of birth, marital status, children, religion, health, photos, or anything else the client must not use to decide. If the notes contain these, drop them and tell the recruiter you did.
- Show gaps. A submittal that hides a missing must have loses the client's trust when the interview finds it.
- Never exaggerate titles, years or results. "Led" only if the resume says led.
- Do not add the agency fee to a submittal unless the agency profile says to.
