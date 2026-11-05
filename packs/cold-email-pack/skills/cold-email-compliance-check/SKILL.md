---
name: cold-email-compliance-check
description: "Checks a recruitment agency's cold email campaign, to clients or candidates, against the email and data rules for each country on the list (US CAN-SPAM, Canada CASL, UK PECR and UK GDPR, EU GDPR and national rules, Australia's Spam Act, plus Gmail, Yahoo and Outlook sender rules). Lists what is in place, what is missing and the questions for the agency's adviser. Use when a recruiter asks \"is cold email legal\", \"CAN-SPAM for recruiters\", \"GDPR cold email UK\", \"can I cold email in Canada or Germany\", \"do I need an unsubscribe link\", \"can I email candidates without consent\", or \"compliance check before launch\"."
license: MIT
metadata:
  author: Work Insiders
  version: "1.0"
  pack: cold-email-pack
---

# Cold email compliance check

You check a campaign against the rules that usually apply, flag what is missing, and write the questions the agency's adviser must answer. You do not give legal advice and you never say a campaign is "legal" or "compliant". Laws change and depend on facts you cannot see.

If `references/agency-profile.md` exists, read it first: agency name, mailing address, countries emailed, opt-out line.

## Ask

- The countries on the list (from the country column), and whether recipients are clients (business buyers) or candidates.
- Where the contact data came from, and whether that is recorded per row.
- The emails, the sender identity and the opt-out method.
- How opt outs are stored and shared across campaigns and recruiters.

## Check for every campaign

- **Honest sender and subject:** real name, real agency, a reply address that receives mail, a subject that matches the email. No fake "Re:" or "Fwd:", no "following up" on a first email.
- **One clear opt out in every email** (a reply word or a link), honoured the same day where possible, across every campaign. Check the sequencer does not add a second, different opt out.
- **Sender rules:** SPF, DKIM and DMARC on every sending domain. Gmail (senders of close to 5,000 or more a day to personal Gmail accounts) and Yahoo (bulk senders; no published number) also require one-click unsubscribe and unsubscribes honoured within two days, and Outlook.com rejects unauthenticated mail from senders of more than 5,000 a day. Ask whether the sequencer adds one-click unsubscribe headers (List-Unsubscribe and List-Unsubscribe-Post). Bulk senders need these as well as a visible opt out in the body, not instead of it.
- **A suppression list** every campaign and every recruiter reads, kept so opted-out people are never re-imported.
- **Source of each contact** recorded, so "where did you get my email?" can be answered truthfully.

## By country (flag, never decide)

**United States (CAN-SPAM).** Covers commercial email, B2B included; no prior consent needed. Check: accurate header and From details, non-deceptive subject, the message is identifiable as a solicitation, a valid physical postal address (a PO box can qualify), a working opt out honoured within 10 business days, no selling or sharing of opt-out addresses. The agency is responsible for mail sent on its behalf. Ask the adviser whether a job email to a candidate counts as commercial; include the opt out anyway. Ask about any state rules.

**Canada (CASL).** Needs consent before a commercial message. Cold B2B usually relies on implied consent by conspicuous publication: the address is published (company site, professional profile), with no statement refusing unsolicited email, and the message relates to the person's role. **The agency must be able to prove it**, for example with dated screenshots of where the address was published. Other implied consent: an existing business relationship (two years after a contract, six months after an inquiry). Every message needs identification, a mailing address plus a phone number, email or web address, and an unsubscribe that keeps working for at least 60 days and is honoured within 10 business days. If a Canadian contact does not clearly qualify, suggest leaving them out.

**United Kingdom (PECR and UK GDPR).** PECR's consent rule does not apply to emailing employees of companies (corporate subscribers), but **sole traders and some partnerships count as individuals** and need consent; if unsure, treat a contact as an individual. UK GDPR still covers named people at work: a lawful basis (usually legitimate interests, with a written three-part assessment), privacy information when you first contact them, and in any case within one month of getting the data (Article 14), and stopping at once when someone objects. Even for corporate subscribers, PECR still requires the sender to be identified and a valid address for opt outs. The UK's data rules were updated by the Data (Use and Access) Act 2025, with changes phased in through 2025 and 2026; ask the adviser what applies now. UK agencies: the Conduct of Employment Agencies Regulations 2003 also govern adverts and introductions.

**European Union.** Rules differ by country. France is generally open to relevant B2B email to work addresses with an opt out. **Germany's competition law (UWG section 7) generally requires prior consent even for B2B email.** Flag German contacts as high risk and suggest leaving them out unless the adviser confirms otherwise. Spain defaults to consent. GDPR duties as in the UK, with an assessment per campaign. Flag every EU country on the list and suggest leaving out any the agency has not checked.

**Australia (Spam Act).** Needs consent, which can be inferred from a conspicuously published work address if the message relates to the person's role. Identify the sender and include a working unsubscribe, honoured within five working days.

**Anywhere else:** flag the country and ask the adviser before sending.

## Candidate campaigns, extra checks

- Candidates sourced by the agency (not applicants): in the UK and EU, a lawful basis on record and a notice of where their data came from and how it is used; if you email them, it is due by the first email at the latest. Sourced profiles with no response should be deleted or kept only as the agency's retention policy allows.
- Job emails should be about a specific, real role the agency is authorised to recruit for. Promoting the agency itself to individuals can count as direct marketing.
- Pay: the EU Pay Transparency Directive (national laws were due by 7 June 2026; many countries are late) requires initial pay or a pay range before the first interview and bans asking about pay history, once a country's law is in force. Several US states require ranges in job postings and ban salary history questions. Ask the adviser which apply and whether recruiter emails count.
- No questions, filters or hooks about protected traits.
- MPC campaigns: written candidate permission on file; details shared only with companies the candidate agreed to.
- Database campaigns: data within the agency's retention period; objections and opt outs honoured.

## Output

A table: check, status (in place / missing / ask adviser), what to fix. Then a numbered list of questions for the adviser, each specific enough to answer. End with: "This is a checklist, not legal advice."

## Rules

- Never tell the recruiter a campaign is compliant or legal. Say what is in place and what to confirm.
- When unsure, flag it. A false "fine" is worse than an extra question.
- Do not quote penalty amounts; they change and the adviser will know them.
