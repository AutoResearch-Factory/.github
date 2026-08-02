# AutoResearch Factory

### Human steers, machine scales

[![Project page](https://img.shields.io/badge/project-page-1f6feb.svg)](https://haizhaoyang.github.io/research/autoresearch.html)
[![arXiv](https://img.shields.io/badge/arXiv-2606.24177-b31b1b.svg)](https://arxiv.org/abs/2606.24177)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-plugin-8A2BE2.svg)](https://claude.com/claude-code)

We build autonomous research systems that take a project from a one-line topic to running experiments, with no human-written experimental code. Agents plan, implement, audit and review each other in closed loops, and every handoff goes through a file on disk — so a run is recoverable, auditable, and reusable across projects. The workflow stays minimal and explicit: `topic → idea → proposal → experiment`.

Everything here is built on [**Prompt Economy**](https://arxiv.org/abs/2606.08878): treat prompt engineering as engineering, and minimize the engineering effort it demands from humans.

![Agon workflow](https://raw.githubusercontent.com/AutoResearch-Factory/Agon/main/figures/figure_xp.png)

## Projects

| | |
|---|---|
| [**Agon**](https://github.com/AutoResearch-Factory/Agon) | The core system. A Claude Code plugin for autonomous AI research, deployed across more than ten research domains. |
| [**agon-artifacts**](https://github.com/AutoResearch-Factory/agon-artifacts) | Example data workspace for Agon — topics, ideas, proposals, and experiment workspaces. |
| [**AgonSR**](https://github.com/AutoResearch-Factory/AgonSR) | Automated symbolic regression: a Claude Code plugin for symbolic ansatz search. |
| [**AgonAlpha**](https://github.com/AutoResearch-Factory/AgonAlpha) | Agent-based framework for automated alpha discovery. |
| [**AgonReproduce**](https://github.com/AutoResearch-Factory/AgonReproduce) | Prompt-first auditing of research claims: literature investigation, direct reproduction, and independent review in one traceable workflow. |

## Quick start

Clone the plugin and an artifacts workspace side by side, then run Claude Code from the workspace:

```
git clone https://github.com/AutoResearch-Factory/Agon.git
git clone https://github.com/AutoResearch-Factory/agon-artifacts.git

cd agon-artifacts
claude --plugin-dir ../Agon --dangerously-skip-permissions --model claude-sonnet-5[1m]
```

Then drive the research forward with `/idea-tick`, `/proposal-tick`, `/experiment-tick`, and `/deep-lit-tick`. See the [Agon README](https://github.com/AutoResearch-Factory/Agon) for details.

## Paper

[**Agon: An Autonomous Large-Scale Omnidisciplinary Research System Built on Prompt Economy**](https://arxiv.org/abs/2606.24177)<br>
Youran Sun, Xingyu Ren, Chugang Yi, Jiaxuan Guo, Kejia Zhang, Jianda Du, Haizhao Yang<br>
[arXiv](https://arxiv.org/abs/2606.24177) · [Project page](https://haizhaoyang.github.io/research/autoresearch.html)
