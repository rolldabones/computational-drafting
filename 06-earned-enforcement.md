# Earned Enforcement

Part of [Computational Drafting](README.md) · v1.6.0 · 2026-11-04, Korea Standard Time (KST)

Files 00 to 03 govern the instruction, [04-proof-carrying-analysis.md](04-proof-carrying-analysis.md) governs what comes back and [05-where-precision-belongs.md](05-where-precision-belongs.md) places the precise form of a rule with the interpreter that must not be allowed a second reading. This file takes up a question that arrives after all of those: how strictly a rule is to be enforced, who decides that and what moves it.

The anatomy settles the ends of the range. A prohibition that lives only in prose is a preference, not a constraint (element three), and an escalation condition that merely asks the system to pause is incomplete (element seven; review checklist question 7). Between a preference and a block there are rungs, and most rules in a working deployment sit on one of them: a line in a handbook, a line in a system prompt, a check that fires at the moment of action, a permission the runtime will not grant, a decision that only a named person may take. Which rung a rule occupies is a drafting decision. The ladder in this file gives that decision a form, an owner and a reason to change. The anatomy stays at eight elements, by the author's ruling of 12 October 2026: what follows is a rule of use for elements two, three, five and seven, the operator card and the clause-to-control map, and it changes nothing those files require.

## The occasion

Nate B. Jones's Executive Briefing of 12 July 2026 (Coordinated Universal Time, UTC; 13 July KST), "AI-Native Companies Run on Code: 15 Rules for Operators", is the occasion. The public page of that post names its three parts: the fifteen rules he wrote for his own company, five questions for turning a resented ritual into a rule that can run and an enforcement ladder that sets how strictly a rule applies. Its opening observes that a company already runs on rules nobody voted on, visible in the recurring meeting nobody questions and the approval chain nobody can explain, and that an agent pointed at the calendar and the repository will show them. The post is paid; the companion worksheet is members-only and is neither cited nor linked here; nothing from the paid text or the worksheet is reproduced. The shape of the ladder, the spine of five questions and three features the anatomy did not state (a rule earns its rung, a rung expires and an enforcement can be appealed) are his. The mapping of each rung to an interpreter and an element, the placement of the appeal beside Exceptions and Escalation, the four rules of use and the test are this repository's, written against its own instruments.

The idea is older than either. Ian Ayres and John Braithwaite's enforcement pyramid (1992) had a regulator begin with persuasion and escalate to sanctions only on non-compliance, keeping the heaviest sanction at the apex so that it would rarely need using. The ladder is that pyramid turned inward: an organization applying it to its own rules, read by interpreters that now include a model and a runtime.

## The spine: five questions before the rung

A rule that is to be enforced by a mechanism must first be a rule a mechanism can enforce. The five questions produce one from a ritual. The answers belong in the specification's evidence (element six), because the climb and the sunset, below, both depend on them.

1. **The ritual.** What is done now, by whom, when and in which artifact: the standing meeting, the template, the approval chain, the person everyone checks with first. Name it as practiced, not as documented. The two differ, and the difference is where the hostile-case pass begins.
2. **The scarcity.** What the ritual protected when it was made: one person's attention, a budget, a system's capacity, a counterparty's trust, a legal position, a window of time. A ritual with no scarcity behind it is a cost with a history.
3. **Still real.** Whether the scarcity exists today, in whose judgment, on what evidence and when that was last checked. The answer is dated and owned, because it is the answer the sunset re-asks.
4. **The checkable rule.** A statement an interpreter can tell was broken: who, what, under which condition, with which record. "Be careful with customer data" is a value. "No export from the customer table leaves the tenancy without a ticket number in the export log" is a rule. Walk it through [03-hostile-case-checklist.md](03-hostile-case-checklist.md) before choosing its rung, because Pattern 1 (letter over purpose) and Pattern 3 (the unforbidden action) are what a rule at the instruction rung meets first.
5. **The machinery.** Trigger, evidence, action, owner, appeal. The trigger is the condition that fires the rule, an escalation condition in the sense of element seven or a lighter one. The evidence is what the record must hold to show that the rule fired or did not (element six). The action is the rung. The owner is the named human who answers for the rule and for its rung. The appeal is the path by which a person other than the one who applied the enforcement can reverse or vary it after the fact.

