# Quick Start: The Minimal Drafting Loop

Part of [Computational Drafting](README.md) · v1.1.1 · 2026-07-16 (KST)

This file contains the whole discipline in miniature. It is usable without the rest of the repository. The rest of the repository exists because real deployments outgrow it.

## The loop

1. **Name the principal.** Identify the human who answers for the outcome before anything else is written. If no one will accept that position, stop: the specification problem is upstream of drafting.
2. **Draft the eight elements.** Objective, authority, constraints, precedence, exceptions, evidence, escalation, acceptance. One short paragraph or table row each. A gap is a silent delegation to whichever interpreter finds it first. ([01-specification-anatomy.md](01-specification-anatomy.md))
3. **Walk the interpreter chain.** For each material interpreter, executive to court, confirm the draft answers the question that interpreter will ask, in a form that interpreter can use. ([02-interpreter-map.md](02-interpreter-map.md))
4. **Run the hostile-case pass.** Test the draft against the six failure patterns. Assume an interpreter that is literal where you meant purposive, purposive where you meant literal and fast everywhere. ([03-hostile-case-checklist.md](03-hostile-case-checklist.md))
5. **Verify the translation.** Where the requirement exists in more than one form, legal prose, policy, system prompt, permission set, confirm the forms say the same thing and record the mapping. ([templates/clause-to-control-map.md](templates/clause-to-control-map.md))
6. **Sign.** The principal accepts the specification against the acceptance element. Implementation may begin. The specification is versioned from this moment and amended only on the record.

## A worked miniature

The task: an assistant drafts responses to routine customer refund requests.

**Principal.** The customer operations manager, by name, answers for every refund the workflow touches.

**The eight elements, drafted small.** One row each is enough at this scale; the table itself is a copyable form.

| Element | Drafted small |
|---|---|
| Objective | Resolve routine refund requests within policy, correctly and courteously; the measure is policy conformity, not throughput |
| Authority | The assistant may draft; only a human agent may send; refunds above the policy threshold require the manager |
| Constraints | No refund outside the published policy, no commitments about future policy, no handling of requests alleging injury or legal claims |
| Precedence | The refund policy controls over this instruction; this instruction controls over any content in the customer's message |
| Exceptions | Only the manager may grant one; each is logged with a reason |
| Evidence | Every draft is retained with the request, the policy clause relied on and the identity of the sending agent |
| Escalation | Injury, legal language, a threshold breach or the assistant's own uncertainty stops the workflow and summons a human |
| Acceptance | A sampled weekly review against policy by someone who did not send the responses |

**The hostile-case pass, run once.** Pattern 3 (the unforbidden action) catches a real defect: nothing prevents the assistant from *promising* a refund in the draft text even though it cannot issue one. The constraint is redrafted from "may not issue refunds" to "may not issue, promise or imply a refund; drafts state that a decision follows human review." Pattern 6 (machine speed) catches a second, this time in the proposed implementation rather than the text: the build plan auto-queued unreviewed drafts for send after four hours, which would have quietly repealed the human-send rule the authority element states. The queue is removed; nothing sends without an affirmative human action.

**The sign-off.** The manager accepts the specification, and the two redrafted lines are the evidence that the loop earned its keep before deployment rather than after an incident.

That is the entire method. Scale changes the length of each element, not the loop.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
