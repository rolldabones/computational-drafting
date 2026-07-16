# Template: The Operator Card

Part of [Computational Drafting](../README.md) · v1.1.0 · 2026-07-16 (KST)

The operator is the interpreter most specifications never address. The executive gets a memo, the model gets a prompt, the runtime gets a permission set, the auditor gets a log, and the human who sits next to the system every day gets folklore: what may I do, what must I not do, and when do I call someone, learned from whoever trained them and amended by whatever has gone wrong so far. The [interpreter map](../02-interpreter-map.md) requires that each actor's authority be stated in the artifact that actor actually reads (review checklist question 2), and for the operator that artifact must exist before it can be read. The operator card is that artifact. It is the form the [worked example](../examples/invoice-agent-worked-example.md) produced when its third interpreter-walk finding was that operator knowledge was folkloric.

Three rules govern its use. First, plain language: the card translates the authority, constraints and escalation elements for a reader with no legal or technical fluency, and any term the operator would have to ask about is a defect in the card, not in the operator. Second, one page: a card nobody reads governs nothing, and length is the usual reason nobody reads. Third, the card is part of the specification set, not documentation beside it: it is versioned with the specification, re-issued whenever the authority, constraints or escalation elements change, and listed as an organizational expression in the [clause-to-control map](clause-to-control-map.md), so a change to the card blanks the Verified cell of every row that cites it.

---

## The skeleton

```
OPERATOR CARD: [system name]

Version [X.Y.Z] · [date] · Replaces [prior version]
Issued under [specification name and version]. If the system and
this card disagree, stop and report it. Do not improvise.

WHAT THIS SYSTEM DOES
[Two or three sentences, in the words of the objective element.
What it is for and how success is measured.]

WHAT IT DOES ON ITS OWN
- [autonomous action 1, in plain words]
- [autonomous action 2]
Everything else it only drafts, recommends or asks about. Nothing
it produces is final until a person confirms it.

WHAT IT MUST NEVER DO
- [prohibition 1]
- [prohibition 2]
If you see it do any of these, stop it (below) and report it. A
rule that failed once is an incident, not a curiosity.

WHAT YOU MAY DO
- [operator action 1, e.g. release, return, correct, annotate]
- [operator action 2]

WHAT YOU MAY NOT DO
- [reserved action 1, e.g. grant exceptions to any rule above]
- [reserved action 2, e.g. approve an item you prepared]
Exceptions are granted only by [named role] and are recorded.

WHEN TO STOP AND CALL
Stop the workflow and contact [named role or queue] when:
- [trigger 1, e.g. amount or volume above threshold]
- [trigger 2, e.g. legal language, injury, regulator contact]
- the system does anything outside this card
- you are unsure. Unsure counts.

HOW TO STOP
[The concrete action: the button, the queue entry, the person.
If stopping takes more than one step, list the steps.]

WHAT TO RECORD
[What the operator writes down and where: the reason for a
referral, the exception request, the anomaly report.]

WHO ANSWERS
[Named principal] answers for this system. Questions about this
card go to [card owner].
```

---

## Annotations

**The header.** The version line and the replaces line make the card an auditable instrument like every other artifact in the set (anatomy element six): what an operator did can only be judged against the card in force when they did it. The disagree-and-report sentence is the card's precedence clause, drafted for a reader who will never see the word precedence: divergence between the card and the system is escalated, never resolved on the floor.

**What it does on its own.** The recommend/execute split from the [system-prompt template](system-prompt-as-delegated-authority.md), restated for the person watching. An operator who does not know which actions are autonomous cannot tell initiative from malfunction, and will either report everything or nothing.

**What it must never do.** The constraints element, translated. The instruction to treat a violated constraint as an incident makes the operator a detection layer: prompt and runtime controls fail silently, and the human watching is often the first to know (hostile-case Patterns 3 and 6).

**What you may and may not do.** The authority element applied to the operator rather than the agent. The reserved list matters more than the granted list: the silent exception (Pattern 5) usually enters through a helpful human, and the card closes that door by naming who may open it.

**When to stop and call.** The escalation element in operational language. The triggers are copied from the specification, not summarized, and the final trigger is deliberately subjective: a well-drafted card prefers false referrals to quiet improvisation, exactly as the system prompt does. "Unsure counts" is the sentence that makes it true.

**How to stop.** A stop that requires looking up how to stop is Pattern 6 with a human in it. The mechanism is named on the card because the moment it is needed is the worst moment to search for it.

**What to record.** The operator's slice of the evidence element. The referral reason recorded at the time is what lets the monthly review distinguish a healthy escalation pattern from an unhealthy one, and its absence in a heavy month is itself an alarm (Pattern 4).

**Who answers.** Final Liability, stated where the operator can see it. The card owner is named separately from the principal so that questions about the card have somewhere to go other than nowhere.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
