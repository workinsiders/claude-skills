---
name: outreach-message-check
description: Checks a drafted outreach message before it goes out, flags only, no rewrite unless asked: is the reason specific and true, is every fact sourced, does it read as a pitch, is there one clear ask, does it match the recruiter's voice, and does it carry the opt out and address lines commercial email needs. Use when a recruiter says "check this email", "is this spammy", "review my InMail", "before I send", or pastes a draft.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: recruiter-outreach-pack
---

# Outreach message check

A second read before sending catches the line that loses the reply. You check a draft and point at problems; the recruiter decides what to change.

If `references/agency-profile.md` exists, read the words the agency never uses, the mailing address, and the rule on naming the client.

## Input

- The draft message and its channel (email, InMail, connection note, text).
- The facts or signal it is built on, if the recruiter has them.
- The voice guide, if there is one.

## The checks, in order

1. **Reason.** Does the first line give a specific, true reason this person, now? Could it be sent unchanged to anyone else?
2. **Facts.** Is every claim about the company, person, pay or placements traceable to a source or the agency profile? List any that are not.
3. **Pitch.** Is the message about the reader, or about the agency? Count sentences about "we".
4. **Ask.** Exactly one, low effort, easy to say no to.
5. **Voice and length.** Matches the voice guide, under the channel limit (email under 120 words, InMail 400 to 600 characters, connection note 300, text 300), no AI tells.
6. **Rules.** For US commercial email: a working opt out and the sender's real postal address, and a subject line that is not misleading. For candidates: client confidentiality followed, no protected-trait references. Flag questions about other countries' rules for the recruiter's adviser.

## Output

```
MESSAGE CHECK | [channel] | [date]
1. Reason: pass / flag: "[line]" ([why])
2. Facts: pass / flag: [unsourced claims]
3. Pitch: pass / flag
4. Ask: pass / flag
5. Voice and length: pass / flag ([n] words)
6. Rules: pass / flag / question for adviser
Send as is? yes / fix [n] flags first
```

## Rules

- Flags only. Quote the exact line. Rewrite only if the recruiter asks, and then change as little as possible.
- Never approve a message that contains an unsourced fact about a person, pay or a placement.
- This is a check, not legal advice.
