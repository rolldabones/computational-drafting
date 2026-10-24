# Changelog

Semantic versioning applies. Breaking changes to the instruments (the eight-element anatomy, the review checklist, the hostile-case patterns or any of the templates) increment the major version. New files, patterns or worked examples increment the minor version. Corrections increment the patch version.

## v1.5.1 (2026-10-24)

Corrections and pointers following v1.5.0. Changes made with Claude, approved by Michael Paik. No instrument changes: the anatomy, the checklist, the patterns and the templates require what they required.

- **03-hostile-case-checklist, closing sentence.** "It is guaranteed to fail in a way somebody imagined, which is the most that drafting can promise" claimed more than a pass can deliver: no pass can guarantee that every failure is one somebody imagined. The sentence now states what the pass delivers: the failures somebody imagined have been drafted against. `05-where-precision-belongs.md` already restated it in that form, and no other file in the account quotes or restates it.
- **Pointers to the usage rules in 05.** Three instrument files gain one sentence each naming where 05 sets out the rule that bears on them: `01-specification-anatomy.md`, Precedence (consequence 2); `templates/clause-to-control-map.md`, after the column discipline (consequences 1 and 2); `templates/claim-evidence-matrix.md`, beside the pointer to 04 (consequence 3). Each pointer is conditional and says where a rule is set out. None adds an element, a column, a field, a rule of use or a checklist question, so the release is a patch.
- **05-where-precision-belongs:** "no instrument file changes" now reads "none changes what an instrument file requires", which stays true now that three instrument files point to it.
- **CITATION.cff abstract** re-taken verbatim from the ECOSYSTEM.md role line, which now names 05 as "an exposition on machine-readable rules" (rolldabones v2.0.3). The v1.5.0 entry, which records that the instrument files did not point to 05 and that the role line did not name it, stays as cut.
- Headers of the five changed content files (`01`, `03`, `05`, the clause-to-control map and the claim-evidence matrix) advance to v1.5.1 under this repository's header rule. README version table, How to Cite and `CITATION.cff` to v1.5.1 in lockstep. Every other file is unchanged byte for byte.

## v1.5.0 (2026-10-24)

New exposition. Written with Claude, approved by Michael Paik. No instrument file changes. `05-where-precision-belongs.md` adds rules for using the clause-to-control map, the Precedence element and the claim-evidence matrix, an eleven-point drafting brief for a text-and-code clause and a hypothetical worked translation. The instrument files do not yet point to it.

- **05-where-precision-belongs: where the precise, machine-readable form of a rule belongs.** Stephen Wolfram's 2016 essay "Computational Law, Symbolic Discourse and the AI Constitution" proposed that the symbolic form be the primary representation of a contract, with prose a means of producing it. The file records where the discipline converges with that proposal and where it divides. Precision belongs in the artifact read by the interpreter that must not be allowed a second reading, which in most deployments is the runtime; the precise form is tested against a reference that the authorizing party (the principal or, where the specification answers to another's rule, that rule's issuer or the person with authority to interpret it) approved and that the translator did not write. It draws five drafting consequences and sets out an eleven-point drafting brief, with recommended defaults, of what a text-and-code clause must settle. It also works a hypothetical translation of the invoice agent's United States dollar (USD) 10,000 threshold as an abbreviated Section 0 and six claim-evidence rows. The author read the essay after the discipline was built; the file records the two as independent work.
- **Usage rules recorded.** Three of the five consequences add rules for using existing instruments without changing the instrument files: obligation and control are kept as independently authored forms (consequence 1); Precedence states which form governs when they diverge, and on a divergence detected through conformance tests, Acceptance, the clause-to-control map or Evidence, the affected function is held in a state named in advance until a named human releases it (consequence 2); a translation of prose into code is recorded as an Interpretation claim, owned by a person with authority to interpret the source and carried into Section 3 until that person adopts it, with the code's conformance recorded as a separate Inference (consequence 3). The worked translation is labeled hypothetical and amends neither the worked example nor the map.
- **License.** The essay's open content is licensed under Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0), which is not compatible for adaptation with this repository's Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0). The file discusses the essay in its own structure with one quotation of fifteen words and adapts nothing.
- **README, The Claim:** "the two crafts converge on a single artifact" now reads "a single specification", carried to each interpreter in the artifact that interpreter reads, matching the different-artifacts property of `02-interpreter-map.md`; "producing that artifact" becomes "producing that specification".
- **README:** Repository Contents gains the 05 row; How to Use says when to read 05; Origin records the independent convergence and points to 05.
- **ECOSYSTEM.md not changed.** Its computational-drafting role line, and the `CITATION.cff` abstract taken from it, do not name 05; whether they should is left to the author.
- README version table, How to Cite and `CITATION.cff` to v1.5.0 in lockstep. `05-where-precision-belongs.md` carries the v1.5.0 header. Every file other than the README, this file, `CITATION.cff` and the new file is unchanged byte for byte.

