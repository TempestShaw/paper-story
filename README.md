# Paper Story

**Build research arguments from claims, evidence, and decisive experiments.**

[繁體中文](README.zh-TW.md) · [Skill](skills/paper-story/SKILL.md) · [Six lenses](skills/paper-story/references/archetypes.md) · [Examples](examples/diagnosis.md) · [Provenance](skills/paper-story/references/sources.md)

Paper Story is an Agent Skill for research positioning, experiment design, academic writing, and reviewer responses. Give it an idea, observations, an experiment table, or a manuscript. It helps identify what you can claim, what remains uncertain, and what evidence would change the conclusion.

It organizes work into five modes and six optional narrative lenses. The central artifact is a **claim–evidence ledger** connecting each contribution to its scope, source, strongest alternative explanation, and next action.

## Quick start

With Node.js/npm and Git available, install through the [Skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add TempestShaw/paper-story --skill paper-story
```

The installer lets you choose a supported agent and installation scope. For a manual installation, copy the complete `skills/paper-story` directory into your client's documented skills directory. Keep `references/`, `assets/`, and `agents/` alongside `SKILL.md`.

Invoke the skill using your client's syntax. For clients supporting `$skill-name`:

```text
Use $paper-story in diagnose mode.
Here are my research question, current results, closest related work, and budget.
Identify the strongest defensible claim, the main alternative explanation,
and the smallest experiment that could change our conclusion.
```

The package follows the [Agent Skills format](https://agentskills.io/specification). It contains Markdown instructions, templates, and optional UI metadata; it has no runtime code, required API key, or automatic experiment execution. Browsing is useful for checking literature and current venue rules. With no browsing, the skill works from supplied material and flags verification gaps. Client-specific installation behavior should be checked in that client's documentation.

## Five modes

| Mode | Typical request | Main output |
| --- | --- | --- |
| `diagnose` | “What is the real contribution of this project?” | Bounded thesis, framing choice, rival explanation, decisive next step |
| `design` | “What experiments would support this claim?” | Evidence ledger and prioritized experiment map |
| `draft` | “Write the abstract or restructure the introduction.” | Requested text with evidence-based claims and visible missing-result placeholders |
| `review` | “Read this as a skeptical reviewer.” | Localized objections, consequences, smallest repairs, honest fallback claims |
| `rebuttal` | “Respond to these reviews.” | Responses distinguishing existing results, completed additions, plans, and concessions |

You can ask in English or Chinese. Explanations follow your language; manuscript text retains its language unless you request translation. A narrow edit stays narrow.

## Six narrative lenses

| Lens | What makes it credible |
| --- | --- |
| **Root-cause diagnosis** | A mechanism is separated from competing explanations through appropriate evidence. |
| **Assumption revision** | A documented assumption fails in a defined regime under a fair comparison. |
| **Theory explaining behavior** | Explicit assumptions and a valid result support a bounded explanation or prediction. |
| **Evaluation exposing a blind spot** | A valid measurement reveals an important capability gap missed by existing evaluation. |
| **Real-world impact** | Relevant stakeholder outcomes and operational constraints are actually examined. |
| **Unifying abstraction** | A shared representation yields useful mappings, simplification, or new consequences. |

The skill chooses one primary lens and at most one supporting lens, or none. It also supports replication, negative results, descriptive studies, and incremental contributions. These lenses are practical heuristics; this repository does not estimate acceptance probabilities or promise awards.

Each lens has a decision guide: when it applies, an argument skeleton, minimum evidence, a falsifier, a useful figure, a common overclaim, and a narrower claim to use when support is incomplete.

## A small example

**Fictional input:** A document-processing agent improves success from 52/100 to 78/100 on compound tasks after adding named intermediate artifacts, a validator, and three times the inference tokens. Only one training seed was tried.

**Useful diagnosis:** The reported comparison supports investigating the combined intervention. It does not isolate ambiguous intermediate references as the root cause. Match the token budget and separate representation changes from validation before making a mechanism claim. The difference is **26 percentage points** on this sample; its reliability and attribution remain unresolved.

See the [worked diagnosis](examples/diagnosis.md) and [abstract with missing results](examples/abstract-before-results.md). All example projects and numbers are fictional.

## What it produces

| Resource | Purpose |
| --- | --- |
| [Research brief](skills/paper-story/assets/paper-brief.md) | Align the research question, thesis, closest work, scope, and next decision. |
| [Claim–evidence ledger](skills/paper-story/assets/claim-evidence-ledger.md) | Track VERIFIED, REPORTED, HYPOTHESIS, PLANNED, CONTRADICTED, and UNKNOWN claims. |
| [Experiment map](skills/paper-story/assets/experiment-map.md) | Connect each test to a claim, rival explanation, control, budget, metric, and falsifier. |
| [Review and rebuttal worksheet](skills/paper-story/assets/review-and-rebuttal.md) | Ground objections and responses in actual passages and completed work. |

VERIFIED means that an inspected artifact supports the bounded assertion. It is not a claim of universal validity or independent reproduction. Templates are used selectively, according to the task.

## Working principles

- Separate observations, explanations, interventions, and plans.
- Match each claim's strength to its evidence and limitations.
- Preserve negative findings, uncertainty, units, denominators, and comparison budgets.
- Treat novelty as a literature question and a metric as something that needs validation.
- Draft useful text even before experiments finish, with explicit placeholders.
- Propose the smallest decision-changing test; respect compute and time constraints.
- Never invent citations, results, proofs, review comments, or completed work.

The research-reporting references include the [NeurIPS checklist](https://neurips.cc/public/guides/PaperChecklist), [Pineau et al. on reproducibility](https://jmlr.org/papers/v22/20-303.html), and [Dodge et al. on experimental reporting](https://aclanthology.org/D19-1224/). The full [source note](skills/paper-story/references/sources.md) distinguishes methodological reading from this repository's own heuristics.

## Validation and limitations

See [evaluation cases](evals/README.md) and the [initial validation record](evals/validation.md). These checks assess format and behavior on synthetic tasks. They do not establish scientific correctness, client-wide compatibility, or an effect on publication outcomes. Verify generated citations, analyses, and manuscript claims before using them.

## Inspiration and attribution

Inspired by user-supplied text titled “Story Is All You Need：扒透35篇顶会最佳/杰出论文的叙事密码，我们找到了六大范式”, attributed to 人工智能学社. The original article URL and publication date were not independently verified. Selected award labels were checked against official records; the full set of 35 technical summaries was not audited.

This repository contributes an original workflow, decision rules, templates, and fictional examples. It does not redistribute the article or paper figures. See [provenance](skills/paper-story/references/sources.md) for the exact scope of verification.

## Contributing and license

Contributions that improve evidence calibration, task coverage, examples, or concise instructions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

[MIT License](LICENSE), copyright © 2026 Victor Kwong. The license covers original repository files; linked third-party works retain their own rights and licenses.
