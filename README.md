# Claude skills for recruiters

Free, MIT-licensed Claude skills for staffing agencies and in-house recruiting teams, from [Work Insiders](https://workinsiders.com/skills/). 25 SKILL.md files in three packs. They also work in ChatGPT, Gemini and Grok.

| Pack | For | Skills | Page |
|---|---|---|---|
| [Agency Recruiting Pack](packs/agency-recruiting-pack) | Staffing agencies | 6: job order intake, Boolean sourcing, candidate outreach, submittals, BD emails, job posts | [workinsiders.com/skills/agency-recruiting-pack/](https://workinsiders.com/skills/agency-recruiting-pack/) |
| [Agency Desk Pack](packs/agency-desk-pack) | Staffing agencies | 7: market maps, calibration, candidate replies, screening calls, counter-offers, offer pre-close, post-mortems | [workinsiders.com/skills/agency-desk-pack/](https://workinsiders.com/skills/agency-desk-pack/) |
| [In-House Recruiting Pack](packs/in-house-recruiting-pack) | Corporate and startup TA teams | 12: scorecard to signed offer, plus an AI hiring policy | [workinsiders.com/skills/in-house-recruiting-pack/](https://workinsiders.com/skills/in-house-recruiting-pack/) |

## The rule every skill follows

The AI drafts. People decide. No skill screens, ranks or scores a candidate, nothing is sent for you, and legal points are flagged for your adviser instead of answered.

## Install in Claude Code

```
/plugin marketplace add workinsiders/claude-skills
/plugin install agency-recruiting-pack@workinsiders-skills
/plugin install agency-desk-pack@workinsiders-skills
/plugin install in-house-recruiting-pack@workinsiders-skills
```

Install only the packs you need.

## Install in Claude.ai, ChatGPT, Gemini or Grok

Download a pack ZIP from its page on [workinsiders.com/skills/](https://workinsiders.com/skills/). Each ZIP holds one ZIP per skill, ready to upload under Customize, Skills in Claude, Plugins, Skills in ChatGPT Business, or Skills in Gemini Enterprise. For a Gemini Gem, a GPT or Grok Bot, paste the SKILL.md text into its instructions. Step-by-step instructions for every app are on each pack page.

## Fill in your profile first

Every skill reads one profile file in its `references/` folder:

- Agency packs: [`agency-profile.md`](profiles/agency-profile.md) (fees, markets, proof points, house rules)
- In-House pack: [`company-profile.md`](profiles/company-profile.md) (stages, pay policy, who decides)

Fill it in once and every output uses your real details. Leave a line blank rather than guess, so the AI never invents fees, pay or proof points.

## Layout

```
.claude-plugin/marketplace.json     Claude Code marketplace
packs/<pack>/.claude-plugin/        plugin manifest
packs/<pack>/skills/<skill>/        SKILL.md + references/<profile>.md
profiles/                           the blank profile files
```

## More

- [Skills Directory](https://workinsiders.com/skills/): these packs plus third-party recruiting skills we read and graded
- [MCP Directory](https://workinsiders.com/mcp-servers/): recruiting tools you can connect to Claude
- Suggest a skill or report a problem: [open an issue](https://github.com/workinsiders/claude-skills/issues)

MIT licensed. These are drafts and checklists for people to use, not legal advice.
