# Template: The Clause-to-Control Map

Part of [Computational Drafting](../README.md) · v1.1.1 · 2026-07-16 (KST)

The same requirement usually exists in several forms: a contract clause, a policy paragraph, a line in a system prompt, a permission in a runtime, a test in a suite. Each form is a translation, translation is where meaning is lost, and the loss is invisible until an incident makes it the finding. The clause-to-control map is the instrument that makes the translations visible and testable. It is the second obligation of the drafter (see [02-interpreter-map.md](../02-interpreter-map.md)): after completeness, consistency.

The map earns its keep twice. At drafting time it exposes requirements that exist in prose but nowhere enforceable. At audit time it is the document that answers, in minutes rather than weeks, how a legal obligation reaches the execution layer.

## The template

One row per obligation. An obligation without a technical expression is not necessarily a defect, some obligations are genuinely organizational, but the "None" must be written down and accepted rather than assumed away.

| # | Obligation (source and cite) | Operative language (verbatim or precise paraphrase) | Organizational expression | Technical expression | Evidence artifact | Owner | Verified (date, method) |
|---|---|---|---|---|---|---|---|
| 1 | | | | | | | |
| 2 | | | | | | | |

Column discipline:

- **Obligation.** Cite the source at the level a reviewer can find it: agreement, section, version. Requirements without sources are candidates for deletion, not mapping.
- **Operative language.** Quote or precisely paraphrase the controlling words. The map fails if it records the drafter's memory of the clause rather than the clause.
- **Organizational expression.** The policy, procedure or role description that carries the obligation to humans.
- **Technical expression.** The permission, gate, limit, filter, configuration or prompt line that carries it to machines. "Prompt line only" is a legitimate entry and a flag: prompt-only constraints are preferences (see the [companion template](system-prompt-as-delegated-authority.md)).
- **Evidence artifact.** What a reviewer would inspect to confirm the control operated: a log, an approval record, a test result, a configuration export.
- **Owner.** A named role that answers for the row staying true. Rows without owners drift.
- **Verified.** The date someone last confirmed the forms still say the same thing, and how. Any change to any form in the row resets this cell to blank.

## Worked rows

Drawn from the [invoice agent worked example](../examples/invoice-agent-worked-example.md), whose documents, systems and figures are fictitious and illustrative:

| # | Obligation (source and cite) | Operative language | Organizational expression | Technical expression | Evidence artifact | Owner | Verified (date, method) |
|---|---|---|---|---|---|---|---|
| 1 | Delegation of Authority Policy §4.2, v3.1 | Payments above USD 10,000 require Controller approval | AP procedure step 6; Controller review queue | Payment API scope capped at 10,000; amounts above route to blocking approval gate | Gate log entry with approver identity per payment | Controller | 2026-07-15, gate test with 10,001 test invoice |
| 2 | Vendor Master Data Standard §2, v2.0 | Payments only to vendors validated in the master file | Vendor onboarding procedure | Agent holds read-only master-file scope; payment call rejects payee absent from file | Rejection log; monthly reconciliation of payees against master | AP Manager | 2026-07-15, rejection test with unregistered payee |
| 3 | AI Use Policy §7, v1.4 | Agent output is a recommendation until human release | AP procedure step 7; reviewer duty statement | No auto-release path exists; release requires authenticated human action | Release record binding payment to releasing identity | AP Manager | 2026-07-15, configuration export review |

## Maintenance protocol

1. The map is versioned with the specification it serves and amended in the same change series.
2. Any amendment to a source document, policy, prompt or configuration named in a row blanks that row's Verified cell until re-verified.
3. Review the full map on a fixed cadence appropriate to the deployment's risk, and after every incident touching a mapped obligation.
4. Rows whose technical expression reads "None" or "Prompt line only" are reviewed first. They are where the next incident lives.

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
