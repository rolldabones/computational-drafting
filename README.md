# Computational Drafting

*Good intentions do not compile. Specifications do.*

**Son-U Michael Paik**
CEO, GRC Solutions Korea | General Counsel, BABL AI
[www.grcskorea.com](http://www.grcskorea.com)

| Version | Date | Status | License |
|---|---|---|---|
| v1.1.0 | 2026-07-16 (KST) | Final | CC BY-NC-SA 4.0 (see [License](#license)) |

Computational drafting is the design of specifications that translate human and institutional intent into behavior across legal, organizational and technical interpreters. The contributing disciplines include legal drafting, software engineering, systems architecture, internal control, risk management, artificial intelligence governance and audit. This repository is the canonical home of the discipline: its claim, its instruments and a worked example. It is built on one principle.

**Final Liability rests with the Human.**

---

## Contents

- [The Claim](#the-claim)
- [Why Now](#why-now)
- [The Eight Elements](#the-eight-elements)
- [The Interpreter Chain](#the-interpreter-chain)
- [The Three Doctrines as Drafting Rules](#the-three-doctrines-as-drafting-rules)
- [Where This Sits](#where-this-sits)
- [Repository Contents](#repository-contents)
- [How to Use This Repository](#how-to-use-this-repository)
- [Design Principles](#design-principles)
- [Origin](#origin)
- [Part of the Ecosystem](#part-of-the-ecosystem)
- [How to Cite](#how-to-cite)
- [License](#license)
- [Changelog](#changelog)
- [About the Author](#about-the-author)

---

## The Claim

Every consequential system executes a specification, whether or not anyone drafted it deliberately. A contract is a specification for counterparties and courts. A policy is a specification for employees and auditors. A system prompt is a specification for a model. An approval workflow is a specification for a runtime. When these artifacts disagree, the system still acts, and what executes is the accidental sum of the fragments.

Two professions have always worked on opposite sides of the same transformation. Law turns institutional intent into rules for people. Software engineering turns operational intent into rules for machines. Artificial intelligence places people and machines inside the same interpretive chain, and the two crafts converge on a single artifact: the specification that every material interpreter must be able to read, act on and answer for.

Computational drafting is the discipline of producing that artifact. The drafter's task is to express intent precisely enough that every material interpreter, human or machine, is pushed toward reliable, accountable behavior, and to make the translation between interpreters visible enough to test.

The specification is not documentation placed around the system. It is part of the system.

## Why Now

When implementation was expensive, the scarce skill was translation into syntax. Model-assisted development makes implementation cheap and moves the bottleneck upstream. The scarce work is now deciding what should be produced, under whose authority, within which constraints and against which evidence. Those are drafting questions, and they are asked of an interpreter that is probabilistic, discretionary and connected to tools with consequences outside the language of the instruction.

An instruction to such an interpreter is not a command. It is a grant of delegated authority. It must state what the agent may do, what it must not do, which decisions require a human principal, what evidence must be preserved and when the agent must stop. Drafting that grant well is the emerging professional skill this repository exists to develop.

## The Eight Elements

A complete computational specification states eight things. Each has a legal ancestor and a technical expression, developed in full in [01-specification-anatomy.md](01-specification-anatomy.md).

| # | Element | The question it answers |
|---|---|---|
| 1 | Objective | What is this system for, stated by someone with the right to decide |
| 2 | Authority | Who may act, on whose delegation, with which decision rights reserved |
| 3 | Constraints | What must never happen, expressed where it can be enforced |
| 4 | Precedence | Which instruction wins when instructions conflict |
| 5 | Exceptions | What departures are permitted, by whom, recorded how |
| 6 | Evidence | What must be preserved so the decision can be reconstructed |
| 7 | Escalation | What conditions force the system to stop and summon a human |
| 8 | Acceptance | What proof establishes that the output satisfies the objective |

A specification missing any element has not eliminated it. It has delegated it, silently, to whichever interpreter encounters the gap first.

## The Interpreter Chain

The specification is read by more than one interpreter, and each asks a different question of it. The executive asks whether the system serves the objective. The developer asks what must be built. The model asks what response or action follows. The runtime asks whether the action is technically permitted. The reviewer asks whether the result meets the acceptance criteria. The auditor asks whether the decision can be reconstructed. The regulator and the court ask who had authority and who must answer.

A specification that works for only one interpreter is incomplete. [02-interpreter-map.md](02-interpreter-map.md) develops the full chain and supplies a review checklist for walking a draft through it.

## The Three Doctrines as Drafting Rules

Three doctrines govern all work in this ecosystem. Their canonical statements live in the [ecosystem map](https://github.com/rolldabones/rolldabones/blob/main/ECOSYSTEM.md) and are not restated here. In this repository they operate as drafting rules.

- **Informed Intent** drafts first: the objective, authority, constraints, acceptance criteria and escalation conditions are made explicit before implementation begins. A machine cannot preserve an intention nobody took the trouble to state.
- **Slow AI** drafts the tempo: the consequential parts of the system are slowed just enough that objectives, evidence, permissions and human judgment can be inspected before machine speed makes an error irreversible. A requirement for oversight is incomplete unless the architecture is technically blocked until approval arrives.
- **Final Liability** drafts the endpoint: a named human principal with actual decision rights, sufficient information, intervention power and residual responsibility, identified before the agent acts.

Each element of the anatomy serves at least one doctrine: elements one and two are Informed Intent's subject matter, elements three through seven are Slow AI reaching the execution layer and element eight, with the named principal throughout, is Final Liability in operation.

## Where This Sits

This repository owns the specification as artifact: its anatomy, its interpreters and its failure modes. It deliberately does not own what its neighbors own. The [origami-method](https://github.com/rolldabones/origami-method) owns workflow design. [definition-of-done](https://github.com/rolldabones/definition-of-done) owns the acceptance decision. [slow-ai-kitchen](https://github.com/rolldabones/slow-ai-kitchen) owns the operating method. [grc](https://github.com/rolldabones/grc) owns the enterprise capability those specifications serve. Computational drafting is the layer beneath all of them: the discipline that produces the artifact the workflow folds, the method operates, the acceptance decision tests and the capability governs.

## Repository Contents

| File | Purpose |
|---|---|
| [00-quick-start.md](00-quick-start.md) | The minimal drafting loop and a worked miniature, usable without the rest of the repository |
| [01-specification-anatomy.md](01-specification-anatomy.md) | The eight elements in full: legal ancestor, technical expression, drafting guidance and failure mode for each |
| [02-interpreter-map.md](02-interpreter-map.md) | The interpreter chain, the question each interpreter asks and the specification review checklist |
| [03-hostile-case-checklist.md](03-hostile-case-checklist.md) | Six failure patterns of interpreted specifications and the drafting countermeasures for each |
| [templates/system-prompt-as-delegated-authority.md](templates/system-prompt-as-delegated-authority.md) | An annotated system prompt skeleton drafted as an instrument of delegated authority |
| [templates/clause-to-control-map.md](templates/clause-to-control-map.md) | A template mapping contractual and policy obligations to technical controls, evidence and owners |
| [templates/operator-card.md](templates/operator-card.md) | A one-page plain-language card giving the operator the system's authority, constraints and escalation triggers without requiring legal or technical fluency |
| [examples/invoice-agent-worked-example.md](examples/invoice-agent-worked-example.md) | A complete specification for an accounts payable agent, walked through the interpreter map and the hostile-case checklist |

## How to Use This Repository

Read [00-quick-start.md](00-quick-start.md) first. It contains the whole loop in miniature and is usable on its own. The worked example shows the same loop at deployment scale, end to end, including two defects the hostile-case pass catches before anyone could rely on the system.

When drafting a real specification: work through the eight elements in [01-specification-anatomy.md](01-specification-anatomy.md), walk the draft through the checklist in [02-interpreter-map.md](02-interpreter-map.md), then stress it against [03-hostile-case-checklist.md](03-hostile-case-checklist.md) before anyone builds against it. The templates are starting points, not substitutes for judgment: adapt them to the authority structure and evidence requirements of the actual deployment.

Nothing in this repository is legal advice. Specifications that allocate legal authority or liability should be reviewed by qualified counsel in the relevant jurisdiction.

## Design Principles

1. **The specification is part of the system.** Objective, authority, evidence and escalation are architecture, not paperwork around it.
2. **Draft for the interpreter you actually have.** Probabilistic, discretionary and fast, not the obedient literalist the rules pretend.
3. **The hostile case is the design case.** Harmful results are rarely written as requirements. They compile from individually defensible decisions. Draft against the compilation.
4. **Translation must be visible.** Where the legal form, the organizational form and the technical form of a requirement differ, the mapping between them is written down and tested.
5. **Every element lands on a named human.** A specification that cannot say who answers has not finished being drafted.

## Origin

The discipline was named and first developed in the essay [*The Dungeon Is a Legal System*](https://redcaps.substack.com/p/the-dungeon-is-a-legal-system) (Substack, [redcaps](https://open.substack.com/pub/redcaps), July 2026), which read Matt Dinniman's *Dungeon Crawler Carl* as an executable legal system and derived the drafting problem from it. This repository states the discipline fresh rather than excerpting the essay, so that the two artifacts can evolve independently: the essay as origin, the repository as canon.

## Part of the Ecosystem

This repository is part of the [rolldabones governance ecosystem](https://github.com/rolldabones/rolldabones/blob/main/ECOSYSTEM.md), classified in Layer 1 (doctrine and method). The Where This Sits section above describes its function; the canonical map places all repositories in one structure. Nearest neighbors:

- [origami-method](https://github.com/rolldabones/origami-method) - the workflow discipline that folds drafted specifications into repeatable, gated workflows
- [definition-of-done](https://github.com/rolldabones/definition-of-done) - the acceptance doctrine that element eight of every specification feeds
- [slow-ai-kitchen](https://github.com/rolldabones/slow-ai-kitchen) - the 12-step method whose gates the escalation and evidence elements are drafted for
- [grc](https://github.com/rolldabones/grc) - the enterprise GRC method the specifications ultimately serve
- [final-liability-rests-with-the-human-book-wip](https://github.com/rolldabones/final-liability-rests-with-the-human-book-wip) - the book-length argument for the named human every specification must reach

## How to Cite

> Paik, Son-U Michael. *Computational Drafting*, v1.0.0. GRC Solutions Korea, 2026. https://github.com/rolldabones/computational-drafting

## License

This repository is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0). You may share and adapt this material for non-commercial purposes provided you give appropriate credit, indicate if changes were made and distribute your contributions under the same license. Commercial use requires the author's prior written permission.

Suggested attribution: "Computational Drafting by Son-U Michael Paik, GRC Solutions Korea, licensed under CC BY-NC-SA 4.0."

Full license text: https://creativecommons.org/licenses/by-nc-sa/4.0/

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## About the Author

Son-U Michael Paik is an attorney, AI auditor and governance architect with more than 25 years of experience designing risk and compliance systems for cross-border institutions in regulated, high-stakes sectors across Asia, Europe and the United States. He is General Counsel at BABL.ai, a global AI audit provider, and Founder and Chief Executive Officer of GRC Solutions Korea. He holds a Juris Doctor from Columbia Law School, a Master of Business Administration from the Yale School of Management and a Bachelor of Arts in Economics from Syracuse University, is admitted to the New York Bar and holds AI audit certifications from BABL.ai and ForHumanity, including certifications under the EU AI Act, GDPR and the Digital Services Act.

**GRC Solutions Korea:** [www.grcskorea.com](http://www.grcskorea.com)
**LinkedIn:** [linkedin.com/in/sonupaik](https://linkedin.com/in/sonupaik)

---

*Good intentions do not compile. Specifications do.*

**Final Liability rests with the Human.**
