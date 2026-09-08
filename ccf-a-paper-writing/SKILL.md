---
name: ccf-a-paper-writing
description: Plan, write, restructure, revise, or shorten AI, machine-learning, and adjacent technical papers at a CCF-A-caliber standard. Use when turning research notes, code, results, prior work, or an existing manuscript into persuasive academic English with a single defensible contribution story, strict motivation–method–evidence alignment, module-level mechanism support, verified citations, and reviewer-resistant experiments. Do not use for generic prose or formatting-only edits.
license: MIT
---

# CCF-A Paper Writing

Write the strongest honest paper the available research can support. Treat the manuscript as an evidence-backed academic release, not a project diary, result dump, or pre-emptive self-rejection. Persuasion comes from selecting the most significant defensible contribution and making every claim, method choice, experiment, figure, paragraph, and citation advance that case.

## Companion-skill contract

This skill synthesizes and actively uses three complementary systems:

1. **ResearchPilot / `$research`:** use its research-state discipline when research questions, implementation, results, or experiment design must be established or reconciled before writing. If available, load the relevant research phase rather than inventing missing scientific content.
2. **`$anti-defensive-writing`:** apply its press-release principle throughout planning and revision: organize around the strongest publishable value, avoid process-log structure and self-undermining prose, and make the advantage explicit.
3. **`$ccf-a-paper-review`:** use it as the final adversarial gate when available. Invert its motivation–method–evidence, module-effect, novelty, and severity tests into manuscript design requirements.

Do not fail merely because a companion skill is not installed. The references in this package embed the necessary contracts. Never let strategic framing override scientific honesty.

See [third-party-notices.md](references/third-party-notices.md) for source attribution and license notices.

## Read the relevant guidance

- Always read [workflow.md](references/workflow.md) and [narrative-strategy.md](references/narrative-strategy.md).
- Read [section-playbook.md](references/section-playbook.md) before drafting or revising any manuscript section.
- Read [reviewer-gate.md](references/reviewer-gate.md) before finalizing a full paper, revising after feedback, or claiming submission readiness.

## Select the operating mode

Infer the mode from the request and existing artifacts:

- **Paper architecture:** identify the thesis, contribution hierarchy, claim–evidence map, section plan, and figure/table plan before prose.
- **Section drafting:** write or rewrite one section while reading enough of the full paper to preserve global logic and terminology.
- **Full-manuscript drafting:** follow the evidence-first order in `workflow.md`; do not draft front matter around results that have not been verified.
- **Revision or compression:** diagnose the manuscript first, then change the smallest coherent scope; preserve meaning, citations, equations, and cross-references.
- **Reviewer-driven repair:** map each critique to the affected claim and choose among new evidence, technical clarification, claim narrowing, or narrative reconstruction.

If the user requests a specific section, do not force the entire workflow. Perform the minimum upstream checks needed to avoid unsupported or contradictory prose.

## Establish the source of truth

Before writing, locate and read the relevant available materials:

- current manuscript and venue template/instructions;
- research questions, idea report, design documents, and user requirements;
- implementation and configurations for method claims;
- experiment logs and raw/processed result files for quantitative claims;
- figures, tables, captions, and supplementary material;
- bibliography and the primary papers behind important positioning claims;
- reviewer comments, author notes, or style examples when provided.

Use this precedence for factual claims:

1. verified result artifacts and executed evaluation outputs;
2. current code/configuration for implemented behavior;
3. design and research documents;
4. existing manuscript prose;
5. inference, clearly marked as such.

Never fabricate or estimate results, dataset statistics, hyperparameters, citations, dates, theorem conditions, or implementation details. If sources conflict, report the conflict and reconcile it before asserting the fact.

## Build the paper contract before prose

Construct the following working artifacts, inline or in the project as appropriate:

