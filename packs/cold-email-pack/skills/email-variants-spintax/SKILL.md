---
name: email-variants-spintax
description: "Turns an approved recruitment cold email into safe variants and spintax for the agency's sequencer, so hundreds of sends are not identical, while keeping the meaning, the facts and the merge fields intact; also checks the syntax before it goes in. Use when a recruiter asks \"add spintax\", \"write variants of this email\", \"make my emails less repetitive\", \"Instantly spintax\", \"RANDOM syntax\", or \"check my merge tags\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Email variants and spintax

Sending the same 80 words to 400 people is a pattern filters notice. Variation spreads that out. You add it without changing what the email says, so every reader still gets the approved message.

If `references/agency-profile.md` exists, read the Cold email lines: sequencer and words never used.

## Two kinds of variation, used for different jobs

1. **Spintax (for deliverability):** small swaps inside one email, so each send differs a little. Greetings, connecting phrases, the ask's wording, sign-off. Same meaning every time.
2. **Variants (for testing):** whole different versions of a line or email, for example two subject lines or two angles, split evenly so the recruiter can learn which works. Plan these with ab-test-plan.

Never use spintax to test. Never use variants to dodge filters.

## Syntax by sequencer

Ask which sequencer they use and use only its syntax:
- **Instantly:** `{{RANDOM | Hi | Hey | Hello}}`
- **EmailBison:** `{Hi|Hey|Hello}`
- **Any other tool:** ask the recruiter to paste one line from that tool's help page showing its spintax and merge-field format, then follow it exactly. Do not guess.

Merge fields stay in the tool's own format (for example `{{firstName}}` in Instantly). Never put a merge field inside a spintax option unless the tool's help says it works.

## What to spin

- Greeting: 3 options.
- The bridge words between sentences: 2 or 3 options each.
- The ask: 2 or 3 wordings with the same request ("Want the profiles?" / "Should I send the profiles?" / "Happy for me to send the profiles?").
- Sign-off: 2 options.
- The opt-out line: 2 options with the same meaning.

## What never to spin

- The signal, the proof point, any number, the offer, company or role names.
- Reply words the reader is asked to type: reply "yes" stays "yes".
- The legal lines (mailing address, opt-out meaning).
- Anything that changes tone to pushy or casual beyond the approved version.

Start light at launch: the ask, the sign-off and the opt-out line. Spin the body more once a version has passed about 2,000 sends. No nesting (spintax inside spintax). Keep options about the same length; one bad option in a set of five ships broken in a fifth of sends. Spintax will not rescue a tired email; a falling reply rate needs a new angle. Every combination must read like a normal email; read three random combinations aloud before handing it over.

## Syntax check before it goes in

Check every email for:
- Matched braces, no stray `|`, no empty option.
- Every merge field spelled exactly as the list column, and no custom field named the same as a built-in one (for example a custom `COMPANY` in EmailBison).
- No spintax inside the subject line unless the tool supports it.
- A piped token is never used as a fallback: in EmailBison `{a|b}` is spintax, so `{personalization|there}` would send the literal word to half the list.

Then print three filled-in samples with real-looking values so the recruiter can read what readers will get.

## Output

The email with spintax in the right syntax, the list of spun spots, the three samples, and a pass on the syntax check. If the recruiter wants test variants too, hand to ab-test-plan.

## Rules

- Variation never adds a claim, a number or an urgency the approved email did not have.
- Keep each option as short as the original. Spintax that doubles the length defeats the email.
