# AutoResearch Factory

### Human steers, machine scales

[![Project page](https://img.shields.io/badge/project-page-1f6feb.svg)](https://haizhaoyang.github.io/research/autoresearch.html)
[![arXiv](https://img.shields.io/badge/arXiv-2606.24177-b31b1b.svg)](https://arxiv.org/abs/2606.24177)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-plugin-8A2BE2.svg)](https://claude.com/claude-code)

[English](https://github.com/AutoResearch-Factory) | 中文

我们做自主科研系统: 把一个项目从一句话的课题一路推到跑起来的实验, 全程无人编写实验代码. 各个 agent 在闭环里互相规划, 实现, 审计和评审, 每一次交接都经由磁盘上的文件 —— 一次运行因此可恢复, 可审计, 也可跨项目复用. 流程保持最小且显式: `topic → idea → proposal → experiment`.

这里的一切都构建于 [**Prompt Economy**](https://arxiv.org/abs/2606.08878) 之上: 把 prompt engineering 当作工程问题, 并最小化它对人的工程投入.

![Agon workflow](https://raw.githubusercontent.com/AutoResearch-Factory/Agon/main/figures/figure_xp.png)

## 项目

| | |
|---|---|
| [**Agon**](https://github.com/AutoResearch-Factory/Agon) | 核心系统. 面向自主 AI 科研的 Claude Code 插件, 已在十余个研究领域部署. |
| [**agon-artifacts**](https://github.com/AutoResearch-Factory/agon-artifacts) | Agon 的示例数据 workspace —— topics, ideas, proposals 和 experiment workspaces. |
| [**AutoSR**](https://github.com/AutoResearch-Factory/AutoSR) | 自动符号回归: 用于符号 ansatz 搜索的 Claude Code 插件 ([论文](https://arxiv.org/abs/2608.16876)). |
| [**AgonAlpha**](https://github.com/AutoResearch-Factory/AgonAlpha) | 面向自动 alpha 发现的 agent 框架 ([论文](https://arxiv.org/abs/2608.11250)). |
| [**AgonReproduce**](https://github.com/AutoResearch-Factory/AgonReproduce) | prompt-first 的科研结论审计: 文献调查, 直接复现和独立评审, 收在一条可追溯的流程里. |

## 快速开始

把插件和一个 artifacts workspace 并排 clone 下来, 然后在 workspace 里启动 Claude Code:

```
git clone https://github.com/AutoResearch-Factory/Agon.git
git clone https://github.com/AutoResearch-Factory/agon-artifacts.git

cd agon-artifacts
claude --plugin-dir ../Agon --dangerously-skip-permissions --model claude-sonnet-5[1m]
```

然后用 `/idea-tick`, `/proposal-tick`, `/experiment-tick` 和 `/deep-lit-tick` 推进科研流程. 细节见 [Agon README](https://github.com/AutoResearch-Factory/Agon).

## 论文

[**Agon: An Autonomous Large-Scale Omnidisciplinary Research System Built on Prompt Economy**](https://arxiv.org/abs/2606.24177)<br>
Youran Sun, Xingyu Ren, Chugang Yi, Jiaxuan Guo, Kejia Zhang, Jianda Du, Haizhao Yang

[**AgonAlpha: Autonomous Alpha Discovery via Prompt Economy and Scalable Agentic Search**](https://arxiv.org/abs/2608.11250)<br>
Weicheng Ye, Youran Sun, Xingyu Ren, Shunyao Yu, Chugang Yi, Haizhao Yang

[**AutoSR: Automatic Symbolic Regression by Searching Research States**](https://arxiv.org/abs/2608.16876)<br>
Kejia Zhang, Youran Sun, Xinyu Ren, Chugang Yi, Haizhao Yang

[**PerspectiveGap: A Benchmark for Multi-Agent Orchestration Prompting**](https://arxiv.org/abs/2606.08878)<br>
Youran Sun, Xingyu Ren, Kejia Zhang, Xinpeng Liu, Jiaxuan Guo

## 引用

```bibtex
@misc{sun2026agonautonomouslargescaleomnidisciplinary,
      title={Agon: An Autonomous Large-Scale Omnidisciplinary Research System Built on Prompt Economy},
      author={Youran Sun and Xingyu Ren and Chugang Yi and Jiaxuan Guo and Kejia Zhang and Jianda Du and Haizhao Yang},
      year={2026},
      eprint={2606.24177},
      archivePrefix={arXiv},
      primaryClass={cs.SE},
      url={https://arxiv.org/abs/2606.24177},
}

@misc{ye2026agonalphaautonomousalphadiscovery,
      title={AgonAlpha: Autonomous Alpha Discovery via Prompt Economy and Scalable Agentic Search},
      author={Weicheng Ye and Youran Sun and Xingyu Ren and Shunyao Yu and Chugang Yi and Haizhao Yang},
      year={2026},
      eprint={2608.11250},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2608.11250},
}

@misc{zhang2026autosrautomaticsymbolicregression,
      title={AutoSR: Automatic Symbolic Regression by Searching Research States},
      author={Kejia Zhang and Youran Sun and Xinyu Ren and Chugang Yi and Haizhao Yang},
      year={2026},
      eprint={2608.16876},
      archivePrefix={arXiv},
      primaryClass={cs.SC},
      url={https://arxiv.org/abs/2608.16876},
}

@misc{sun2026perspectivegapbenchmarkmultiagentorchestration,
      title={PerspectiveGap: A Benchmark for Multi-Agent Orchestration Prompting},
      author={Youran Sun and Xingyu Ren and Kejia Zhang and Xinpeng Liu and Jiaxuan Guo},
      year={2026},
      eprint={2606.08878},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2606.08878},
}
```
