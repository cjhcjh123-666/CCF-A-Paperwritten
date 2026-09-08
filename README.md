# CCF-A Paper Writing

`ccf-a-paper-writing` is a Codex Skill for turning research assets into a persuasive, evidence-aligned AI/ML paper at a CCF-A-caliber standard.

It combines three engines:

1. [ResearchPilot-Skills](https://github.com/LMDHQ-0420/ResearchPilot-Skills): staged research-to-writing discipline and the evidence-first writing order.
2. [anti-defensive-writing-Skill](https://github.com/Adkid-Zephyr/anti-defensive-writing-Skill): the press-release principle—build the paper around its strongest defensible value instead of writing a project log or attacking the work in advance.
3. [CCF-A-PaperReview](https://github.com/cjhcjh123-666/CCF-A-PaperReview): invert strict reviewer checks into writing-time requirements so every motivation, module claim, and experiment closes the loop before submission.

The result is not a prompt that merely “polishes English.” It treats paper writing as research argument engineering:

> important problem → precise gap → technical insight → method mechanism → discriminating evidence → scoped significance

## What it does

- reconstructs the source of truth from manuscript, code, configs, logs, results, figures, and bibliography;
- selects one primary, evidence-backed contribution story;
- builds claim–evidence, motivation–mechanism–evidence, module-effect, and novelty ledgers;
- plans sections and visuals around scientific questions;
- drafts in the evidence-first order Method → Experiments → Abstract → Introduction → Related Work → Conclusion;
- writes strategic but honest academic English without defensive or generic AI prose;
- verifies citations, result numbers, comparison fairness, equations, and cross-references;
- runs a reviewer-resistance gate before declaring submission readiness;
- supports full-paper drafting, section writing, revision, compression, and reviewer-driven repair.

## Install

Install the `ccf-a-paper-writing` directory as a Codex Skill:

```text
https://github.com/cjhcjh123-666/CCF-A-Paperwritten/tree/main/ccf-a-paper-writing
```

Or copy `ccf-a-paper-writing/` into your Codex skills directory.

The Skill is self-contained. For the richest workflow, also install ResearchPilot and anti-defensive-writing; when available, it explicitly coordinates with `$research`, `$anti-defensive-writing`, and `$ccf-a-paper-review`.

## Use

Full manuscript:

```text
Use $ccf-a-paper-writing to turn my code, results, research notes, and draft into a CCF-A-caliber paper in professional academic English. Build the evidence architecture first and do not invent missing results or citations.
```

One section:

```text
Use $ccf-a-paper-writing to rewrite the Introduction around the strongest supported contribution. Keep every motivation aligned with a specific method design and experiment.
```

Pre-submission repair:

```text
Use $ccf-a-paper-writing to run the reviewer-resistance gate on this manuscript, repair all decision-driving claim–evidence gaps, and preserve a confident but scientifically honest narrative.
```

## Design principles

- **Evidence before rhetoric.** Prose strength never exceeds evidence strength.
- **One winning arena.** The manuscript competes where its contribution is meaningful and fairly supported.
- **Mechanisms need diagnostics.** End-task improvement establishes utility, not automatically why a module works.
- **Strategic is not deceptive.** The Skill never hides material counter-evidence or cherry-picks results.
- **Review starts during writing.** Strict reviewer criteria become design constraints, not a last-minute checklist.
- **Templates serve content.** Section length and structure follow the contribution and venue, not fixed paragraph counts.

## Repository layout

```text
ccf-a-paper-writing/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── narrative-strategy.md
    ├── reviewer-gate.md
    ├── section-playbook.md
    ├── third-party-notices.md
    └── workflow.md
```

## Attribution

This project is an original synthesis that adapts workflow concepts from ResearchPilot-Skills and narrative principles from anti-defensive-writing-Skill, both under the MIT License. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## 中文简介

这是一个面向 AI、机器学习及相邻技术领域的 CCF-A 级论文写作 Skill。它不是单纯润色英文，而是先从代码、实验结果和文献中建立证据结构，再选择最强且真正成立的论文主线；同时把严苛审稿标准前置，使每个 motivation、方法模块、机制解释和实验都一一对应。最终目标是写出自信、清晰、有说服力，但不隐瞒重要证据、不捏造结果和引用的专业英文学术论文。
