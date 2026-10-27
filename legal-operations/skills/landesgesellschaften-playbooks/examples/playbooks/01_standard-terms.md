# Standard Terms and Conditions (T&Cs) – Legal Ambassador Playbook

| Field | Value |
|---|---|
| Playbook ID | PB-01 |
| Request type | Requests about the subsidiary's own sales T&Cs, counterparties' purchase terms, and local T&C changes |
| Owner (HQ Legal) | [COMPANY-SPECIFIC] |
| Version / status | v0.1 draft |
| Last reviewed | 2026-10-27 |
| Next review | 2027-10-27 or on country-law change |
| Country annex | Section 8 – to be filled per jurisdiction |

---

## 1. Purpose and scope

This playbook helps you handle the recurring requests around **standard terms**: our own General Terms of Sale (B2B and B2C), the purchase terms customers try to impose on us, and changes local business wants to make to the group template. It tells you which requests you can close yourself, which need a standard answer, and which must go to HQ Legal with the escalation form.

**Not covered here:** warranty and guarantee claims under an already-concluded contract (PB-03), distributor and selective-distribution agreements (PB-02), consumer complaints that have reached a regulator or court (PB-04).

This is a triage guide, not legal advice for a specific contract.

## 2. Who does what

| Role | Responsibility |
|---|---|
| Requester (sales, customer service, e-commerce) | describes the request, attaches the document in question |
| Ambassador | classifies the request (section 3), runs the decision tree (section 4), closes local cases, escalates with the form (section 6) |
| Local external counsel | [COMPANY-SPECIFIC: may be instructed by the ambassador for local-law points up to spend limit T-05] |
| HQ Legal | owns the group T&C template, decides all deviations from group standard clauses, maintains this playbook and the country annex |

## 3. Case categories

- **C1 – "Which T&Cs apply?"** – Business asks whether our T&Cs were validly included in a deal (order form, webshop, email quote, verbal order).
  Route: **Local with standard answer S1**, unless a dispute has already started → C5.

- **C2 – Customer sends its own purchase terms** – A B2B customer (retailer, project developer, public buyer) answers our offer with its own terms or a purchase-order referencing them ("battle of forms").
  Route: **Local with standard answer S2** if the deal is below [THRESHOLD T-01] and the customer's terms contain no automatic trigger; otherwise **Escalate**.

- **C3 – Request to change a group standard clause** – Local sales wants to change liability, warranty period, retention of title, payment terms, governing law or jurisdiction in our T&Cs for one customer or for the whole market.
  Route: **Escalate** (reserved matter [RESERVED – R-01: group template]). Exception: changes listed as "local discretion" in the country annex → **Local**.

- **C4 – Local law requires a change to our T&Cs** – Consumer authority guidance, new statute, or local counsel says a clause in the group template is invalid or must be adapted locally (typical: consumer withdrawal periods, warranty periods, language requirements, price-adjustment clauses).
  Route: **Escalate** with the local-law point attached. HQ Legal updates the template; you do not patch it locally.

- **C5 – T&C clause is disputed in a live case** – A customer or its lawyer claims a clause is invalid, surprising, or was never included, and threatens or has started a claim.
  Route: **Escalate** (automatic trigger: dispute/litigation).

- **C6 – New sales channel or webshop goes live** – E-commerce or a marketplace launch needs T&Cs, a checkout flow, or a consumer-information set.
  Route: **Escalate** for first setup (reserved: [RESERVED – R-02: new channel]); routine text updates after HQ approval → **Local with standard answer S3**.

- **C7 – Translation or language version** – Business needs a local-language version of the group T&Cs, or a customer refuses to accept English/German terms.
  Route: **Local with standard answer S4**; escalate only if the translation changes meaning or a customer makes language the basis of a dispute (→ C5).

## 4. Decision tree

