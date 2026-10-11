# Changelog

Semantic versioning applies. Breaking changes to the instruments (the eight-element anatomy, the review checklist, the hostile-case patterns or any of the templates) increment the major version. New files, patterns or worked examples increment the minor version. Corrections increment the patch version.

## v1.3.2 (2026-10-12)

Corrections from the continuous improvement rotation, slot 1 of 1, sweep of 12 October 2026 (`account-maintenance`, `records/COMPLETION-RECORD-2026-10-12-01-session-sweep-rotation.md`). No instrument changes.

- **Pattern count residue from v1.3.0 cleared.** README Repository Contents read "Six failure patterns" and the closing question of the hostile-case pass read "all six countermeasures"; both now say seven. The worked example states that its pass was run against the six patterns then in the checklist and that Pattern 7, added at v1.3.0, has not been run against that specification. Extending the example to Pattern 7 is new content and is not made here.
- **Doctrine pointer corrected.** README, The Three Doctrines as Drafting Rules, sent the reader to ECOSYSTEM.md for the doctrines' canonical statements. DOCTRINE.md has been the single normative statement since 13 August 2026 (ECOSYSTEM.md v1.7.7); the section now points there and names the map as the summary, matching the Part of the Ecosystem section.
- **Header rule applied retroactively.** `00-quick-start.md` and `03-hostile-case-checklist.md` changed at v1.3.0 (pattern counts, six to seven) and kept their v1.1.1 headers, against the convention logged at v1.2.0. Every file touched in this release carries the v1.3.2 header; untouched files keep theirs.
- **README interpreter summary** names the counterparty and the operator, so the summary lists all nine interpreters of the map.
- **House style.** US spellings (judgment, recognizes, license) and four serial commas removed from the author's prose in 02, 03 and the operator card; the three lawful outcomes of confirmation are now listed with semicolons so "amend and confirm" stays one outcome.
- README version table, How to Cite and `CITATION.cff` to v1.3.2 in lockstep. `01-specification-anatomy.md`, `04-proof-carrying-analysis.md`, the three other templates and `LICENSE.md` are unchanged byte for byte.

## v1.3.1 (2026-09-06)

Citation infrastructure, doctrine citation line and lockstep maintenance. Session C of the September 2026 improvement pack, one patch release per repository across all 21 public repositories.

- **`CITATION.cff` added** in the house form settled at D-C1: no `type` field, `version` and `date-released` in lockstep with the README, `license` as the SPDX identifier for this repository's license, `abstract` taken from this repository's ECOSYSTEM.md role line rather than newly written.
- **How to Cite block** aligned to this release and pointing at `CITATION.cff`.
- **Doctrine citation line added** to the Part of the ecosystem section. This repository restates a doctrine and cited DOCTRINE.md nowhere, which is the Class E2 finding the new guards report.
- **Citation lockstep lag corrected.** How to Cite read `v1.2.0` against a README of `v1.3.0`, the 16 July 2026 defect class. One of the three lags the new Class E3 guard was proved against on the unrepaired tree before this release.
- **Company name corrected.** `BABL.ai` to `BABL AI` in the About the Author section, both occurrences.
- All other files in this repository are unchanged byte for byte.

## v1.3.0 (2026-08-13)

Seventh hostile-case pattern, previously parked.

- **03-hostile-case-checklist: Pattern 7, the premise that looks unavoidable.** The interpreter accepts a framing it was never authorized to accept, because the framing arrived as description rather than as instruction. Nothing in the specification is violated; the specification simply never contemplated that the choice set would be narrated to the system by a party with an interest in the answer. The system then optimizes correctly inside a set someone else drew.
- Patterns 1 through 6 are failures of the interpreter against a known specification. Pattern 7 is a failure of the specification's own boundary, which is why it adds an element rather than a test, and why it was held until the eight-element anatomy was stable enough to absorb it.
- The countermeasure has three moves: name who may set the choice set; give refusal a landing place, extending the three lawful outcomes of confirmation to premises so that "the alternatives presented are incomplete" halts the action with a record rather than becoming an error state the system routes around; and for irreversible actions require an explicit, independently sourced answer to "what happens if we do nothing".
- Pattern counts updated in 00-quick-start and in the checklist preamble. Six to seven.
- License metadata sweep folded into this release: `SPDX-License-Identifier: CC-BY-NC-SA-4.0` and the canonical Creative Commons legal code added inside the existing license file, filename unchanged, human summary retained above the legal code.

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
