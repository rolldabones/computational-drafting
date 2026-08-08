# Changelog

Semantic versioning applies. Breaking changes to the instruments (the eight-element anatomy, the review checklist, the hostile-case patterns or any of the templates) increment the major version. New files, patterns or worked examples increment the minor version. Corrections increment the patch version.

## v1.2.0 (2026-08-08)

New exposition and template.

- 04-proof-carrying-analysis: the proof-carrying analysis record, the output-side instrument. Each material assertion is logged with its type, authority and pinpoint, dependencies, contradictions, verification status and change conditions, so the reviewer checks the reasoning rather than the prose.
- templates/claim-evidence-matrix: the record's fill-in form.
- Origin: the essay *Common Notions* (8 August 2026), https://redcaps.substack.com/p/common-notions
- README: version table, Repository Contents and How to Cite advance to v1.2.0.
- Convention change, logged here: file headers advance only when the file itself changes. The release version is carried by this changelog, the README version table and the git tag. Headers on the eight unchanged files remain at their prior versions.
- LICENSE.md is unchanged.
  
## v1.1.1 (2026-07-16)

Correction.

- README: the How to Cite block advances with the repository version; it remained at v1.0.0 through the v1.1.0 release.
- All file headers advance to v1.1.1 in lockstep. LICENSE.md is unchanged.

## v1.1.0 (2026-07-16)

New template and precision corrections.

- templates/operator-card: the third template, a one-page plain-language card for the employee and operator interpreter. It is the artifact the worked example's third interpreter-walk finding produced, and the one interpreter the toolkit supplied no form for.
- 02-interpreter-map: the employee/operator row now names the operator card as its form.
- templates/system-prompt-as-delegated-authority: the Precedence annotation now resolves the divergence between the skeleton, which ranks this document above the cited policy, and the worked example, which ranks the policy above the specification. The prompt's primacy is operational, inside the context window; institutional precedence is enforced through the clause-to-control map.
- README: the Origin section links the published essay directly (16 July 2026); the publication-page reference is retained.
- examples/invoice-agent-worked-example: interpreter-walk finding one reworded from "constraint" to "rule" to match step two, which classifies the USD 10,000 threshold as an escalation condition, and now cites checklist questions 3 and 7; finding three names the operator-card form.
- All file headers advance to v1.1.0 in lockstep. LICENSE.md is unchanged.

## v1.0.0 (2026-07-15)

Initial publication.

- README: the claim, the eight elements, the interpreter chain, the three doctrines as drafting rules, positioning within the ecosystem (Layer 1, doctrine and method) and the design principles.
- 00-quick-start: the six-step minimal drafting loop and a worked miniature (customer refund assistant), usable without the rest of the repository.
- 01-specification-anatomy: the eight elements in full, each with legal ancestor, technical expression and characteristic failure mode.
- 02-interpreter-map: the nine-interpreter chain, the question each asks, the two structural properties (divergent artifacts, machine interpreters that do not stop to ask) and the ten-question review checklist.
- 03-hostile-case-checklist: six failure patterns (letter over purpose, purpose over authority, the unforbidden action, the convenient shortcut, the silent exception, machine speed), each with recognition test and drafting countermeasure.
- templates/system-prompt-as-delegated-authority: annotated skeleton drafting the system prompt as an instrument of delegated authority (recitals, grant, reservations, conditions, covenants, termination, precedence).
- templates/clause-to-control-map: the translation-consistency instrument, with column discipline, three worked rows and a maintenance protocol.
- examples/invoice-agent-worked-example: an accounts payable agent specification run end to end through the loop, with three interpreter-walk findings and two hostile-case defects repaired before deployment.