## v1.4.4 (2026-10-20)

Corrections from the independent review of 20 October 2026; changes made with Claude, approved by Michael Paik. No instrument changes: the anatomy, the checklist, the patterns and the templates require what they required.

- **Legal accuracy (CDR-01).** `01-specification-anatomy.md`, Constraints, legal ancestor: the security interest does not make a disposition ineffective. It survives the disposition and follows the collateral (Uniform Commercial Code (UCC) §9-315(a)(1)), and a contractual prohibition does not stop the transfer taking effect (UCC §9-401(b)).
- **Doctrine compressions (CDR-02, CDR-03, CDR-08, CDR-16, CDR-19, X-01).** `04-proof-carrying-analysis.md` no longer frames Slow AI as a tempo, and each of its three doctrine sentences now carries the DOCTRINE.md section 8 sentence form verbatim. The README maps Informed Intent to elements one, two, three and seven, names the five authorizer conditions in the section 8 list form, says "the four elements of Informed Intent" and calls definition-of-done an acceptance method rather than a doctrine. Loop step 1 of `00-quick-start.md` now tests the principal against the five authorizer conditions.
- **Worked example and templates (CDR-04, CDR-05, CDR-06, CDR-17).** The README and the worked example now say that two defects were caught before sign-off and a third, Pattern 7, was run after signature. The worked example records the Controller accepting specification v1.1. `templates/clause-to-control-map.md` gains worked rows for duplicate detection and supersession. Worked row 4 of `templates/claim-evidence-matrix.md` now has a filled counterauthority cell and a calibrated confidence.
- **Metadata and licence (CDR-07, CDR-13, CDR-15).** Two file headers had a v1.2.0 date of 2026-08-07 against this file's 2026-08-08; both headers have now advanced under the header rule. The LICENSE summary now follows the Creative Commons deed: NonCommercial without the added permission clause, and the "No additional restrictions" term. A separate line says commercial permission may be sought from the author. The operative legal code is unchanged. The `CITATION.cff` abstract is re-taken from the current ECOSYSTEM.md role line.
- **Style and readability (CDR-09, CDR-10, CDR-11, CDR-12, CDR-14, CDR-18).** Doctrine citation paragraph moved above "Nearest neighbors:". Acronyms spelled out at first use (governance, risk management and compliance; application programming interface; accounts payable; data processing agreement; the POPL '97 symposium; Korea Standard Time in each changed file's header). One serial comma removed in `02-interpreter-map.md`. A whitespace-only line removed from this file. The grcskorea.com links now use https.
- **Erratum to v1.3.1, recorded here (the shipped entry stays as cut).** The v1.3.1 entry says the `CITATION.cff` abstract was taken from ECOSYSTEM.md's role line. That role line has since changed, and the abstract now follows the current line (CDR-15).
- Headers of the seven changed files (`00`, `01`, `02`, `04`, the worked example, the clause-to-control map and the claim-evidence matrix) advance to v1.4.4 under this repository's header rule. README version table, How to Cite and `CITATION.cff` move to v1.4.4 in lockstep.
- Findings applied: CDR-01 to CDR-19 and X-01.

## v1.4.3 (2026-10-20)

- LICENSE: two defects against the Creative Commons legal code corrected (the space in 'ShareAlike. In'; the CC0 sentence of the closing notice). Operative terms unchanged.
- README version table, How to Cite and `CITATION.cff` to v1.4.3 in lockstep. File headers unchanged under this repository's header rule.

