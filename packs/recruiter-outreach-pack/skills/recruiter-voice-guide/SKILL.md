---
name: recruiter-voice-guide
description: Builds a short voice guide from a recruiter's own past messages so every draft sounds like them, not like a template: how they open, ask and sign off, words they use and never use, and a checklist of AI tells to strip out. Use when a recruiter says "make it sound like me", "this sounds like ChatGPT", "my voice", "writing style", or before drafting any outreach run.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Recruiter voice guide

Hiring managers and candidates can spot a pasted chatbot message in one line. You help a recruiter capture how they really write, so every draft starts in their voice.

If `references/agency-profile.md` exists, read the "Words we never use" list and the sign-off details.

## Input

Five to ten messages the recruiter wrote themselves and was happy with: BD emails, InMails, texts, replies. Real ones, not templates. Remove names and contact details first.

## Read for

- **Openings:** do they lead with the reason, a name, a question?
- **Length:** typical sentences per message, sentence length.
- **The ask:** how they ask for a call or a reply.
- **Sign-off:** exactly how they end.
- **Words they use** often, and words they never use.
- **Tone:** formal or casual, contractions, humour, how direct.

## The AI-tell checklist

Flag and remove in any draft:
- Openers like "I hope this finds you well", "I came across your profile", "I wanted to reach out".
- Words like "delve", "leverage", "exciting opportunity", "game-changer", "synergy", "rockstar", "ninja".
- Three-part lists everywhere, em dashes everywhere, every paragraph the same length.
- Flattery not tied to a real fact.
- A closing line that asks two things.

## Output

```
VOICE GUIDE: [recruiter name] | built from [n] messages | [date]
How I open: [ ]
How long: [ ]
How I ask: [ ]
How I sign off: [ ]
Words I use: [ ]
Words I never use: [ ]
Tone in one line: [ ]
AI tells to strip: [checklist]
Before and after: [one generic sentence rewritten in this voice]
```

Keep it under one page so it can sit at the top of every drafting request.

## Rules

- Build it only from the recruiter's own messages. Do not imitate a named person or another recruiter.
- If fewer than five samples are given, say the guide is a first draft and list what to add.
