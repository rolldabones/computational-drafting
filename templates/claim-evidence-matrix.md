# Template: The Claim-Evidence Matrix

Part of [Computational Drafting](../README.md) · v1.2.0 · 2026-08-07 (KST)

An AI-assisted analysis arrives as continuous prose in a confident register. Inside it sit twenty or thirty separable claims, of which two or three carry the conclusion, and nothing on the surface distinguishes the claim that was checked against a primary source from the claim the model supplied because the sentence needed a subject. The claim-evidence matrix separates them. It is the output-side counterpart to the [clause-to-control map](clause-to-control-map.md): that instrument makes the translations of a requirement visible, this one makes the support for an assertion visible.

The matrix earns its keep twice. At drafting time it exposes the claims that exist in prose and nowhere in the record. At review time it lets a reviewer test the analysis rather than read it, which is the difference between an hour and a day, and between a check and an impression.

The rationale for each field is in [04-proof-carrying-analysis.md](../04-proof-carrying-analysis.md). Fill the frame before generating anything. A matrix assembled after the fact records what was produced; a frame set beforehand constrains what gets produced.

---

## Section 0: The frame

Completed before substantive prompting. Every row in Section 1 is conditional on this block.

| Field | Entry |
|---|---|
| Decision question (one narrow proposition, and the action requested) | |
| Audience and reliance (who acts on this, and how far it travels) | |
| Governing law or forum, and the authority hierarchy that applies | |
| Law as of (date) | |
| Record authorized (documents, systems, data sets the analysis may use) | |
| Assumptions carried into the work, and their owners | |
| Unacceptable error (false positive, false negative, missed exception, confidentiality breach, unauditable advice) | |
| Tier (Light / Standard / Full) | |

## Section 1: The claims

One row per material claim, ordered so that no claim depends on a later one. If that ordering cannot be produced, the analysis contains a circularity.

| # | Claim, as asserted | Type | Support (pinpoint source, retrieval date) | Depends on | Status | Counterauthority or conflict | Confidence and reversal trigger | Owner |
|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | |
| 2 | | | | | | | | |
| 3 | | | | | | | | |

Column discipline:

- **Claim, as asserted.** The proposition in the words the output used, not a tidied version. Tidying is where an inference quietly becomes a rule.
- **Type.** Fact, rule, interpretation, inference, recommendation or uncertainty. Type before verifying: the standard of support differs by type, and most review failures are a standard applied to the wrong type.
- **Support.** Enough for a reviewer to find it independently: issuer, instrument, section, version and date, plus the date it was retrieved. "The regulation" is not a citation. A model-generated summary of a source is not the source.
- **Depends on.** The row numbers this claim stands on. A material claim depending on nothing is either a premise, which belongs in Section 0, or an assertion nobody has traced.
- **Status.** Verified, Inferred, Disputed, Unverified or Superseded, with no sixth value. Anything a model produced is Unverified until a human opens the source.
- **Counterauthority or conflict.** Contrary authority, conflicting evidence, an applicable exception or the strongest objection. An empty cell means searched, none found, on this date, by this method. It never means nobody looked.
- **Confidence and reversal trigger.** Calibrated confidence plus the specific event that would change the answer. Confidence without a trigger is decoration.
- **Owner.** A named person who answers for the row staying true. Rows without owners drift.

## Section 2: Adversarial pass

Run by a different reviewer, a different model or at minimum a different context from the one that generated Section 1. A system asked to attack its own output produces a fluent list of the objections it already accommodated.

| Question | Finding | Rows affected |
|---|---|---|
| What is the strongest contrary authority, and was it addressed? | | |
| Which fact is assumed rather than evidenced? | | |
| Which authority may be outdated, nonbinding or superseded? | | |
| Which exception, carve-out or factual distinction would defeat the conclusion? | | |
| Where does a probabilistic step get reported as a certainty? | | |
| Could a skeptical reviewer reproduce this result from the record alone? | | |

## Section 3: Sign-off

| Field | Entry |
|---|---|
| Conclusion, stated narrowly and conditionally | |
| Unresolved items carried forward, with owners | |
| Named human accepting the analysis, and role | |
| Scope of approval (what is accepted, and for what use) | |
| Date and time zone | |

The signature accepts the analysis in the state this record describes. It does not accept anything the record leaves Unverified, and the scope line is where that limit is written down.

---

## A worked fragment

Fictitious and illustrative. The question: whether a vendor may add a subprocessor without the client's consent under an executed data processing agreement.

**Section 0, abbreviated.** Decision question: may the vendor appoint Subprocessor X on 30 days' notice, and if not, what is the remedy. Governing law: England and Wales. Law as of: 7 August 2026. Record: executed DPA v2, the notice email, the vendor's subprocessor register. Unacceptable error: advising that consent is not required when it is. Tier: Standard.

| # | Claim, as asserted | Type | Support | Depends on | Status | Counterauthority or conflict | Confidence and reversal trigger | Owner |
|---|---|---|---|---|---|---|---|---|
| 1 | The executed DPA is version 2 dated 3 March 2025 | Fact | DPA execution copy, signature page, retrieved 6 Aug 2026 | | Verified | None. Searched the contract file 6 Aug 2026; no later amendment located | High; reverses on production of an executed amendment | Counsel |
| 2 | Clause 8.3 permits subprocessor appointment on 30 days' written notice, subject to a client objection right | Rule | DPA v2 cl. 8.3, retrieved 6 Aug 2026 | 1 | Verified | Cl. 8.5 conditions the notice right on the register being current, which cuts against the plain reading of 8.3 | High as to text; the interaction with 8.5 is claim 3 | Counsel |
| 3 | Because the register was last updated in 2024, the 30-day notice route is unavailable and consent is required | Interpretation | Reasoning on cl. 8.3 with cl. 8.5; register export retrieved 6 Aug 2026 | 1, 2 | Disputed | Vendor asserts 8.5 is a reporting covenant rather than a condition; no authority located either way on this drafting | Moderate; reverses if the register was updated and the export is stale, which we have not confirmed with the vendor | Counsel |
| 4 | Whether the client waived the objection by silence on two earlier appointments is not known | Uncertainty | No document located; question put to the account team 6 Aug 2026 | 2 | Unverified | | Material: a course-of-dealing argument would defeat claim 3 | Account team |

Row 4 is the point of the instrument. In prose it would have been a subordinate clause near the end, or nothing at all.

---

## Rules of use

1. **The frame precedes the prompting.** Section 0 completed first, or the matrix is an act of reconstruction and inherits whatever the generation assumed.
2. **A claim without support is not deleted.** It is marked Unverified and the conclusion is re-tested with it removed. If the conclusion survives, the claim was not material. If it does not, the analysis is not ready.
3. **A status change blanks the downstream rows.** Downgrade a source claim and every row depending on it returns to Unverified until re-checked. This is the property the dependency column exists to deliver.
4. **The matrix is versioned with the analysis** and travels with it. A memorandum issued without its matrix is a memorandum issued without its proof.
5. **Tier before work.** Applying the Full tier to routine questions guarantees the instrument is abandoned. Choose the tier deliberately and record it.

This template is a starting point rather than a substitute for judgment, and nothing in it is legal advice. Whether a completed record satisfies a documentation or record-keeping obligation in any jurisdiction is a question for counsel in that jurisdiction.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
