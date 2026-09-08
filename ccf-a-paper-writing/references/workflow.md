# Evidence-first manuscript workflow

This workflow adapts ResearchPilot's staged research-to-writing discipline for a portable, single-skill paper-writing process.

## 1. Intake and state reconstruction

Determine which artifacts exist and what can be trusted. Search common locations, but adapt to the project:

- `docs/user_requirements.md` or equivalent author/venue constraints;
- `docs/idea_report.md`, research notes, hypotheses, and related-work matrices;
- `docs/implementation.md`, source code, configs, and model definitions;
- `docs/dev_log.md`, `results/`, experiment trackers, exported CSV/JSON, and logs;
- `docs/manuscripts/`, `.tex`, `.bib`, `.md`, figures, tables, and supplements;
- reviews, rebuttals, and author annotations.

Do not assume the manuscript or design document reflects the current implementation. Compare method descriptions, code, configs, result artifacts, and experiment naming. Produce a conflict list such as:

| Item | Manuscript/design says | Code/result says | Source of truth | Required repair |
|---|---|---|---|---|

Resolve decision-relevant conflicts before drafting. Cosmetic conflicts can be queued.

## 2. Respect user and venue constraints

Read user requirements before defaults. Establish:

- target venue and official current format/length/review criteria;
- paper language and output format;
- anonymity, supplementary, artifact, ethics, and reproducibility requirements;
- requested scope and deadline;
- provided style exemplars.

If the venue is known, verify current instructions from the official venue source. Do not rely on remembered page limits or old rating forms.

When exemplars are supplied, extract section proportions, paragraph rhythm, terminology density, figure/table usage, and caption style. Match structural and stylistic traits without copying phrasing or scientific content.

## 3. Build the evidence architecture

Create six linked artifacts before full drafting.

### 3.1 Paper thesis

Use this semantic form, not necessarily this sentence template:

> For [important problem/setting], we identify [specific limitation], introduce [technical insight and method], and demonstrate [strongest supported advantage] through [decisive evidence].

Test the thesis:

- Is the problem important to the target community?
- Is the limitation specific, evidenced, and not a strawman?
- Does the method contain the promised response?
- Does the evidence directly establish the stated advantage?
- Is the scope no broader than the evaluated setting?

### 3.2 Contribution hierarchy

Choose one primary contribution. A secondary contribution belongs only if it:

- enables the primary result;
- explains its mechanism;
- establishes generality or practical value; or
- provides a distinct, verified scientific insight.

Do not list implementation steps as equal contributions. Do not use “novel,” “first,” “significant,” or “comprehensive” as substitutes for a factual technical delta.

### 3.3 Claim–evidence ledger

| Claim ID | Candidate claim | Importance | Method locus | Evidence locus | Alternative explanation controlled? | Status | Allowed wording |
|---|---|---|---|---|---|---|---|

The ledger is authoritative for the abstract, introduction contribution list, experiment takeaways, and conclusion. When any of those sections changes a claim, update every occurrence.

### 3.4 Motivation–mechanism–evidence ledger

| Motivation ID | Demonstrated failure | Closest approaches affected | Design response | Mechanism hypothesis | Targeted diagnostic | Status |
|---|---|---|---|---|---|---|

An asserted limitation with no observed or cited evidence cannot carry the central story. A design that does not specifically answer the diagnosed failure cannot be justified by proximity in prose.

### 3.5 Module contract

| Module | Operation | Claimed function | Clean intervention | End metric | Mechanism diagnostic | Matched qualitative evidence | Confounds | Status |
|---|---|---|---|---|---|---|---|---|

Require matched qualitative evidence only when it can reveal the claimed phenomenon. Do not add decorative attention maps or embeddings that lack a validated interpretation.

### 3.6 Novelty boundary

| Claimed contribution | Closest prior work | Shared ingredients | Exact delta | Why delta matters | Evidence for delta | Defensible novelty wording |
|---|---|---|---|---|---|---|

Verify important citations and priority using original papers, official proceedings, arXiv version histories, OpenReview, or publisher pages. “Not found” does not prove “first.”

## 4. Plan sections and figures

Create a manuscript architecture containing:

- semantic section/subsection titles;
- the single job of every section and paragraph group;
- claims introduced, explained, or verified there;
- figure/table placement and the exact conclusion each visual must support;
- expected page/word budget based on contribution importance;
- cross-section dependencies.

For each visual, plan:

| ID | Location | Scientific question | Data source | Comparison | Reader takeaway | Claim supported |
|---|---|---|---|---|---|---|

One visual should have one primary conclusion. Captions must be self-contained and state setup, metric/direction, relevant conditions, uncertainty convention, and takeaway. Figures and tables must read real result artifacts; never type invented placeholder numbers into manuscript-ready output.

## 5. Draft in dependency order

Use the default ResearchPilot sequence:

1. **Method:** stabilize what exists, its role, and its mechanism.
2. **Experiments:** stabilize what the evidence proves and under which conditions.
3. **Abstract:** advertise only claims already secured by Method and Experiments.
4. **Introduction:** lead the reader from important problem through precise gap and insight to contributions.
5. **Related Work:** define the intellectual neighborhood and exact differentiation.
6. **Conclusion:** reinforce the verified memory point; add no new scientific claim.

Individual section requests may start elsewhere, but still consult upstream evidence. For example, do not write an abstract without checking method/results, or related work without verifying sources.

## 6. Revision loop

For each substantial revision:

1. read the full manuscript and relevant evidence;
2. identify the target outcome, affected claims, and cross-section consequences;
3. create a recoverable checkpoint;
4. revise the smallest coherent set of locations;
5. update ledgers and architecture;
6. check references, numbers, symbols, figures, and cross-references;
7. run the reviewer gate for affected claims;
8. summarize what changed and what remains unsupported.

When reviewer feedback exposes a structural problem, do not patch one sentence. Trace the affected claim through motivation, method, experiment, and conclusion, then repair the full chain.

## 7. Decision rules for insufficient material

- **Missing implementation detail:** inspect code/config; otherwise mark and ask rather than invent.
- **Missing result:** propose the smallest decisive experiment or use explicitly labeled placeholders in a planning artifact, never in submission-ready prose.
- **Weak central result:** search for a better supported capability, regime, mechanism, or trade-off; otherwise narrow the claim.
- **Contradictory result:** investigate protocol and uncertainty; if valid, disclose and scope the claim rather than hide it.
- **Missing citation:** verify it on the web; if unverifiable, omit or mark outside manuscript text for author action.
- **No substantive novelty:** do not manufacture it with naming. Reframe around a verified combination, analysis, benchmark, negative result, or practical capability only if scientifically meaningful.
