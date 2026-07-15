# The Anatomy of a Computational Specification

Part of [Computational Drafting](README.md) · v1.0.0 · 2026-07-15 (KST)

A computational specification states eight elements. Each is presented here in the same four-part form: what it is, its legal ancestor, its technical expression and the characteristic failure when it is missing. The order is deliberate. Elements one and two establish who wants what and who may act. Elements three through five bound the field of action. Elements six through eight make the action inspectable, interruptible and acceptable.

The elements may live in one artifact or several: a contract, a policy, a system prompt, a permission set, an approval workflow, an API specification. The discipline does not require a single document. It requires that each element exist somewhere enforceable and that the drafter can point to where.

## 1. Objective

**What it is.** The purpose of the system, stated by someone with the right to decide it, at a level of specificity an interpreter can act on. "Improve efficiency" is a wish. "Resolve routine refund requests within policy, measured by policy conformity on weekly sample review" is an objective.

**Legal ancestor.** Recitals and purpose clauses, which courts use to resolve ambiguity in operative terms. The objective performs the same office for every downstream interpreter: it is the tiebreaker when the operative language runs out.

**Technical expression.** The task definition in the system prompt, the success metric in the evaluation suite, the description field that tells a reviewing human what this system is for.

**Failure when missing.** The interpreter substitutes its own objective, usually the most measurable one available. Throughput displaces correctness. Engagement displaces accuracy. The system optimizes what it can see.

## 2. Authority

**What it is.** Who may act, under whose delegation, with which decision rights reserved to the principal. Authority distinguishes the power to recommend from the power to act, and reversible actions from actions that require a human before they occur.

**Legal ancestor.** Agency law, powers of attorney, corporate delegations of authority, signing matrices. The oldest drafting problem there is: conferring enough power to be useful without conferring enough to be dangerous.

**Technical expression.** Role and permission assignments, tool access lists, scopes on credentials, the distinction between draft and send, between propose and execute.

**Failure when missing.** Authority defaults to capability. Whatever the system can technically do, it is treated as permitted to do, and the discovery is made in production.

## 3. Constraints

**What it is.** What must never happen, expressed at the layer where it can be enforced. A prohibition that lives only in prose while the agent retains the permissions and tools to violate it is a preference, not a constraint.

**Legal ancestor.** Negative covenants and conditions. A lender does not merely ask the borrower not to dispose of collateral; the security interest makes the disposition ineffective.

**Technical expression.** Permission boundaries, network and data egress controls, hard-coded refusals, input and output filters, rate and value limits.

**Failure when missing.** The prohibition is honored at exactly the moments it is not needed and fails at the moment it is: under pressure, at speed, on the edge case.

## 4. Precedence

**What it is.** Which instruction wins when instructions conflict. Specifications for interpreted systems are layered: policy over prompt, prompt over retrieved content, principal over user, and the hierarchy must be stated rather than assumed.

**Legal ancestor.** Order-of-precedence clauses in complex agreements, the hierarchy of statute over regulation over guidance, entire-agreement clauses that exclude stray representations.

**Technical expression.** The instruction hierarchy of the deployment: system instructions over user input over tool output over retrieved documents, and the explicit rule that content encountered during execution is data, not command.

**Failure when missing.** The most recent, most local or most insistent instruction wins. In adversarial settings this is the injection vulnerability; in ordinary settings it is drift.

## 5. Exceptions

**What it is.** The permitted departures from the rules above: who may grant one, on what showing, recorded where. A system with no exception path drives its users to work around it; a system with an undrafted exception path has delegated rule-making to whoever is most willing to improvise.

**Legal ancestor.** Waiver and amendment clauses, which insist that departures be express, authorized and written precisely because course-of-dealing otherwise rewrites the contract silently.

**Technical expression.** Override mechanisms with authentication and logging, break-glass procedures, feature flags with owners and expiry dates.

**Failure when missing.** The silent exception: a departure that becomes precedent without anyone deciding it should, invisible until an incident makes it the explanation.

## 6. Evidence

**What it is.** What must be preserved so the decision can be reconstructed: inputs, the instruction version in force, the action taken, the approvals given and the exception record. Evidence is specified before the event, because after the event the only evidence is whatever happened to survive.

**Legal ancestor.** Books-and-records obligations, audit rights, litigation-hold discipline. The law has always known that an unrecorded decision is indistinguishable from an unauthorized one.

**Technical expression.** Logging requirements with retention periods, versioned prompts and configurations, immutable audit trails, the identity binding between an action and the account that took it.

**Failure when missing.** The same incident becomes unprecedented for the third time. The technical log shows which input produced which output but cannot say whether the objective was legitimate or the interpretation correct, and no human record fills the gap.

## 7. Escalation

**What it is.** The conditions that force the system to stop and summon a human: value thresholds, confidence thresholds, named subject matters, novelty, detected conflict among instructions. Escalation is drafted as a blocking condition, not an aspiration. A requirement for human oversight is incomplete unless the system is technically prevented from proceeding until approval arrives.

**Legal ancestor.** Conditions precedent, reserved matters in shareholder agreements, referral obligations in professional rules.

**Technical expression.** Approval gates that block execution, kill switches, human-in-the-loop checkpoints wired into the architecture rather than described beside it.

**Failure when missing.** Machine speed converts a recoverable error into a completed one. The human learns of the decision from its consequences.

## 8. Acceptance

**What it is.** The proof that establishes the output satisfies the objective: the tests, the reviewer, the sampling regime, the criteria fixed before the work begins. Acceptance closes the loop that the objective opened.

**Legal ancestor.** Acceptance testing and inspection clauses in supply and construction contracts, closing conditions in transactions.

**Technical expression.** Evaluation suites, acceptance criteria in the definition of done, sign-off records naming the human who confirmed.

**Failure when missing.** Plausibility substitutes for correctness. The output looks like what was asked for, no one is charged with confirming that it is, and reliance accumulates on unverified work. The acceptance decision itself is developed in depth in [definition-of-done](https://github.com/rolldabones/definition-of-done); this element is where the specification hands off to it.

## Using the anatomy

Draft the eight elements in order, however briefly, before implementation begins. Then walk the draft through the interpreter map ([02-interpreter-map.md](02-interpreter-map.md)) and the hostile-case checklist ([03-hostile-case-checklist.md](03-hostile-case-checklist.md)). An element drafted in one sentence and consciously accepted is discipline. An element absent because nobody asked is a defect waiting for its incident.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
