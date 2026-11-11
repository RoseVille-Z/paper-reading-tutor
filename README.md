# Paper Reading Tutor

An agent skill for interactive, equation-by-equation research paper tutoring.

用中文陪读论文：解释每个符号与公式的来源，展开中间推导，补足当前需要的前置知识，并根据学习者的回答继续推进。适合 PINN、控制、机器人与动力学等包含数学推导的论文。

## Features

- 保留论文的公式编号、记号、页码和假设，区分原文事实、辅助推导与待核对项。
- 逐项解释变量类型、矩阵形状、单位、坐标系、元素和正负号。
- 一轮聚焦一个核心公式及必要关联式，讲清后给一两个检查问题，等待回答。
- 根据本人实际解释、推导或代码证据判断理解程度；笔记整理按用户需要进行。

## Installation

下载本仓库 ZIP 并解压，将文件夹重命名为 `paper-reading-tutor`，放到目标项目的 `.agents/skills/` 目录。安装后应有：

```text
.agents/skills/paper-reading-tutor/
├── SKILL.md
├── agents/openai.yaml
├── references/provenance.md
├── README.md
└── LICENSE
```

本包提供 `SKILL.md` 和 Codex 界面元数据。其他宿主的发现方式以其技能机制为准。

## Usage

先提供可读取的论文或明确的原文位置，然后调用：

```text
使用 $paper-reading-tutor，从论文式（11）开始精读。
先补必要前置，每个符号和中间步骤都解释清楚，讲完后检查我的理解。
```

默认使用简体中文讲解。也可以要求只解释一个符号、核对自己的推导，或整理已经读过的范围。论文 PDF、学习者资料和项目笔记不随技能分发。

## Sources and License

来源及独立撰写范围见 [Source Notes](references/provenance.md)。本项目采用 [MIT License](LICENSE)。