```
Q1  Is there already a dispute, a lawyer's letter, a regulator or the press involved?
     ├─ yes → ESCALATE (automatic trigger A1) – use form, mark URGENT
     └─ no  → Q2

Q2  Does the request ask to change, waive or deviate from a group standard clause
    (liability, warranty, retention of title, payment, governing law, jurisdiction)?
     ├─ yes → Q2a
     └─ no  → Q3

Q2a Is the clause listed as "local discretion" in the country annex for your market?
     ├─ yes → LOCAL – apply the annex position, document in [COMPANY-SPECIFIC: register]
     └─ no  → ESCALATE [RESERVED – R-01]

Q3  Has the counterparty sent its own standard terms (purchase terms, PO conditions)?
     ├─ yes → Q3a
     └─ no  → Q4

Q3a Does the contract value exceed [THRESHOLD T-01] OR do the counterparty's terms contain
    an automatic trigger (unlimited liability, penalties, IP assignment, exclusivity,
    most-favoured-customer, audit rights, non-standard jurisdiction)?
     ├─ yes → ESCALATE
     └─ no  → LOCAL with standard answer S2

Q4  Is the request about setting up T&Cs for a new channel, webshop or marketplace?
     ├─ yes → ESCALATE [RESERVED – R-02] (first setup); routine update → LOCAL S3
     └─ no  → Q5

Q5  Does local law or a local authority require a change to the group template?
     ├─ yes → ESCALATE (attach the local-law source; HQ owns the template)
     └─ no  → Q6

Q6  Is it a question about inclusion ("do our T&Cs apply?") or language/translation?
     ├─ inclusion   → LOCAL with standard answer S1
     ├─ translation → LOCAL with standard answer S4
     └─ neither     → ESCALATE with note "unclassified – please advise category"
```

Placeholders `[THRESHOLD T-xx]` and `[RESERVED – R-xx]` are filled from the company's reserved-matters catalogue. Do not set values locally.

## 5. Standard answers (local handling)

### S1 – "Do our T&Cs apply to this deal?"

**Check**
- Did the offer, order confirmation or webshop checkout **refer to our T&Cs before** the customer accepted? (A reference only on the invoice is too late.)
- Could the customer **access** the T&Cs (link, attachment, printed on the back)?
- B2B or B2C? Consumer rules are stricter; see country annex rows A1–A3.
- Did the customer object or send its own terms? If yes → C2.

**Answer**
- All three boxes ticked and no objection: "Our T&Cs form part of the contract." Keep the evidence (dated offer/confirmation, checkout screenshot).
- A box is missing: tell the business which step was missing and how to do it next time (include reference and link in the offer and confirmation; webshop: checkbox or clear notice before "order with obligation to pay").
- ⚠ Do not state that a specific clause is *enforceable*; inclusion and content validity are different questions.

**Document**: case ID, counterparty, B2B/B2C, evidence of inclusion, answer given.

**Becomes an escalation when**: the customer disputes inclusion in writing, or the contract is above [THRESHOLD T-01].

### S2 – Customer sends its own purchase terms (battle of forms)

**Check**
- Value below [THRESHOLD T-01]?
- Scan the customer's terms for the **automatic triggers** (section 6.1). Any hit → escalate.
- Did we already confirm the order without objecting? (Then the position is weaker; note it.)

**Answer**
- Reply in writing that our offer/confirmation is based on our T&Cs and that the customer's terms are not accepted. Model text:
  > "Thank you for your order. Our delivery is made exclusively on the basis of our General Terms of Sale [date/version], which you can find at [link]. We do not accept deviating purchase conditions; this applies even if we do not object to them again in individual cases."
- Do not sign, countersign or "accept" the customer's PO conditions. If the customer insists on signature → escalate.
- ⚠ In many jurisdictions, conflicting terms cancel each other out and statutory law fills the gap ("knock-out rule"). Which rule applies in your country: see annex row B1. Your written objection is what keeps our position.

**Document**: copy of the customer's terms, our objection email, date.

**Becomes an escalation when**: value above threshold, automatic trigger, customer requires signature of its terms, or the customer is a public buyer with mandatory procurement terms.

### S3 – Routine update of released T&Cs on a local channel

**Check**
- Is the new text the version released by HQ (version number and date match)?
- Only the released text, no local additions.
- B2C channel: version date and a short change notice visible; existing customers notified where the annex (row A5) requires it.

**Answer**: publish; store the previous version with its validity period.

**Becomes an escalation when**: anyone asks to add, remove or reword a clause.

### S4 – Local-language version

**Check**
- Is there already an HQ-released translation? Use it.
- If not: commission a translation of the **released** version only; have local counsel or a qualified reviewer confirm it reflects the meaning; mark the English/German version as prevailing where the template provides for it.

**Answer**: supply the translated version with a prevailing-language note. B2C: check annex row A4 – some jurisdictions require the contract language to be the local language regardless of a prevailing-language clause.

**Becomes an escalation when**: a translation requires substantive change, or a customer makes language the basis of a dispute.

## 6. Escalation

### 6.1 Automatic escalation triggers (always, regardless of value)

- A1 Dispute, lawyer's letter, regulator, consumer association, press
- A2 Counterparty terms containing: unlimited liability, contractual penalties, IP assignment or broad licence, exclusivity or non-compete, most-favoured-customer pricing, audit rights, set-off/retention waivers in the customer's favour, foreign governing law or arbitration we have not approved
- A3 Any change to a group standard clause (unless annex "local discretion")
- A4 Public-sector buyer with mandatory procurement conditions
- A5 Request to sign or countersign the counterparty's conditions
- A6 Setup of a new sales channel, marketplace or webshop
- [COMPANY-SPECIFIC: further triggers from the reserved-matters catalogue]

