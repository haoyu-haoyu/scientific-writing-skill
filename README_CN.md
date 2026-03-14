# Scientific Writing Skill — Claude Code 学术写作技能

一个面向 [Claude Code](https://claude.ai/claude-code) 的综合学术写作技能插件，能够分析、审稿、重构和润色面向任何主流学术会议/期刊的科学论文——从 Nature、Science 到 IEEE、NeurIPS、AMIA 等。

> **[English Version / 英文版说明](README.md)**

## 功能特色

### 覆盖 12 个 Venue 家族

| Venue 家族 | 代表刊物/会议 |
|---|---|
| 综合顶刊 | Nature, Science, Cell |
| 医学期刊 | Lancet, NEJM, BMJ |
| IEEE | TPAMI, TMI, JBHI, EMBC, BHI |
| ACM | CHI, KDD, CSCW, SIGMOD |
| ML 顶会 | NeurIPS, ICML, ICLR, AAAI |
| 健康信息学 | AMIA, CHIL, MLHC, ML4H, ICHI, MedInfo |
| 出版社 | Elsevier, Springer/LNCS |

### 七种任务模式

| 命令 | 功能 |
|---|---|
| `review` | 结构化审稿反馈（不改写原文） |
| `polish` | 句子级别的清晰度和精确度提升 |
| `restructure` | 重新组织章节，优化逻辑流 |
| `rewrite` | 大幅重写某个章节 |
| `adapt` | 在不同 venue 的写作规范之间转换 |
| `outline` | 从零开始规划论文结构 |
| `check` | 检查是否符合目标 venue 的格式要求 |

### 知识库内容

- **Venue 规范**：12 个 venue 家族的精确字数限制、摘要格式、Methods 放置位置、标题风格、贡献列表规则、引用格式
- **写作原则**：Swales CARS 模型、已知到未知信息流、Hedging 校准连续谱、六种核心科学句式、段落架构
- **常见错误**：期刊编辑统计的拒稿原因、句子级错误模式、学术写作的"致命错误"
- **AI 痕迹检测**：AI 生成文本的高频词汇黑名单和结构性标记

## 安装方法

### 方式一：作为 Claude Code Skill 安装（推荐）

将文件复制到 Claude Code 的 skills 目录：

```bash
mkdir -p ~/.claude/skills/scientific-writing/references
cp SKILL.md ~/.claude/skills/scientific-writing/
cp references/*.md ~/.claude/skills/scientific-writing/references/
```

重启 Claude Code 后自动识别。

### 方式二：作为 Claude Code Command 安装

```bash
cp SKILL.md ~/.claude/commands/scientific-writing.md
```

注意：此方式不包含参考文件，推荐使用 Skill 方式以获得完整功能。

## 使用方法

安装后，在 Claude Code 中调用：

```
/scientific-writing review my introduction for MLHC
/scientific-writing polish this paragraph for Nature
/scientific-writing adapt this section from IEEE to Lancet format
/scientific-writing check compliance with CHIL 2026 requirements
/scientific-writing outline a full paper for NeurIPS
/scientific-writing rewrite this discussion section
```

也可以直接粘贴文本：

```
/scientific-writing review this for AMIA: [在此粘贴你的文本]
```

## 文件结构

```
scientific-writing-skill/
├── README.md                          # 英文说明
├── README_CN.md                       # 中文说明（本文件）
├── SKILL.md                           # 主技能定义
└── references/
    ├── venue-conventions.md           # 12 个 venue 家族的详细规范
    └── writing-principles.md          # 通用学术写作原则与参考
```

### SKILL.md
主技能定义文件。包含分析框架、任务类型、venue 感知的审稿流程和输出格式。自动处理 venue 识别、章节类型判断，并应用对应的写作规范。

### references/venue-conventions.md
全面的 venue 规范参考，涵盖：
- 各 venue 的摘要格式与字数限制
- Methods 章节放置惯例
- 标题风格规范
- 贡献列表要求
- 引用格式（编号制 vs. 作者-年份制）
- 跨 venue 对比表格

### references/writing-principles.md
通用学术写作工具箱：
- 六种核心科学句式（背景句、缺口句、动作句、设计句、结果句、边界句）
- 已知到未知信息流原则
- Hedging 校准连续谱（从 "might possibly" 到 "demonstrates" 的 7 级体系）
- 主动/被动语态决策指南
- 精确性与简洁性替换表
- 各章节时态速查表
- 常见错误及修复方法
- AI 生成文本词汇黑名单
- 跨学科语域差异（CS vs. 临床 vs. 自然科学）
- Swales CARS 引言模型

## Venue 快速参考

### Methods 放置位置
- **论文末尾：** Nature, Science, Cell
- **Introduction 之后（IMRAD）：** Lancet, NEJM, BMJ
- **第 2-3 节（显著位置）：** IEEE, ACM, NeurIPS, ICML, ICLR, AMIA, CHIL, MLHC

### 贡献列表（Contribution List）
- **从不使用：** Nature, Science, Cell, Lancet, NEJM, BMJ
- **必须有：** IEEE, ACM, NeurIPS, ICML, ICLR, AAAI
- **建议有：** AMIA, CHIL, MLHC, Elsevier, Springer

### 摘要格式
- **非结构化（~125-150 词）：** Nature, Science, Cell
- **非结构化（~150-250 词）：** IEEE, ACM, NeurIPS, ICML
- **结构化（~250-300 词）：** Lancet, NEJM, BMJ

## 理论基础

本技能综合了以下来源的写作规范和指南：

- **风格指南：** Strunk & White, Williams & Bizup ("Style"), Pinker ("The Sense of Style"), Glasman-Deal ("Science Research Writing"), Schimel ("Writing Science"), Sword ("Stylish Academic Writing")
- **基础研究：** Swales CARS 模型 (1990), Gopen & Swan (1990), Hyland 的 hedging 分类体系 (1998)
- **期刊/会议投稿指南：** Nature, Science, Cell, Lancet, NEJM, BMJ, IEEE, ACM, NeurIPS, ICML, ICLR, AAAI, AMIA, CHIL, MLHC, ML4H, BHI, ICHI, MedInfo, Elsevier, Springer
- **编辑评述与元分析：** 常见拒稿原因、写作质量标准、AI 文本检测模式 (Liang et al., 2024)

## 许可证

MIT
