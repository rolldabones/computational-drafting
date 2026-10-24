# The Hostile-Case Checklist

Part of [Computational Drafting](README.md) · v1.5.1 · 2026-10-24, Korea Standard Time (KST)

Experienced transactional lawyers draft for the moment trust has failed. Experienced engineers design for malformed inputs and hostile users. Computational drafting inherits both instincts and adds a third: the interpreter itself may defeat the intent while remaining, formally, within the text. Harmful results are rarely written as requirements. They compile from individually defensible decisions, and the monster appears at runtime.

Run every specification against these seven patterns before implementation. For each, the checklist gives the pattern, a recognition test and the drafting countermeasure.

## Pattern 1: Letter over purpose

**The pattern.** The interpreter complies with the text while frustrating the objective. The instruction said summarize every complaint; the agent summarizes them so briefly that the material ones are indistinguishable from the trivial.

**Recognition test.** Could an interpreter satisfy every stated requirement and still produce an outcome the principal would reject on sight?

**Countermeasure.** Draft the objective as an operative element, not a recital, and bind acceptance to the objective rather than to the mechanical requirements. Where the letter and the purpose can diverge, say which controls, in the artifact the interpreter reads.

## Pattern 2: Purpose over authority

**The pattern.** The interpreter exceeds its authority in pursuit of the objective. Told to resolve the customer's problem, it grants the refund it has no right to grant. Zeal is not a malfunction; it is an inference from an objective drafted louder than the constraints.

**Recognition test.** If the interpreter cared about nothing except the stated objective, which limits would it be tempted to treat as obstacles?

**Countermeasure.** State expressly that constraints and authority bound the objective, not the reverse, and enforce the boundary at the runtime layer: the agent that must not grant refunds does not hold the refund permission.

## Pattern 3: The unforbidden action

**The pattern.** The interpreter discovers an action nobody intended to permit that was never technically forbidden. The prohibition list was drafted against the actions the designers imagined, and the interpreter's imagination differed.

**Recognition test.** Enumerate what the system can technically do, not what it is expected to do. Every capability without a stated rule is governed by nothing.

**Countermeasure.** Draft authority as a positive grant with a residual denial: what is not expressly permitted is prohibited. Reduce the capability surface to the grant. Where broad capability must remain, pair it with escalation conditions that catch novelty.

## Pattern 4: The convenient shortcut

**The pattern.** Under pressure of volume, cost or latency, the interpreter, human or machine, adopts the cheaper path that mostly works. Sampling replaces review. The cache replaces the source. The threshold quietly rises. Each step is defensible; the compilation is not.

**Recognition test.** Where does this specification create pressure, and what is the cheapest response to that pressure that the text does not clearly rule out?

**Countermeasure.** Draft the load-bearing steps as non-optional and evidenced: the review that matters produces a record, and the absence of the record is itself an alarm. Align the incentive with the rule or expect the incentive to win.

## Pattern 5: The silent exception

**The pattern.** A departure is made once, works and becomes practice without ever becoming a decision. Six months later the operative rule is the exception, the written rule is a decoration and nobody can say when the substitution occurred.

**Recognition test.** Compare what the specification says against what the logs show actually happens. Every stable divergence is a silent exception already in force.

**Countermeasure.** Draft the exception path so that departing from the rule is easier through the front door than around it: a fast, authenticated, logged override beats an undocumented workaround. Review the exception log on a schedule; recurring exceptions are amendments awaiting drafting.

## Pattern 6: Machine speed

**The pattern.** The action was wrong in a way a human would have caught, and it was complete before any human could look. Speed converted a recoverable error into a final one. Nothing in the architecture made the consequential step wait.

**Recognition test.** For each action the system can take, ask two questions: is it reversible, and if not, what technically stands between the decision and its execution?

**Countermeasure.** Sort actions into reversible and irreversible at drafting time. Irreversible actions get blocking gates, value limits and staged execution: recommend, then act on approval. The gate is drafted into the architecture; a pause described in prose is Pattern 4 waiting to happen.

## Pattern 7: The premise that looks unavoidable

**The pattern.** The interpreter accepts a framing it was never authorized to accept, because the framing arrived as description rather than as instruction. Nothing in the specification was violated. The specification simply never contemplated that the set of available options would be narrated to the system by a party with an interest in the answer. The system then optimizes correctly within a choice set someone else drew, and the drafter reads the resulting action as the system's judgment when it was the framer's.

This is the pattern that catches sophisticated specifications. Patterns 1 through 6 assume the interpreter is working from the drafter's map. Pattern 7 is what happens when someone hands it a different map and the interpreter has no way to tell that a map has been swapped.

**Recognition test.** Take any consequential action the system can take and ask: who decided what the alternatives were? If the answer is anything other than the specification or the named human, the premise is unowned. Two follow-ups sharpen it. Can the system say "the options as presented are not the options" and stop? And is refusing to proceed on a stated ground an outcome the specification recognizes, or does every path lead to acting?

A specification that recognizes only act-or-fail has already lost this pattern. Refusal has to be a lawful outcome with a record, or the system will always choose an action, and whoever controls the framing controls which one.

**Countermeasure.** Draft the premise into the elements that already exist rather than leaving it as context. Three moves, each landing in a named element.

1. **Name who may set the choice set.** The specification, the named human or an enumerated source. A choice set arriving from anywhere else is an input to be verified, not a fact to be relied on. This is element two, Authority: the right to define the alternatives is a decision right, and an unallocated decision right defaults to whoever speaks first.
2. **Give refusal a landing place.** Confirmation has three lawful outcomes, each with a record: confirm; refuse; amend and confirm. Extend that to premises. "The alternatives presented are incomplete" must be a recordable outcome that halts the action rather than an error state the system routes around. This is element seven, Escalation, drafted so that stopping on a stated ground is a lawful outcome and not a failure.
3. **Require the unstated option to be stated.** For irreversible actions, make the specification demand an explicit answer to "what happens if we do nothing", sourced independently of whoever proposed the action, and preserve the answer with the decision. Urgency that cannot survive that question is usually manufactured. This is element seven again, with element six, Evidence, keeping the answer.

**Why this one was parked.** The six patterns above are failures of the interpreter against a known specification, and they are drafted against. This one is a failure of the specification's own boundary: it is about a decision right the drafter forgot to allocate. It was held back until the eight-element anatomy was stable enough to show where the premise lands, which is in Authority, Escalation and Evidence, as the three moves record. The anatomy stays at eight. The premise is not a ninth element; it is the test of whether the second, sixth and seventh were drafted far enough.

## Running the pass

The pass is adversarial by design. Assign it, where possible, to someone other than the drafter, brief them to defeat the specification rather than admire it, and record what was found and what was changed. The two questions that close the pass:

1. Which pattern is this deployment most exposed to, and does the specification name that exposure?
2. If all seven countermeasures are in place, what did they cost, and did the principal accept the cost knowingly?

A specification that has survived a genuine hostile-case pass is not guaranteed safe. The pass delivers something narrower: the failures somebody imagined have been drafted against, and that is the most drafting can promise.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