### 6.2 Escalation form

```
Subject: PB-01 – [Subsidiary] – C[n] – [Counterparty]

Case category: C[n]
Decision-tree route: Q[n] → Escalate (trigger: T-xx / R-xx / A-x)
Facts (max 5 lines):
Documents attached: our offer/confirmation, counterparty terms, correspondence, local counsel note (if any)
Value or exposure: [amount, currency, one-off or annual]
Deadline: [date – e.g. tender closing, delivery date, customer ultimatum]
Local-law point already known: [yes/no – summary, source]
Ambassador's proposed handling: [one sentence]
```

### 6.3 Recipient
[COMPANY-SPECIFIC: intake mailbox / coordinator]

## 7. FAQ

**The customer's PO says "our purchase terms apply exclusively". Does that beat our T&Cs?**
Not by itself. Object in writing (S2). Whether both sets, neither, or the last one applies depends on local law (annex row B1) – that is why the objection matters and why anything above threshold goes to HQ.

**Can I shorten the warranty period in our T&Cs for a big customer who insists?**
No. Warranty period is a group standard clause → C3 → escalate. HQ decides, often within hours if the form is complete.

**Our T&Cs are in English, the customer is a local consumer. Is that a problem?**
Possibly. Several jurisdictions require consumer contracts and pre-contractual information in the local language (annex row A4). For B2C, use the released local-language version; for B2B, English is usually acceptable, but check the annex.

**Local counsel says one of our clauses is invalid here. Can I just delete it?**
No. Send the counsel note with the escalation form (C4). HQ decides whether to adapt the template for your market; an invalid clause usually falls away and statutory law applies, but deleting it locally creates an uncontrolled version.

**The business wants to add a "subject to our T&Cs" line to invoices. Is that enough?**
No. The reference must be made before the contract is concluded – in the offer, the order confirmation or the checkout. Invoices come too late.

**A marketplace (e.g. an online platform) imposes its own seller terms. Who approves?**
C6 → escalate. Marketplace terms often include liability, IP and data provisions that are reserved matters.

**Do I need to notify existing customers when T&Cs change?**
For B2B usually only for future orders. For B2C and for running contracts, many jurisdictions require notice and sometimes active consent (annex row A5). Follow the annex; if unclear, ask HQ before publishing.

## 8. Country annex

Filled per jurisdiction from the country-law source; dated. Query definitions in `justima-queries/01_standard-terms.md`.

| Row | Item | [Country A] | [Country B] | Source / date |
|---|---|---|---|---|
| A1 | B2C inclusion requirements (notice, access, checkbox) | | | |
| A2 | B2C content control – black/grey list exists? key prohibited clauses | | | |
| A3 | Mandatory consumer rules that override T&Cs (warranty period, withdrawal, price adjustment) | | | |
| A4 | Language requirement for consumer contracts | | | |
| A5 | Notice/consent requirement for T&C changes in running contracts | | | |
| B1 | Battle-of-forms rule (last shot / knock-out / first shot) | | | |
| B2 | B2B content control – does a fairness test apply to B2B standard terms? | | | |
| B3 | Surprising-clause / transparency doctrine | | | |
| B4 | Enforceability of retention-of-title clause in standard terms | | | |
| B5 | Liability cap in B2B standard terms – permissible limits | | | |
| B6 | Jurisdiction / arbitration clause in standard terms – formal requirements | | | |
| C1 | Local discretion items (clauses the subsidiary may adapt without escalation) | [COMPANY-SPECIFIC] | | |

## 9. Sources and legal status

- Legal status of the generic layer: 2026-10. Structural model: German BGB §§ 305–310 (inclusion, surprising clauses, content control, consequence of invalidity), CISG Art. 8–9 (inclusion by interpretation and usage), UNIDROIT Principles Art. 2.1.19–2.1.22 (standard terms, surprising terms, battle of forms), Directive 93/13/EEC (unfair terms in consumer contracts). These are used to define the questions, not to state the law of any subsidiary's jurisdiction.
- ⚠ No case law is cited in this playbook. Country-specific statements must be verified against the country annex before being relied on.
- Country annex: [country-law tool], retrieval date per row.

## 10. Change log

| Date | Version | Change | By |
|---|---|---|---|
| 2026-10-27 | v0.1 | Initial generic draft | HQ Legal |
