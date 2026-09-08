# Reviewer-resistance gate

This gate converts the CCF-A Paper Review protocol into pre-submission writing constraints. It is not a request to invent criticism. Its purpose is to ensure that the paper's own claims survive a strict, evidence-bound reading.

## 1. Contribution entailment

Extract every contribution claim from the title, abstract, introduction, captions, experiment takeaways, and conclusion. For each, verify:

| Claim | Exact occurrences | Method support | Quantitative evidence | Mechanism evidence | Qualitative evidence if relevant | Prior-art boundary | Status |
|---|---|---|---|---|---|---|---|

Required repairs:

- **Contradicted:** fix the factual inconsistency or remove/reconstruct the claim.
- **Missing:** add decisive evidence or remove the claim.
- **Partial:** narrow the quantifier, setting, causal language, or significance statement.
- **Unclear:** clarify method, protocol, or scope until the claim can be evaluated.
- **Established:** preserve consistent wording across all occurrences.

No abstract or conclusion claim may be stronger than the detailed evidence section.

## 2. Motivation–method–evidence closure

For every motivation:

1. locate evidence that the diagnosed failure exists;
2. identify the exact method design that responds to it;
3. articulate a plausible causal pathway;
4. identify a targeted test measuring the failure before and after;
5. check alternative explanations and scope.

Flag:

- rhetorical motivation with no corresponding design;
- design component with no scientific purpose;
- benchmark gain used as the only evidence for a failure-repair story;
- motivation stated universally but tested in one narrow regime;
- gap definition inconsistent across Introduction and Related Work.

Repair the chain, not merely the sentence.

## 3. Module-effect closure

For each module-level function claim, require:

- clean with/without or replacement intervention;
- end-task delta with appropriate uncertainty;
- direct diagnostic of the claimed intermediate effect;
- matched qualitative diagnosis when meaningful;
- parameter, compute, data, optimization, and test-time confound controls.

Use these verdicts:

- **Mechanism established:** utility and claimed internal effect are both supported.
- **Utility established:** ablation supports usefulness, but mechanism remains unproven; rewrite accordingly.
- **Inconclusive:** intervention is confounded or uncertainty dominates.
- **Refuted:** evidence conflicts with the claimed effect; reconstruct or remove it.

Do not let a multi-component ablation stand in for individual component evidence.

## 4. Experimental validity

Check decision-driving comparisons for:

- same data, split, preprocessing, external data, and supervision;
- comparable scale, pretraining, training/inference compute, and tuning budget;
- current, relevant, and closest baselines;
- no train/test leakage, oracle access, selective filtering, or unreported stopping rules;
- appropriate metrics and statistical treatment;
- isolated ablations;
- representative qualitative examples and failure cases;
- claims of robustness/generalization/efficiency/etc. tested under operational definitions.

State unavoidable mismatches and reduce the affected claim rather than hiding them.

## 5. Novelty and positioning

Decompose novelty into component, combination, application, theory/analysis, and empirical discovery. Search exact terminology and normalized mechanisms; compare operation, objective, information flow, supervision, and role. Verify original sources and earliest public dates.

For each novelty claim, choose:

- supported within the searched literature;
- novel combination or extension;
- incremental;
- not novel as stated;
- inconclusive.

Do not manufacture novelty with naming. Conversely, do not discard a meaningful contribution merely because individual ingredients are known.

## 6. Reproducibility and internal consistency

Trace:

- symbols and dimensions through equations;
- algorithm steps to implementation and configurations;
- training-only information versus inference-time access;
- reported hyperparameters to actual runs;
- table/figure values to result artifacts;
- citations to bibliography entries and source claims;
- acronyms, method names, dataset names, and metric direction throughout the paper;
- figure, table, equation, section, and appendix references.

Any ambiguity that changes implementation, validity, or interpretation is scientific—not merely stylistic—and must be repaired.

## 7. Reverse-outline test

Extract each paragraph's topic sentence and evidence. Verify:

- the paragraph evidence supports the topic sentence;
- the topic sentence advances the section job;
- the section job advances the paper thesis;
- neighboring paragraphs have an explicit logical relationship;
- no essential premise is deferred until after its consequence;
- no claim is repeated without adding evidence or interpretation.

Repair the argument before polishing transitions.

## 8. Decision-driving red team

Identify the two or three issues most likely to determine a strict review outcome. Assign:

- **Fatal:** invalidates the main result or interpretation;
- **Major:** undermines a central claim, novelty statement, or claimed advantage;
- **Moderate:** affects non-central generality, reproducibility, or evidence;
- **Minor:** localized clarification or presentation repair.

For each issue, specify:

1. claim and manuscript location;
2. observed evidence;
3. exact gap or contradiction;
4. consequence for the paper thesis;
5. smallest decisive repair;
6. all cross-section occurrences requiring synchronization.

Do not double-count one root cause. Do not downgrade a paper because the method is simple, fails to win an unclaimed metric, omits an unrelated experiment, or states an honest limitation.

## 9. Submission-readiness exit criteria

Declare the manuscript ready only when:

- all central claims are Established or deliberately narrowed to their evidence;
- every central motivation has a method response and targeted test;
- every claimed module function is supported or rewritten as utility only;
- closest-work differentiation is technically precise and citation-verified;
- decisive comparisons are fair and reproducible;
- all numbers, citations, equations, captions, and cross-references are verified;
- the reverse outline forms one coherent argument;
- no Fatal or unresolved central Major issue remains;
- narrative strategy is persuasive without concealing material evidence.

If the gate fails, output a prioritized repair plan. Do not certify readiness through stylistic polish alone.