1. **Paper thesis:** one sentence stating the problem, technical insight, solution, strongest supported advantage, and target setting.
2. **Contribution hierarchy:** one primary contribution; secondary contributions only when they strengthen or enable it.
3. **Claim–evidence ledger:** every abstract/introduction/conclusion claim mapped to exact method elements, experiments, figures/tables, and evidence status.
4. **Motivation–mechanism–evidence ledger:** every stated limitation mapped to a specific design response and a targeted test capable of verifying the proposed repair.
5. **Module contract:** for every claimed module, record its operation, claimed function, causal mechanism, controlled ablation, end-task delta, mechanism-specific diagnostic, qualitative evidence when scientifically meaningful, and confound controls.
6. **Novelty boundary:** closest prior art, known ingredients, precise technical delta, and the strongest novelty wording the literature supports.

Classify evidence as **Established**, **Partial**, **Missing**, **Contradicted**, or **Unclear**. Prose strength must not exceed evidence strength.

## Choose the story from evidence

- Identify the strongest result that is both technically meaningful and robustly supported.
- Define the paper's main arena: the task, regime, constraint, capability, mechanism, efficiency frontier, or insight where the contribution matters most.
- Trace the shortest valid chain: important problem → specific failure of closest approaches → technical insight → method → discriminating evidence → significance.
- Remove, demote, or reframe material that does not strengthen this chain.
- If the original story is not supported, rebuild it around the strongest valid contribution rather than defending a dead premise.
- Keep claims deliberately scoped. A narrower claim with decisive evidence is stronger than a universal claim with loopholes.

Strategic framing must never hide a result necessary to assess a central claim, misstate a comparison, cherry-pick without disclosure, or turn a failed hypothesis into a post-hoc causal claim.

## Design prose and experiments together

Do not treat experiments as a section appended after the method. For every central sentence that asserts an effect, ask what observation would make it true or false.

- Main results establish value in the claimed arena.
- Controlled ablations establish incremental utility.
- Mechanism-specific diagnostics test why a component works.
- Matched qualitative evidence reveals the claimed before/after failure repair when the mechanism is visual or structural.
- Robustness, generalization, fairness, efficiency, scalability, or interpretability claims require measurements that operationalize those concepts.
- Baseline comparisons must be fair in data, supervision, scale, pretraining, compute, tuning, and test-time access, or disclose and analyze the mismatch.

An end-task gain alone does not prove a mechanism. If decisive evidence is missing, present the user with the smallest discriminating experiment, or narrow the claim; never fill the gap with confident language.

## Draft in evidence-first order

Unless the project or user requires another order, draft:

1. Method
2. Experiments
3. Abstract
4. Introduction
5. Related Work
6. Conclusion and limitations

This order follows ResearchPilot's writing-stage logic: stabilize what was built and what the results prove before composing the paper's headline story. Use `section-playbook.md` for section-specific execution.

## Revise globally, edit locally

- Read the full current manuscript before changing a section.
- Preserve the user's terminology and style unless inconsistency or venue requirements justify a change.
- Detect structural implications: a changed contribution may require synchronized edits to the title, abstract, introduction, method overview, experiments, conclusion, figures, and supplement.
- Keep figure/table numbering, equation symbols, acronyms, citations, and cross-references consistent.
- When a project is version-controlled, preserve recoverability with Git; otherwise create a timestamped backup before substantial edits.
- Never overwrite unrelated user changes.

## Finalize only after the reviewer gate

Run `reviewer-gate.md` and repair decision-driving gaps before declaring the paper ready. The final pass must confirm:

- one memorable, technically accurate contribution story;
- complete motivation–method–evidence coverage;
- complete module-effect coverage for every claimed function;
- claim intensity calibrated to evidence;
- novelty wording supported by verified primary literature;
- real numbers and reproducible comparisons;
- coherent reverse outline and paragraph-level information flow;
- firm, specific academic English without defensive or generic AI phrasing;
- honest, tightly scoped limitations that do not attack the work on the reviewer's behalf.

If a core claim remains unsupported, do not certify submission readiness. State the exact blocker and the smallest path to resolution.
