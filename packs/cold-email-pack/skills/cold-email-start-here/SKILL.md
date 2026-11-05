---
name: cold-email-start-here
description: "Runs a staffing or recruitment agency's cold email campaign from zero to a launch-ready draft, one stage at a time, handing each stage to the right skill in the Cold Email Pack and keeping a campaign brief so the work can resume later. Use when a recruiter or agency owner says \"set up cold email\", \"start a cold email campaign\", \"new to cold email\", \"cold email for my recruitment agency\", \"BD campaign from scratch\", \"where do I start with cold email\", or \"resume my campaign\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Cold email: start here

You run one cold email campaign for a recruitment agency in the right order. You do not do every stage yourself. Each stage belongs to one skill in this pack; you open it, hand it what it needs and move on only when its output exists and the recruiter has approved it.

Most agency cold email fails for reasons that come before the copy: the wrong domain, an unverified list, no real offer, or a list of companies with no reason to hire now. The order below fixes those first.

If `references/agency-profile.md` exists, read it first, especially the Cold email lines. Never invent fees, proof points, sender names or domains.

## Step 0: new or resume

Ask whether a campaign brief already exists. If the recruiter pastes one, find the first stage not marked done and continue there. If not, ask for:

1. A campaign name (for example `controls-engineers-ohio-q1`).
2. Who the campaign is for: **clients** (selling recruitment services, the default) or **candidates** (job opportunities).
3. The sequencer they use, or "none yet".

## The stages

| # | Stage | Skill | Done when |
|---|---|---|---|
| 1 | Who to email | recruitment-icp-builder | One written ICP with titles, triggers and exclusions |
| 2 | What to offer | recruitment-offer-builder | One offer and up to three angles the recruiter approved |
| 3 | Sending setup | sending-setup-plan | Domains, mailboxes and warmup start date written down |
| 4 | The list | lead-list-builder | A list file with the agreed columns and a signal per row |
| 5 | Verification | list-verification-gate | Bounce risk under the gate, suppressions removed |
| 6 | The emails | bd-cold-email-sequence or mpc-email-campaign (clients), candidate-cold-email-sequence or candidate-database-campaign (candidates) | Sequence approved |
| 7 | Variants | email-variants-spintax | Variants and merge fields checked |
| 8 | Test plan | ab-test-plan | One variable to test, with the stop rule |
| 9 | Legal check | cold-email-compliance-check | Every flag answered or sent to the adviser |
| 10 | Launch gates | campaign-launch-checklist | Every gate passed; campaign saved as paused |

After launch: cold-email-reply-handler daily, campaign-results-review weekly, deliverability-check if replies drop.

If a skill is not installed, do that stage inline using the same rules and say which skill would do it better.

## How to run each stage

1. Say which stage you are on and why it comes now, in one sentence.
2. Hand the skill only what it needs from the brief.
3. Show the result and ask the recruiter to approve or change it. Never mark a stage done without a yes.
4. Update the campaign brief and show it.

Stages 3 and 4 can overlap: new mailboxes need two to four weeks of warmup, so the copy can be written while they warm. Build the list in the last week of warmup, or re-check every signal and re-verify if more than 14 days pass before launch, because hiring signals go stale fast. Say so when stage 3 is done.

## The campaign brief

Keep this block up to date and give it back at the end of every turn so the recruiter can paste it into a new chat:

```
CAMPAIGN BRIEF: [name]
Audience: clients | candidates
Sequencer: [name]
Stage status: 1 [done/open] ... 10 [done/open]
ICP: [one line]
Offer: [one line]   Angles: [a] [b] [c]
Domains / mailboxes: [list]   Warmup started: [date]   Earliest launch: [date]
List: [file name], [rows] rows, verified [date], bounce estimate [x]%
Sequence: [n] emails, approved [date]
Test: [variable], [contacts per variant]
Legal flags open: [list or none]
Next action: [one line, who, by when]
```

## Rules

- Nothing is sent or launched by you. If a sequencer connector (for example Instantly's) is connected and the recruiter asks, you may create the campaign as a **paused** draft. You never activate it.
- Never skip the verification gate or the legal check to save time.
- Never use the agency's main website domain for cold email.
- Candidates are never marketed to clients without the candidate's permission.
- No invented reply rates or results. Use the recruiter's own numbers once the campaign runs.
- Legal questions go to the recruiter's adviser; you list them, you do not answer them.
