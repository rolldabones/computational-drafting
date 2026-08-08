# Proof-Carrying Analysis

Part of [Computational Drafting](README.md) · v1.2.0 · 2026-08-07 (KST)

The first four files of this repository govern the instruction. This one governs what comes back.

A specification drafted to the eight elements establishes what an interpreter was authorized to do. It does not establish that a particular output did it. Those are different questions, they fail in different ways and they need different instruments. A perfectly drafted specification is fully compatible with an output that cites a superseded rule, assumes a fact nobody checked and reaches a conclusion the record does not support. Nothing in the specification catches that, because the specification was written before the output existed.

The name is borrowed. In computer security, proof-carrying code attaches to a program a machine-checkable proof that it satisfies the receiving system's safety policy, so the host verifies rather than trusts an untrusted producer (George C. Necula, "Proof-Carrying Code," POPL '97, 106-119). The analogy is deliberate and partial: professional analysis admits no machine-checkable proof, and the verifier is a competent human rather than a checker. What transfers is the shape. The producer supplies the evidence for its own claims in a form the recipient can test, and the recipient tests rather than trusts.

## The asymmetry this closes

| Question | Governed by | Owned by |
|---|---|---|
| What the system may do | The specification, eight elements | This repository, [01-specification-anatomy.md](01-specification-anatomy.md) |
| What a given output actually claims, and on what | The claim-evidence record | This file and [templates/claim-evidence-matrix.md](templates/claim-evidence-matrix.md) |
| Whether the result may be relied upon | The definition of done and its confirmation | [definition-of-done](https://github.com/rolldabones/definition-of-done) |

The middle row is the one that has no natural owner. Reviewers inherit a finished document and assess it as prose, which means they assess the register. Register is the single thing a language model produces most reliably and the single worst predictor of whether the analysis holds.

## The unit of review is the claim

A memorandum is not a claim. It is a container for twenty or thirty of them, of which perhaps two carry the conclusion. Reviewing the container tells you whether it reads well. Reviewing the claims tells you whether it is right.

Decomposition is therefore the first operation, and it is unglamorous: read the output, extract every proposition that a decision would rest on, discard the connective tissue and number what remains. Claims that survive decomposition get a row. Claims that dissolve on inspection, because they turn out to be restatements, transitions or emphasis, were never load-bearing and their disappearance is itself a finding.

## Six claim types

Each type asserts a different kind of thing, is supported by a different kind of material and fails in a characteristic way. Typing every claim before verifying it prevents the most common review failure, which is applying a factual standard to a legal proposition or a legal standard to an inference.

| Type | What it asserts | What supports it | Characteristic failure |
|---|---|---|---|
| Fact | Something about the record or the world | A source document, a system record, a witness account, an identified data set | Assumed rather than evidenced, then relied upon as though evidenced |
| Rule | That an authority provides something | A pinpoint citation with issuer, level, jurisdiction and date | Superseded, nonbinding or misread authority cited as controlling |
| Interpretation | A reading of a rule that the rule does not state on its face | Reasoning, plus the competing constructions and why they lose | Presented in the register of the rule itself, so the reader never sees the choice |
| Inference | A conclusion drawn from facts and rules | The claims it depends on, and the step from them | A probabilistic step reported as a certainty |
| Recommendation | That someone should do something | The claims it rests on, the objective it serves and the alternatives declined | Smuggles a value judgment or a risk appetite in as an analytic result |
| Uncertainty | That something material is not known | What would resolve it, who owns resolving it, what turns on it | Stated in the draft and quietly absent from the final |

Uncertainty is a claim type rather than an absence of one. A stated gap is an assertion about the state of the record, it is frequently the most valuable line in the analysis, and it is the line most often lost between the working draft and the client version.

## The dependency chain

Every material claim names the claims it stands on. This is the property borrowed from the *Elements*, where a proposition cites the earlier propositions it uses and a reader can walk backward from any result to the postulates.

Its practical value is not elegance. It is what happens when something changes. When a source claim is downgraded, because the document turned out to be a draft, the regulation was amended or the witness withdrew the statement, every claim downstream of it is unverified again, immediately and by construction. Without the chain, a change in one fact requires re-reading the whole analysis and hoping. With it, the affected rows are visible in seconds.

Order the rows so that no claim depends on a later one. If that ordering cannot be produced, the analysis contains a circularity that was invisible in prose.

## Counterauthority is a field, not a courtesy

The record requires an entry for contrary authority, conflicting evidence, applicable exception or the strongest available objection.

An empty cell means one thing only: searched, none found, on this date, by this method. It never means nobody looked. The distinction is the whole control. Generative systems are agreeable by construction and will assemble a supporting case on request without volunteering that a better one runs the other way, and human reviewers under time pressure exhibit the same behavior for different reasons.

In legal work the exception frequently decides the outcome, so exception-first validation is not a refinement of the review. It is the review.

## Status values

Five, and no others. Ambiguity in this column defeats the instrument.

- **Verified.** Checked against the cited source by a named person on a named date.
- **Inferred.** Follows from other claims in the record. Not independently evidenced, and legitimate where labeled.
- **Disputed.** A contrary authority, a conflicting document or an opposing party asserts otherwise, and the conflict is unresolved.
- **Unverified.** Asserted, plausible, not yet checked. The default for anything a model produced and nobody opened.
- **Superseded.** Was true of an earlier version of the record or the law. Retained with its replacement noted, because deletion destroys the audit trail.

Anything a model generated is Unverified until a human opens the source. Fluency is not a status.

## Confidence and the reversal trigger

Calibrated confidence on its own is decoration. Paired with the condition that would change the answer, it becomes operative: it tells the recipient what to watch and what to go and find.

State the trigger as an event rather than a feeling. Not "moderate confidence" but "moderate; reverses if the master agreement contains a most-favored-nation clause, which we have not seen."

## Proportionality

The record is calibrated to consequence, not applied uniformly. Three tiers, and the tier is chosen before the work rather than after.

| Tier | Typical work | Record |
|---|---|---|
| Light | Internal explanation, first-pass triage, drafting support with no external reliance | Sources listed, assumptions listed, one human check |
| Standard | Advice relied upon internally, contract positions, policy interpretation | Full matrix on material claims, counterauthority field completed, named sign-off |
| Full | Regulatory positions, board advice, litigation, employment decisions, AI system classification, anything external-facing | Full matrix on every claim, separate adversarial pass, preserved sources, version history, retained as a matter file |

Applying the Full tier to everything guarantees the instrument is abandoned within a month. That failure mode is more likely than under-application and should be designed against.

## Where this sits

Computational drafting governs the instruction. The claim-evidence matrix governs the output. The [definition of done](https://github.com/rolldabones/definition-of-done) governs whether the output may be relied upon: its confirmation record is the signature, and the completed matrix is a principal thing the confirmer inspects before signing.

The three doctrines operate here as they do throughout the discipline. **Informed Intent** requires the frame before the prompting: decision question, governing law, law-as-of date, authorized record and unacceptable error, settled before generation rather than reconstructed after it. **Slow AI** is the decomposition itself, which imposes exactly enough delay between a fluent output and reliance on it for the two to be told apart. **Final Liability** is the sign-off block: a named human, a stated scope of approval and a date, on a record that made the acceptance an act of judgment rather than an act of faith.

## What this is not

It is not a claim that legal or professional analysis can be made deductive. Law has open texture, its authority is institutional rather than logical, its facts are contested and its conclusions are defeasible by design. The instrument does not remove any of that and should not be described as though it does.

It does not make an analysis correct. It makes an analysis inspectable, which is a lesser and more achievable property, and the only one that survives contact with a reviewer, a regulator or a court.

It does not validate itself. The adversarial pass must be run by a different reviewer, a different model or at minimum a different context from the one that produced the claims. A system asked to find the weaknesses in its own output will produce a fluent list of the weaknesses it already accounted for.

And it is not evidence of conformity with any particular standard or statutory record-keeping obligation. Whether a completed record satisfies a documentation requirement in a given jurisdiction is a legal question for counsel in that jurisdiction, and this file makes no such claim.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