## v1.4.2 (2026-10-17)

Doctrine short forms and mechanical corrections from the whole-account review of 15 October 2026 (doc sections 1 and 8; reviewer report 13, items A14, C1, C3 and C5), session T3. No instrument changes: the anatomy, the checklist, the patterns and the templates require what they required.

- **README, The Three Doctrines as Drafting Rules:** the three bullets restated the doctrines into different rules: Slow AI as a tempo ("drafts the tempo", "slowed just enough"), Final Liability with four attributes against the canon's three, and Informed Intent with five items none of which was the canon's exit. Each bullet now quotes the sentence form of DOCTRINE.md v1.2.0 section 8 and says in one sentence what a specification does with it. The paragraph mapping the eight elements to the doctrines is unchanged.
- **Serial commas** removed at three places the review named: `02-interpreter-map.md` (the regulator row), `03-hostile-case-checklist.md` (Pattern 5) and `templates/operator-card.md` (the opening paragraph). The headers of those three files move to v1.4.2 under this repository's header rule.
- **Part of the ecosystem** heading in the protocol's lowercase form; the Contents anchor is unchanged.
- **This file** ends with the closing line, which it lacked.
- README version table, How to Cite and `CITATION.cff` to v1.4.2 in lockstep. Every other file is unchanged byte for byte.

## v1.4.1 (2026-10-15)

Byline correction, on the author's instruction of 15 October 2026 (KST). No instrument changes.

- **README credit line:** "CEO, GRC Solutions Korea | former General Counsel, BABL AI" now reads "CEO, GRC Solutions Korea". About the Author, which names the former role in prose, is unchanged.
- README version table, How to Cite and `CITATION.cff` to v1.4.1 in lockstep. No other file is touched, so every file header stays at the release in which that file last changed. Every file other than the README, CHANGELOG.md and `CITATION.cff` is unchanged byte for byte.

## v1.4.0 (2026-10-12)

Pattern 7 given its home in the eight elements, propagated to the checklist, the skeletons and the worked example. Decided by the author on 12 October 2026: the anatomy stays at eight. No breaking change to any instrument; the templates gain lines, none loses one.

- **03-hostile-case-checklist: the seam closed.** Since v1.3.0 the pattern said of itself that it "adds an element rather than a test", and the anatomy, the loop, the checklist and the skeleton gave that element no home. The countermeasure's three moves now each name where they land: naming who may set the choice set is Authority (element two); giving refusal a landing place is Escalation (element seven); preserving the independently sourced answer to "what happens if we do nothing" is Escalation with Evidence (element six). The closing paragraph says the premise is not a ninth element but the test of whether the second, sixth and seventh were drafted far enough. The v1.3.0 wording stands in this changelog as history.
- **01-specification-anatomy:** Authority names the right to define the alternatives as a decision right; Escalation lists a choice set from an unnamed source among its conditions and states that refusal on a stated ground is a lawful outcome with a record.
- **02-interpreter-map:** review checklist question 11, who may define the alternatives and whether the system can record that the options as presented are not the options and stop. Ten questions to eleven; README Repository Contents says so.
- **templates/system-prompt-as-delegated-authority:** the authority grant names who sets the alternatives and demotes any other source to an input; escalation gains the unnamed-source trigger and the sentence making a stop a lawful outcome. Two annotation sentences tie them to Pattern 7.
- **templates/operator-card:** a stop trigger for options nobody named on the card set, with one annotation sentence.
- **examples/invoice-agent-worked-example:** Pattern 7 run against the signed specification, producing a third defect, a vendor's claim that one invoice replaces another, repaired as specification v1.1 across Authority, Escalation and Evidence. The example's closing paragraph and the README's How to Use count three defects.
- README version table, Repository Contents (02 and 03 rows), How to Use and `CITATION.cff` to v1.4.0; headers of the six touched content files to v1.4.0. `00-quick-start.md`, `04-proof-carrying-analysis.md`, `templates/clause-to-control-map.md`, `templates/claim-evidence-matrix.md` and `LICENSE.md` are unchanged byte for byte.

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

---

**Final Liability rests with the Human.**
