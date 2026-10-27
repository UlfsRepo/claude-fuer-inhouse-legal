# Reserved Matters Catalogue – Skeleton (structure only)

This file defines the **shape** of the reserved-matters catalogue that the playbooks reference via `[RESERVED – R-xx]` and `[THRESHOLD T-xx]`. The content is company-specific and is completed inside the company tenant from the existing reserved-matters checklist. **Do not fill this file in this repository.**

## Part 1 – Reserved matters (always HQ Legal)

| ID | Matter | Trigger wording for ambassadors | Playbooks referencing |
|---|---|---|---|
| R-01 | Deviation from group standard clauses | "change / waive / deviate from liability, warranty, retention of title, payment, governing law, jurisdiction" | PB-01, PB-02, PB-03 |
| R-02 | New sales channel, marketplace or webshop setup | "go live", "new platform", "new checkout" | PB-01 |
| R-03 | [COMPANY-SPECIFIC] | | |
| … | | | |

## Part 2 – Materiality thresholds

| ID | Measure | Value | Currency / basis | Applies to |
|---|---|---|---|---|
| T-01 | Contract value above which counterparty terms must be escalated | [COMPANY-SPECIFIC] | [one-off / annual] | PB-01 S2 |
| T-02 | Claim or exposure value for warranty/guarantee cases | [COMPANY-SPECIFIC] | | PB-03 |
| T-03 | Litigation value / amount in dispute | [COMPANY-SPECIFIC] | | PB-04 |
| T-04 | Settlement authority of the subsidiary | [COMPANY-SPECIFIC] | | PB-03, PB-04 |
| T-05 | Spend limit for instructing local external counsel without HQ approval | [COMPANY-SPECIFIC] | | all |

## Part 3 – Automatic triggers (value-independent)

Consolidated list of A-triggers from all playbooks, de-duplicated. Source of truth for the playbooks' section 6.1.

| ID | Trigger | Playbooks |
|---|---|---|
| A1 | Dispute, lawyer's letter, regulator, consumer association, press | all |
| A2 | Counterparty terms with unlimited liability / penalties / IP / exclusivity / MFC / audit / foreign law | PB-01, PB-02 |
| … | | |

## Part 4 – Local discretion

Clauses or decisions a subsidiary may take without escalation, per market. Mirrors annex row C1 in each playbook.

| Market | Item | Limits | Approved by / date |
|---|---|---|---|
| | | | |

## Mapping check (to do once the existing checklist is available)

1. Map every item of the existing checklist to R-, T- or A-IDs. Items that fit none → new category or drop.
2. Items in the playbooks with no counterpart in the checklist → propose to add, or downgrade to "local".
3. Terminology: adopt the checklist's wording in the playbooks, not the other way round.
4. Compare against the request log (intake table): requests that were escalated but fall under "local" here, and vice versa, are the calibration cases for the thresholds.
