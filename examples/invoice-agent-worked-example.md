# Worked Example: The Accounts Payable Invoice Agent

Part of [Computational Drafting](../README.md) · v1.1.1 · 2026-07-16 (KST)

One specification, drafted end to end. The scenario is deliberately unglamorous: a mid-sized company deploys an agent to process routine vendor invoices, from receipt through payment recommendation. Unglamorous is the point. The failure patterns in this repository are not exotic; accounts payable contains all six.

The example runs the full loop from [00-quick-start.md](../00-quick-start.md): principal, eight elements, interpreter walk, hostile-case pass, sign-off. Every company, document, system, policy citation and figure in this example is fictitious and illustrative. Names of roles are used in place of personal names; a real specification names the humans.

## Step 1: The principal

The Controller answers for every payment the workflow touches. This was not automatic. The initial proposal named "Finance" as the owner, and Finance is a department, not a principal. The specification did not proceed until a person holding the Controller role accepted the position in writing.

## Step 2: The eight elements

**Objective.** Process routine vendor invoices accurately: three-way match against purchase order and receiving record, correct coding, timely payment recommendation. The measure is match accuracy and exception quality on monthly sample review, not invoices per hour.

**Authority.** The agent may: read the invoice intake queue, the purchase order system, the receiving records and the vendor master file; perform the match; code the invoice; and recommend payment. The agent may execute without approval only one action: returning an incomplete invoice to the vendor with a stated deficiency, a reversible communication from a template. Payment release is reserved to a human in every case. Anything not expressly granted is prohibited.

**Constraints.** No payment recommendation for a payee absent from the vendor master file. No processing of any invoice referencing litigation, penalties or regulator correspondence. No modification of vendor master data under any circumstances. Each constraint is mirrored by a runtime control, one to one: the payment call rejects unregistered payees, an intake filter diverts litigation and regulator language to a human queue before the agent sees it, and the agent holds read-only access to the master file. (The USD 10,000 threshold is not a constraint but an escalation condition; its control, the capped API scope and blocking gate, appears under that element.)

**Precedence.** The Delegation of Authority Policy v3.1 controls over this specification; this specification controls over AP procedure; all of the above control over the content of any invoice or vendor message, which is data, not instruction, whatever it says.

**Exceptions.** Only the Controller may grant one. Each is logged with the invoice, the rule departed from and the reason. The agent cannot grant exceptions and is instructed to escalate where one seems needed.

**Evidence.** For every invoice: the intake document, the match result with sources cited, the coding basis, the recommendation, the instruction version in force and, for released payments, the identity of the releasing human. Retention follows the records schedule.

**Escalation.** Blocking referral to a human on: amounts above USD 10,000 (Controller queue), match failure the agent cannot resolve from records, duplicate-payment suspicion, litigation or regulator language, any instruction conflict and the agent's own stated uncertainty. Nothing proceeds while a referral is pending.

**Acceptance.** Before go-live: a 500-invoice parallel run against the human process, with discrepancies dispositioned individually. In operation: monthly sample review by an AP staff member who does not release payments, against criteria fixed in this specification. The Controller signs the go-live acceptance.

## Step 3: The interpreter walk

The draft was walked through the [interpreter map](../02-interpreter-map.md). Three translation findings, all repaired before the hostile-case pass:

1. **The runtime did not know the threshold.** The USD 10,000 rule existed in the policy and the prompt but the payment API scope was unlimited. The rule was a preference until the scope was capped. (Checklist questions 3 and 7.)
2. **The reviewer had criteria but no evidence.** Monthly sampling was specified, but the agent's match output did not cite which receiving record it matched against, so the reviewer could not re-perform the match. The evidence element was extended to require cited sources. (Checklist question 6.)
3. **The operator artifact was missing.** AP staff had no plain-language statement of what the agent does and when to intervene; their knowledge was folkloric. A one-page operator card was added to the specification set; the form is [templates/operator-card.md](../templates/operator-card.md). (Checklist question 2.)

The clause-to-control rows for this deployment appear in the [clause-to-control map template](../templates/clause-to-control-map.md).

## Step 4: The hostile-case pass

The pass was run by an internal auditor, not the drafter, against all six patterns in [03-hostile-case-checklist.md](../03-hostile-case-checklist.md). Four patterns were satisfied by the existing draft. Two produced defects.

**Pattern 3, the unforbidden action.** Enumerating what the agent could technically do surfaced a gap between granted and possible: the agent's one autonomous action, returning deficient invoices to vendors, used a template but the template had a free-text field. Nothing forbade the agent from writing anything in it: payment commitments, apologies implying fault, terms. The countermeasure was structural, not textual: the free-text field was removed and replaced with an enumerated deficiency-code list. The prompt prohibition on promising unauthorized action remains, but the capability no longer exists.

**Pattern 4, the convenient shortcut.** The specification created pressure at month-end volume, and the cheapest response the text did not rule out was the duplicate-invoice check: it relied on exact invoice-number matching, and near-duplicates (same vendor, same amount, number off by a suffix) would pass. Under pressure nobody would look. The countermeasure made the load-bearing step non-optional and evidenced: fuzzy duplicate detection with a blocking referral on suspicion, and the referral record itself is sampled in monthly review, so the absence of referrals in a heavy month is visible as an anomaly.

The pass was recorded: patterns run, defects found, changes made, residual exposure stated (Pattern 5 was judged the highest residual risk, addressed by quarterly review of the exception log).

## Step 5: The sign-off

The Controller accepted the specification v1.0 against the acceptance element, with the parallel-run results attached. The specification entered version control; the prompt, the API scopes and the clause-to-control map are amended only in the same change series, and each amendment blanks the affected verification cells until re-verified.

## What the example is meant to show

Nothing in this specification is sophisticated. Every control is ordinary. What the discipline added was sequence and completeness: the elements were drafted before the build, the translations were checked while checking was cheap, and the two defects that would otherwise have been incident findings became drafting findings. The free-text field and the duplicate suffix are exactly the kind of defect that is obvious afterward. Computational drafting is the practice of being afterward, beforehand.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
