# The Interpreter Map

Part of [Computational Drafting](README.md) · v1.1.1 · 2026-07-16 (KST)

A specification is not read once. It is read by a chain of interpreters, each asking a different question of it, each acting on the answer, and each capable of defeating the drafter's intent while remaining formally faithful to the text. The drafter's obligation runs to all of them. A specification that works for only one interpreter is incomplete.

## The chain

| Interpreter | The question it asks | What the specification must give it |
|---|---|---|
| Executive / principal | Does this system serve the objective, and am I willing to answer for it | The objective and authority elements in plain institutional language, plus the residual liability made explicit |
| Counterparty | What am I entitled to, and what remedy do I have | Operative obligations, allocations of risk and the evidence that performance can be demonstrated |
| Employee / operator | What may I do, what must I not do, and when do I call someone | Authority, constraints and escalation in operational language, without requiring legal or technical fluency; the form is [templates/operator-card.md](templates/operator-card.md) |
| Developer | What must be built, and how will I know it is right | Constraints and acceptance criteria in implementable form; the precedence hierarchy as configuration, not folklore |
| Model / agent | What response or action follows from this instruction | The objective, authority, constraints, precedence and escalation elements inside the instruction context, drafted for a probabilistic reader |
| Runtime | Is this action technically permitted for this identity right now | Constraints and authority compiled into permissions, scopes, gates and limits |
| Reviewer | Does this output satisfy the acceptance criteria | Criteria fixed before the work, and the evidence needed to apply them |
| Auditor | Can the decision and its authority be reconstructed from the record | The evidence element: versions, logs, approvals, exceptions, identity bindings |
| Regulator / court | Who had authority, which duties applied, and who must answer | The authority chain and the named human, demonstrable from documents that predate the dispute |

Two properties of the chain matter more than any single row.

**Each interpreter reads a different artifact.** The executive reads a memo, the model reads a prompt, the runtime reads a permission set, the court reads everything. These artifacts are translations of one intent, and translation is where meaning is lost. The drafter's second obligation, after completeness, is to keep the translations consistent and to make the mapping between them explicit enough to test. The instrument for that mapping is [templates/clause-to-control-map.md](templates/clause-to-control-map.md).

**The machine interpreters do not stop to ask.** A human interpreter who finds a gap requests instructions. A model fills the gap with an inference and a runtime fills it with a default, both at speed. Whatever the drafter leaves open is not left undecided. It is decided by the interpreter least equipped to know what the drafter meant.

## The review checklist

Walk every material specification through these questions before implementation begins. Record the answers; the record is itself evidence under element six.

1. Can the principal state the objective in one sentence and confirm, in writing, willingness to answer for the system's operation against it?
2. Does each actor in the chain, human and machine, have its authority stated in the artifact that actor actually reads?
3. Is every constraint enforced at a layer that does not depend on the goodwill of the interpreter it constrains?
4. Is the precedence hierarchy stated, and does it resolve the specific conflict most likely to occur in this deployment?
5. Does the exception path exist, name its approver and produce a record?
6. Could the auditor reconstruct, from evidence specified today, a decision the system will make six months from now, including which version of the instruction was in force?
7. Do the escalation conditions technically block execution, or do they merely request that execution pause?
8. Are the acceptance criteria fixed, and is the accepting human named, before the first output exists?
9. For each pair of artifacts expressing the same requirement, has anyone verified they say the same thing since the last time either changed?
10. If the system did tomorrow the worst thing it is technically capable of doing today, which element was supposed to prevent it, and does that element exist outside prose?

A "no" on any question is not necessarily a defect. It is a decision, and the discipline requires only that it be made by the principal rather than discovered by an incident.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
