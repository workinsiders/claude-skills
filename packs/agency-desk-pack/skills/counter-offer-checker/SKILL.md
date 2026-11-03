---
name: counter-offer-checker
description: Scores a candidate's counter-offer and fall-off risk before you submit them, then writes the questions and talk track to deal with it before the offer, plus resignation prep. Use when a recruiter asks "will they take a counter", "check counter-offer risk", "resignation prep", pastes screening notes for a candidate about to be submitted, or a candidate is about to resign.
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: agency-desk-pack
---

# Counter-offer checker

Most agency fall-offs are decided long before the offer: the candidate never had a real reason to leave, or their employer had an easy way to keep them. Your job: spot that early, while there is still time to deal with it or stop.

If `references/agency-profile.md` exists, read the guarantee period. A fall-off inside the guarantee costs the agency a refund or a free replacement, so say so when the risk is high.

## Input

- Screening notes or a call transcript.
- Current pay and the role's pay, if known.
- Anything about the current employer: a recent raise, a promised promotion, the manager, workload.

## Step 1: score the risk

Score each factor 0 (low risk), 1 or 2 (high risk). Use only what the notes say. If the notes do not cover a factor, mark it `ASK` and score it 1.

| Factor | 0 | 1 | 2 |
|---|---|---|---|
| Reason to leave | Specific, about the work or growth, said unprompted | General ("ready for a change") | Only money, or no clear reason |
| Pay jump | Under 10% | 10 to 20% | Over 20%, or money is the main reason |
| Who started it | Candidate was already looking | Open after one call | Recruited cold, not looking at all |
| Current employer | Has tried to fix it and failed, or cannot fix it | Unknown | Has matched offers before, or is "talking about" a promotion |
| Other activity | No other processes | One other process | Several offers or late-stage interviews |
| Decision talked through | Candidate says they have discussed it with anyone who has a say | Not discussed yet | Candidate says someone with a say is against it |
| Tenure | 2 to 5 years | Under 1 year, or 6 to 10 | Over 10 years in one place |
| How they talk about resigning | Has thought it through, has a date in mind | Unsure | Nervous, avoids the topic, "I'll see what they say" |

Total out of 16:

- **0 to 5, low:** submit. Do resignation prep before the offer.
- **6 to 10, medium:** submit, and run the counter-offer conversation below before the second interview.
- **11 to 16, high:** tell the recruiter plainly. Hold the submittal until the candidate has a reason to move that is not money, or write down why you are submitting anyway.

## Step 2: questions to close the gaps

Write a question for every `ASK` and every 2. Keep them natural, for example:

- "If your manager matched this number tomorrow, what would still bother you about staying?"
- "When did you first start thinking about leaving? What happened that week?"
- "Who else has a say in this move, and where are they on it?"
- "How has your company reacted when other people resigned?"

## Step 3: the counter-offer conversation

Draft five to seven lines for the recruiter's phone call. A talk track, not a script to read. It should:

1. Ask the candidate to predict the counter: "What do you think they'll do when you resign?"
2. Have them say in their own words why more money would not fix their reasons.
3. Agree that if a counter comes, they call the recruiter before they answer.
4. Never run down the current employer, and never quote made-up statistics about counter-offers.

## Step 4: resignation prep, once an offer is close

- A short resignation letter the candidate can edit: thanks, last day, an offer to help with handover. Nothing about the new job or the reason.
- Advice: resign in person or on video, hand over the letter, keep it brief, do not negotiate in the meeting.
- A check-in plan: the recruiter calls the evening of the resignation, then weekly until the start date.

## Output

```
COUNTER-OFFER CHECK: [Candidate] for [Role]
Score: [n]/16 -> Low / Medium / High
Biggest risks: [top two factors, with the evidence]
Ask before submitting: [questions]
Talk track: [five to seven lines]
Recommendation: Submit / Submit after the call / Hold
```

## Rules

- Base every score on the notes. Never guess about someone's personal life.
- Never score on family status, age, health or other protected traits, even if the notes mention them.
- The candidate decides. The aim is an honest decision early, not pressure.
