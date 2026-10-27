# [Playbook title] – Legal Ambassador Playbook

| Field | Value |
|---|---|
| Playbook ID | PB-[nn] |
| Request type | [one line: which standard requests this covers] |
| Owner (HQ Legal) | [COMPANY-SPECIFIC] |
| Version / status | v0.1 draft / reviewed / released |
| Last reviewed | YYYY-MM-DD |
| Next review | YYYY-MM-DD (default: 12 months, or on regulatory change flagged by country-law tool) |
| Country annex | Section 8 – filled per jurisdiction from [country-law source], dated |

Target length: 4–6 pages plus annex. Written for a non-lawyer ambassador. English. No legal citations in the body; sources go to section 9.

---

## 1. Purpose and scope

- What this playbook helps the ambassador do (two sentences).
- What it does **not** cover (point to sibling playbooks).
- Reminder: this is a triage and standard-handling guide, not legal advice for a specific case.

## 2. Who does what

| Role | Responsibility |
|---|---|
| Requester (local business) | describes the issue, supplies documents |
| Ambassador | classifies, closes standard cases, escalates reserved matters with the escalation form |
| Local external counsel | [COMPANY-SPECIFIC: when the ambassador may instruct directly, spend limit] |
| HQ Legal | decides reserved matters, maintains this playbook |

## 3. Case categories

Numbered list of the 4–8 recurring request types this playbook covers. For each:

- **C[n] – [Name]**
  - Typical request wording ("Can we…", "The customer says…")
  - Route: **Local** / **Local with standard answer** / **Escalate**
  - Reference to decision-tree node

## 4. Decision tree

Start at the top; each question has a yes/no answer that leads to a route or the next question. Thresholds are placeholders until the company's reserved-matters catalogue is mapped.

```
Q1  [first discriminating question]
     ├─ yes → Q2
     └─ no  → ROUTE: Local (C[n])
Q2  [second question, usually: is a mandatory-law issue or a reserved matter involved?]
     ├─ yes → ROUTE: Escalate [RESERVED – see catalogue item R-xx]
     └─ no  → Q3
Q3  [value/exposure question] exceeds [THRESHOLD T-xx]?
     ├─ yes → ROUTE: Escalate
     └─ no  → ROUTE: Local with standard answer S[n]
```

Rules:
- Every leaf is a route, never "it depends".
- `[RESERVED – R-xx]` and `[THRESHOLD T-xx]` are filled from the reserved-matters catalogue; do not invent values here.
- Automatic escalation triggers (always escalate regardless of value) are listed in section 6.

## 5. Standard answers (local handling)

For each case category routed "Local with standard answer":

- **S[n] – [Name]**
  - What the ambassador checks (3–5 bullets)
  - What the ambassador answers / does (plain language, may include a short model text)
  - What to document (where, what fields)
  - Watch-outs that turn this into an escalation

## 6. Escalation

### 6.1 Automatic escalation triggers
Bullet list: situations that always go to HQ regardless of value (e.g. regulator involvement, press, litigation threat, deviation from group standard clause, IP, data breach).

### 6.2 Escalation form
The ambassador sends this and nothing less:

```
Subject: [Playbook ID] – [Subsidiary] – [Case category] – [Counterparty]

Case category: C[n]
Route reached in decision tree: Q[n] → Escalate (trigger: [threshold / reserved item / automatic])
Facts (5 lines max):
Documents attached: [contract / correspondence / local counsel note]
Value or exposure: [amount, currency]
Deadline: [date and why]
Local-law point already known: [yes/no – summary]
Ambassador's proposed handling: [one sentence]
```

### 6.3 Who receives it
[COMPANY-SPECIFIC: mailbox / intake tool / named coordinator]

## 7. FAQ

5–10 short questions ambassadors actually ask, each answered in 2–4 lines.

## 8. Country annex

One table per jurisdiction, filled from the country-law source. Dated. Fields are defined by the query list `justima-queries/[playbook].md`.

| Item | [Country A] | [Country B] | Source / date |
|---|---|---|---|
| … | | | |

## 9. Sources and legal status

- Legal status as of: YYYY-MM.
- Sources used for the generic layer (structural model: BGB §§ 305–310, CISG Art. 8–9, PICC 2.1.19–2.1.22, Directive 93/13/EEC).
- Country annex sources: [country-law tool, retrieval date].
- Open points / uncertainty flagged in text with ⚠.

## 10. Change log

| Date | Version | Change | By |
|---|---|---|---|
