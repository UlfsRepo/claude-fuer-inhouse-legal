# Legal Ambassador Playbooks – Generic Layer

Structural, jurisdiction-neutral and company-neutral playbooks for a **legal ambassador network**: non-lawyer or local-lawyer contacts in sales subsidiaries who handle standard legal requests locally and escalate reserved matters to HQ Legal.

## What this repository contains (and does not)

| Layer | Lives here? | Source |
|---|---|---|
| **Structure & triage** – template, case categories, decision tree, escalation form | Yes | Abstracted from German-law skill library (claude-fuer-deutsches-recht), generalised for cross-border use |
| **Country facts** – statutory periods, mandatory consumer rules, local formalities | Query lists only | To be filled per jurisdiction from a licensed country-law source (e.g. Justima) by HQ Legal |
| **Company governance** – reserved-matters catalogue, materiality thresholds, named approvers | **No** | Company-internal; filled inside the company tenant only |

Every file marks the company layer with `[COMPANY-SPECIFIC]` blocks. These must be completed inside the company's own environment (e.g. an enterprise AI tenant with access to the reserved-matters catalogue) and the result stored in the company's knowledge base – **not committed back to this repository**.

## Folder structure

```
templates/      PLAYBOOK_TEMPLATE.md – the one structure all playbooks follow
playbooks/      one playbook per request type (English)
justima-queries/ per-playbook list of country-fact questions to run against a country-law tool
reserved-matters/ skeleton of the reserved-matters catalogue (structure only, no content)
```

## Build order

1. `templates/PLAYBOOK_TEMPLATE.md` – agree the structure first.
2. `playbooks/01_standard-terms.md` – pilot playbook, used to validate the template.
3. `justima-queries/01_standard-terms.md` – run per priority jurisdiction, store results in the country annex of the playbook (company tenant).
4. Map the company's existing reserved-matters checklist onto the `[THRESHOLD]` and `[RESERVED]` placeholders; adjust template if the taxonomy differs.
5. Only then: remaining playbooks (selective distribution, warranty & guarantee, litigation, corporate governance, product liability).

## Playbook philosophy

A playbook is **not a legal opinion**. It is a triage instrument:

- recognise which case category a request belongs to,
- decide whether it can be closed locally, closed locally with a standard answer, or must be escalated,
- know which information to collect *before* escalating, so HQ can answer in one pass.

Legal content is kept at the level of "what matters and where the traps are", with jurisdiction-specific facts in a separate, dated annex.

## Legal status note

German-law references in the source skills (BGB §§ 305–310 etc.) are used as a **structural model** only. Where a playbook states a legal rule, the applicable law is the law of the subsidiary's jurisdiction unless a choice-of-law clause provides otherwise. Status of legal statements: 2026-10, to be verified per jurisdiction.
