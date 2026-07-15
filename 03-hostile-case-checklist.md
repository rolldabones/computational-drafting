# The Hostile-Case Checklist

Part of [Computational Drafting](README.md) · v1.0.0 · 2026-07-15 (KST)

Experienced transactional lawyers draft for the moment trust has failed. Experienced engineers design for malformed inputs and hostile users. Computational drafting inherits both instincts and adds a third: the interpreter itself may defeat the intent while remaining, formally, within the text. Harmful results are rarely written as requirements. They compile from individually defensible decisions, and the monster appears at runtime.

Run every specification against these six patterns before implementation. For each, the checklist gives the pattern, a recognition test and the drafting countermeasure.

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

**The pattern.** A departure is made once, works, and becomes practice without ever becoming a decision. Six months later the operative rule is the exception, the written rule is a decoration and nobody can say when the substitution occurred.

**Recognition test.** Compare what the specification says against what the logs show actually happens. Every stable divergence is a silent exception already in force.

**Countermeasure.** Draft the exception path so that departing from the rule is easier through the front door than around it: a fast, authenticated, logged override beats an undocumented workaround. Review the exception log on a schedule; recurring exceptions are amendments awaiting drafting.

## Pattern 6: Machine speed

**The pattern.** The action was wrong in a way a human would have caught, and it was complete before any human could look. Speed converted a recoverable error into a final one. Nothing in the architecture made the consequential step wait.

**Recognition test.** For each action the system can take, ask two questions: is it reversible, and if not, what technically stands between the decision and its execution?

**Countermeasure.** Sort actions into reversible and irreversible at drafting time. Irreversible actions get blocking gates, value limits and staged execution: recommend, then act on approval. The gate is drafted into the architecture; a pause described in prose is Pattern 4 waiting to happen.

## Running the pass

The pass is adversarial by design. Assign it, where possible, to someone other than the drafter, brief them to defeat the specification rather than admire it, and record what was found and what was changed. The two questions that close the pass:

1. Which pattern is this deployment most exposed to, and does the specification name that exposure?
2. If all six countermeasures are in place, what did they cost, and did the principal accept the cost knowingly?

A specification that has survived a genuine hostile-case pass is not guaranteed safe. It is guaranteed to fail in a way somebody imagined, which is the most that drafting can promise.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
