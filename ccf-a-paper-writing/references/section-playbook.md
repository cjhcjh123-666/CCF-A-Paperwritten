# Section playbook

Use this playbook to draft or revise individual sections. Follow the venue's form and the paper's evidence architecture; the structures below are reasoning patterns, not rigid paragraph counts.

## Global paragraph contract

Every paragraph should have:

1. **Job:** one purpose in the paper's argument.
2. **Topic sentence:** the claim or relationship the paragraph establishes.
3. **Support:** technical explanation, evidence, citation, or comparison.
4. **Interpretation:** why the support matters to the paper thesis.
5. **Transition:** only when the next logical move is not already obvious.

If a paragraph performs several unrelated jobs, split it. If it has no support or no consequence, revise or remove it. Do not add transitions to conceal a broken argument.

## Title

The title should identify the distinctive technical idea or capability and the target problem. Prefer searchable technical nouns over slogans. Avoid unsupported priority, universality, or superlatives.

Check that a reader seeing only the title would expect the paper actually delivered by the experiments.

## Abstract

Write the abstract only after Method and Experiments are stable. It must establish:

1. the important technical problem and setting;
2. the precise limitation preventing existing approaches from succeeding;
3. the paper's key insight;
4. the method at the level needed to understand the contribution;
5. the strongest verified result or capability, with exact numbers when meaningful and venue-appropriate;
6. the scientific or practical significance.

Every factual performance or mechanism claim must appear in the claim–evidence ledger. Do not cite work unless the venue convention requires it. Avoid background surveys, implementation detail, undefined acronyms, vague “extensive experiments,” and claims broader than evaluated conditions.

Run an abstract entailment test: for every sentence, point to the exact section, table, figure, theorem, or cited source that makes it true.

## Introduction

Build a causal argument rather than a history lesson:

1. **Problem and stakes:** define the task and why the community should care.
2. **Specific gap:** show what closest approaches fail to capture, under which conditions, and why. Use evidence or citations; do not build a strawman.
3. **Technical insight:** state the observation that changes how the problem should be solved.
4. **Solution:** explain how the method operationalizes that insight.
5. **Evidence preview:** state the most decision-relevant result, mechanism finding, or trade-off.
6. **Contributions:** factual, non-overlapping, ordered by importance, each mapped to evidence.

The contribution list is a contract with the reviewer. Each item should say what was introduced or discovered and what evidence establishes its value. Do not list paper organization, code release plans, routine implementation, or generic “extensive evaluation” as contributions.

Introduction and Related Work must share the same gap definition. Introduction and Conclusion must share the same claim scope. Abstract, Introduction, and Experiments must use compatible result numbers and evaluation settings.

## Related Work

Organize by technical approach, assumption, or limitation—not by author chronology. A useful subsection performs four moves:

1. characterize the family of methods;
2. synthesize representative and closest works;
3. identify the precise boundary relevant to this paper;
4. locate the present work without dismissive or inflated language.

Discuss the closest prior work explicitly. Compare operation, objective, supervision, data flow, inference behavior, assumptions, and evaluated setting. Avoid laundry-list prose such as repeated “X et al. proposed ...” sentences.

Every citation must be verified and used for a proposition it actually supports. Prefer primary papers over surveys for specific method claims. Do not cite a paper from a search snippet alone.

## Method

Write from stable implementation and design artifacts. Recommended order:

1. problem formulation and assumptions;
2. overview and computational/data flow;
3. one subsection per meaningful component;
4. training objective and optimization;
5. inference procedure and complexity when relevant.

For every component, answer:

- **Role:** which diagnosed failure or requirement it addresses;
- **Operation:** inputs, outputs, transformations, shapes, and interaction with other components;
- **Mechanism:** why the operation should change the claimed intermediate phenomenon;
- **Advantage:** the exact technical difference from the closest alternative;
- **Evidence pointer:** where the module's utility and mechanism are tested.

Use a consistent local sequence: purpose/role → design and equation → variable definitions → mechanism explanation → relationship to prior alternatives → evidence pointer. The prose must match code and configuration.

For equations:

- define every symbol at first use;
- state dimensions or domains where ambiguity affects implementation;
- distinguish training-only and inference-time quantities;
- explain reductions, normalization, constraints, and optimization direction;
- ensure the surrounding prose adds interpretation rather than repeating notation.

Do not write “inspired by” as a substitute for identifying the borrowed operation and the paper's actual delta.

## Experiments

Organize experiments around scientific questions, not the chronological order in which runs completed.

### Experimental setup

State datasets and splits, baselines and selection rationale, metrics and direction, implementation details, hyperparameter/tuning protocol, pretraining/external data, compute/hardware, seeds, uncertainty, and statistical tests as relevant. Mark reproduced versus reported baseline values.

### Main results

Answer whether the method delivers the primary claimed value under the target conditions. For every result paragraph:

1. state the comparison and exact setting;
2. report the relevant numbers or trade-off;
3. interpret why the difference matters;
4. avoid mechanism claims unless a diagnostic establishes them.

Do not narrate every table cell. Lead with the comparison that proves the paper thesis, then discuss patterns, exceptions that affect the claim, and practical magnitude.

### Ablations

Each ablation should be a clean intervention. Report what changes, what is held constant, end-task effect with uncertainty, and confound controls. A combined “remove several components” row does not establish each component's contribution.

### Mechanism analysis

Measure the intermediate effect the method claims to create. A diagnostic should distinguish the proposed explanation from capacity, regularization, compute, or optimization effects. When the mechanism is visual/structural, use matched before/after cases on identical inputs and settings, along with an aggregate measurement and representative failures.

### Additional claims

Only add robustness, generalization, efficiency, scalability, fairness, or interpretability sections when the paper makes those claims or the venue/field makes them necessary. Use claim-appropriate protocols rather than decorative breadth.

## Figures, tables, and captions

Each visual must have one principal argumentative job. Use real result sources and preserve uncertainty. A self-contained caption should state:

- what is compared;
- dataset/setting and important conditions;
- metric and whether higher/lower is better;
- error bars or aggregation convention;
- abbreviations and visual encodings;
- the conclusion supported, without overstating causality.

Use accessible colors, readable text at final size, consistent method names, and fair axes. Mark unavailable or timed-out values rather than silently dropping them. Do not bold the proposed method merely because it is the proposed method; use emphasis consistently according to the stated rule.

## Conclusion and limitations

The conclusion should reinforce the verified memory point:

1. problem and insight;
2. method contribution;
3. strongest evidence;
4. significance within the tested scope.

Add no new method, result, or citation-dependent claim. State limitations when scientifically material or required, but keep them factual, scoped, and connected to assumptions or evaluated regimes. Do not turn the final paragraph into a speculative self-rejection. Future work should follow from a real boundary, not a generic wish list.

## Compression

When shortening:

1. remove repetition and process history;
2. compress generic background;
3. consolidate results that serve the same claim;
4. move non-decision-critical detail to the supplement when allowed;
5. retain definitions, assumptions, decisive comparisons, uncertainty, and claim evidence;
6. re-run the reverse outline and cross-reference checks.

Never meet a page limit by deleting qualifications that make a claim accurate.