The appeal is distinct from the two paths the anatomy already has. Exceptions (element five) permit a departure in advance, by an approver, with a record. Escalation (element seven) stops the system and summons a human before the action. The appeal runs after an enforcement has been applied, is decided by someone other than the one who applied it and leaves a record; and a run of successful appeals is the evidence that the rung is set too high. A rule with no appeal is enforced by whoever is least willing to be argued with.

## The ladder

| Rung | What it is | Interpreter that supplies it | Where it is written | Element it serves | What it costs when the rule is wrong |
|---|---|---|---|---|---|
| 1 Value | A stated preference with no mechanism behind it | The executive | The objective, the design principles, the handbook | One (Objective) | Nothing; it also enforces nothing |
| 2 Instruction | The rule addressed to the interpreter that will act, in the artifact that interpreter reads | The operator, through the operator card; the model, through the system prompt | [templates/operator-card.md](templates/operator-card.md); [templates/system-prompt-as-delegated-authority.md](templates/system-prompt-as-delegated-authority.md) | Three or seven, as text; in element three's terms a preference until a higher rung backs it | Compliance at the interpreter's discretion; Patterns 1, 2 and 3 |
| 3 Reminder | The rule restated at the moment of action by a mechanism that can be dismissed: a gate in the workflow, a scheduled check, a linter, a confirmation step | The developer, who builds it; the operator, who meets it | Workflow gates ([origami-method](https://github.com/rolldabones/origami-method)), scheduled checks, pre-commit and pre-submit hooks | Seven's trigger without seven's stop | Friction, and a fatigue that turns the reminder into noise; a dismissed reminder is Pattern 4 |
| 4 Hard block | The action is technically impossible unless a condition holds: a permission set, a scope, a value limit, a gate the runtime enforces | The runtime | The precise artifact of [05-where-precision-belongs.md](05-where-precision-belongs.md) | Three, enforced; seven, where the block summons a human | A legitimate action blocked, which drives a workaround unless the path of element five exists; Pattern 5 |
| 5 Human-owned decision | The action is reserved to a named person who decides each instance; the system may prepare the decision and may not take it | The named human, holding decision rights the authority element reserves | The reserved matters of element two; the stop of element seven | Two and seven | The person's attention and a queue; delegation by fatigue if the queue is never resourced |

Two properties of the table bear on drafting. First, each rung is supplied by a different interpreter, so a climb is a change to a different artifact: from the card to the workflow to the permission set to the reserved-matters list. The [clause-to-control map](templates/clause-to-control-map.md) records which artifact carries the rule, which is to say its rung, and a climb blanks the Verified cell of that row until the new artifact is tested against the reference the authorizing party approved (05, consequence 1). Second, rung five is not the top of a scale of strictness. It is a different kind of rule: a decision kept for a person because the organization has decided that no mechanism should take it, whatever that mechanism's record. The reserved actions, below, live there by design and not by failure.

The worked example shows three rungs in one deployment. The USD 10,000 rule in the policy and the prompt was a preference until the payment API scope was capped, the climb from rung two to rung four that the first interpreter-walk finding records; the Controller queue above the threshold is rung five; the operator card added on the third finding is rung two for the accounts payable staff ([examples/invoice-agent-worked-example.md](examples/invoice-agent-worked-example.md)).

## Four rules of use

**1. Default down.** A rule begins at the lightest rung that protects the scarcity named in question 2, which for most rules is the instruction rung, in the artifact the interpreter reads. The hostile-case pass can justify a higher starting rung, but only by naming the failure the instruction would not survive, and that name goes in the record. A rule that starts at the hard block because a block was easy to build has skipped the questions, and the organization will learn what the block protected when a legitimate action meets it.

**2. Climb on an observed failure, named.** A rule moves up one rung on an incident record (element six) that names the rule, the interpreter that failed it, what the interpreter did and the harm or the near miss. "People keep forgetting" is a count, not a record; the record says who forgot what, when and with what consequence. The climb is a change to the specification: the owner signs it, the map row that carries the rule is re-verified and, for a climb to rung four, the conformance tests of 05 run before deployment. A rung is not climbed on an anticipated failure. Anticipation belongs in the hostile-case pass that set the starting rung.

**3. Sunset.** Every rung above instruction carries an expiry date, and on that date the rule returns to the rung below unless the owner renews it on evidence that the scarcity is still real (question 3) and that the failure which justified the climb would recur without it. The renewal is recorded; so is the lapse. An enforcement above instruction is an authorization to a mechanism to act against people, and like the authorization that **Informed Intent** requires before an AI system acts, it states its exit at the outset. A block that nobody can remember the reason for is the ritual of question 1, one generation on.

**4. Reserved actions.** Some actions never leave rung five, whatever the evidence record of the mechanism that could take them: ending a person's employment or engagement; moving money outside a limit tested in advance; publishing to a customer, a counterparty or a regulator; destroying or altering production data or evidence; judging a person's character, honesty or fitness. The reservation is written into element two as reserved decision rights, and it does not sunset. The system prepares the decision, assembles the evidence and presents the options; a person decides, and the record shows that a person decided (checklist question 11 governs the options presented). The classes follow Nate B. Jones's reservation; they are restated here for this repository's interpreters, and the drafter adds to them for the deployment in hand.

## Where the rungs land in the instruments

No instrument file changes. Each already has a place for the rung.

- **The operator card** is rung two for the human interpreter. Its sections WHAT YOU MAY NOT DO and WHEN TO STOP AND CALL carry the rules at rung two; its section WHO ANSWERS names the owner; and the actions reserved at rung five appear in it as the cases in which the operator decides or refers, never as cases the system decides.
- **The system prompt as delegated authority** is rung two for the model. A prohibition in the prompt is honored at the model's discretion, which element three calls a preference; the block that makes it a constraint lives in the runtime, outside the prompt, where 05 places the precise form.
- **The clause-to-control map** records the artifact that carries each rule, which fixes its rung. A climb changes the artifact and blanks the Verified cell; the map's test record is where the climb's conformance test is logged.
- **The claim-evidence matrix** holds the answer to question 3 as a dated Fact or Uncertainty claim with an owner, so that the sunset's re-ask has a row to update.
- **The hostile-case checklist** sets the starting rung and holds the anticipated failures on which, under rule 2, a climb may not be based.

## The interpreters, by rung

Read against [02-interpreter-map.md](02-interpreter-map.md): the executive holds rung one and signs every climb. The operator reads rung two on the card, meets rung three in the workflow and, where named, is the person at rung five. The developer builds rungs three and four and builds nothing at rung five. The model reads rung two in the prompt, is bounded by rung four and is never the decider at rung five. The runtime supplies rung four. The reviewer tests that the rung the specification sets is the rung in force (checklist question 9). The auditor reconstructs the climbs, the renewals and the lapses from the record (question 6). The regulator and the court ask who held the rung-five decision and whether that person took it.

## The test

For each rule: name the scarcity and show that it is still real. State the rule so that an interpreter can tell it was broken. Choose the lightest rung that protects the scarcity and name the artifact that carries it. Name the owner and the appeal. Date the sunset. Keep the reserved actions at rung five and write them into element two. Write down which observed failure would move the rung, and who signs the move.

## Sources

- Nate B. Jones, "AI-Native Companies Run on Code: 15 Rules for Operators," Executive Briefing, *Nate's Newsletter* (Substack), 12 July 2026 (UTC). https://natesnewsletter.substack.com/p/ai-native-company-rules Paid post; its public page (title, subtitle and opening) was read on 4 November 2026 (KST), and the subtitle names the fifteen rules, the five questions and the enforcement ladder. Nothing from the paid text is reproduced. The companion worksheet is members-only and is neither cited nor linked. No companion video was located.
- Ian Ayres and John Braithwaite, *Responsive Regulation: Transcending the Deregulation Debate* (Oxford University Press, 1992), the enforcement pyramid. Cited without quotation.
- [DOCTRINE.md](https://github.com/rolldabones/rolldabones/blob/main/DOCTRINE.md), the account's single normative statement of the three doctrines, section 8 short forms.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
