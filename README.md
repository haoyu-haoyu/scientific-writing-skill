# Scientific Writing Skill for Claude Code

A comprehensive [Claude Code](https://claude.ai/claude-code) skill that analyzes, critiques, restructures, and polishes scientific manuscripts for any major academic venue — from Nature and Science to IEEE, NeurIPS, AMIA, and beyond.

## Features

### Multi-Venue Coverage (12 venue families)

| Venue Family | Examples |
|---|---|
| General Science | Nature, Science, Cell |
| Medical Journals | Lancet, NEJM, BMJ |
| IEEE | TPAMI, TMI, JBHI, EMBC, BHI |
| ACM | CHI, KDD, CSCW, SIGMOD |
| ML Conferences | NeurIPS, ICML, ICLR, AAAI |
| Health Informatics | AMIA, CHIL, MLHC, ML4H, ICHI, MedInfo |
| Publishers | Elsevier, Springer/LNCS |

### Seven Task Types

| Command | What It Does |
|---|---|
| `review` | Structured feedback without rewriting |
| `polish` | Sentence-level clarity and precision improvements |
| `restructure` | Reorganize sections for better logical flow |
| `rewrite` | Substantially rewrite a section |
| `adapt` | Convert text between venue conventions |
| `outline` | Plan a paper structure from scratch |
| `check` | Verify compliance with venue formatting rules |

### Knowledge Base

- **Venue conventions**: Exact word limits, abstract formats, methods placement, title styles, contribution list rules, citation formats for all 12 venue families
- **Writing principles**: Swales CARS model, known-to-new information flow, hedging calibration continuum, six core sentence types, paragraph architecture
- **Common mistakes**: Editor-catalogued rejection reasons, sentence-level error patterns, the "deadly sins" of scientific writing
- **AI-pattern detection**: Vocabulary blocklist and structural markers that flag text as AI-generated

## Installation

### Option 1: As a Claude Code Skill (Recommended)

Copy the files to your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/scientific-writing/references
cp SKILL.md ~/.claude/skills/scientific-writing/
cp references/*.md ~/.claude/skills/scientific-writing/references/
```

The skill will be automatically detected by Claude Code on next launch.

### Option 2: As a Claude Code Command

```bash
cp SKILL.md ~/.claude/commands/scientific-writing.md
```

Note: This option won't include the reference files. The skill version is recommended for full functionality.

## Usage

Once installed, invoke the skill in Claude Code:

```
/scientific-writing review my introduction for MLHC
/scientific-writing polish this paragraph for Nature
/scientific-writing adapt this section from IEEE to Lancet format
/scientific-writing check compliance with CHIL 2026 requirements
/scientific-writing outline a full paper for NeurIPS
/scientific-writing rewrite this discussion section
```

You can also provide text directly:

```
/scientific-writing review this for AMIA: [paste your text here]
```

## File Structure

```
scientific-writing-skill/
├── README.md                          # This file
├── SKILL.md                           # Main skill definition
└── references/
    ├── venue-conventions.md           # Detailed rules for 12 venue families
    └── writing-principles.md          # Universal writing principles & reference
```

### SKILL.md
The main skill prompt. Defines the analysis framework, task types, venue-aware review process, and output formats. Handles venue detection, section identification, and applies the correct conventions automatically.

### references/venue-conventions.md
Comprehensive reference covering:
- Abstract format and word limits per venue
- Methods placement conventions
- Title style norms
- Contribution list requirements
- Citation format (numbered vs. author-year)
- Cross-venue comparison tables

### references/writing-principles.md
Universal scientific writing toolkit:
- Six core sentence types (background, gap, action, design, result, boundary)
- Known-to-new information flow principle
- Hedging calibration (7-level continuum from "might possibly" to "demonstrates")
- Active vs. passive voice decision guide
- Precision and conciseness replacements
- Tense quick reference by section
- Common mistakes with fixes
- AI-pattern vocabulary blocklist
- Cross-discipline register differences (CS vs. clinical vs. natural science)
- Swales CARS model for introductions

## Supported Venues — Quick Reference

### Where Methods Go
- **End of paper:** Nature, Science, Cell
- **After Introduction (IMRAD):** Lancet, NEJM, BMJ
- **Section 2–3 (prominent):** IEEE, ACM, NeurIPS, ICML, ICLR, AMIA, CHIL, MLHC

### Contribution Lists
- **Never used:** Nature, Science, Cell, Lancet, NEJM, BMJ
- **Mandatory:** IEEE, ACM, NeurIPS, ICML, ICLR, AAAI
- **Recommended:** AMIA, CHIL, MLHC, Elsevier, Springer

### Abstract Format
- **Unstructured (~125–150 words):** Nature, Science, Cell
- **Unstructured (~150–250 words):** IEEE, ACM, NeurIPS, ICML
- **Structured (~250–300 words):** Lancet, NEJM, BMJ

## Based On

This skill synthesizes conventions and guidelines from:

- **Style guides:** Strunk & White, Williams & Bizup ("Style"), Pinker ("The Sense of Style"), Glasman-Deal ("Science Research Writing"), Schimel ("Writing Science"), Sword ("Stylish Academic Writing")
- **Foundational research:** Swales CARS model (1990), Gopen & Swan (1990), Hyland's hedging taxonomy (1998)
- **Journal/venue author guidelines:** Nature, Science, Cell, Lancet, NEJM, BMJ, IEEE, ACM, NeurIPS, ICML, ICLR, AAAI, AMIA, CHIL, MLHC, ML4H, BHI, ICHI, MedInfo, Elsevier, Springer
- **Editor commentaries and meta-analyses:** Common rejection reasons, writing quality criteria, AI-text detection patterns (Liang et al., 2024)

## License

MIT

---

# Scientific Writing Skill — Claude Code 学术写作技能

一个面向 [Claude Code](https://claude.ai/claude-code) 的综合学术写作技能插件，能够分析、审稿、重构和润色面向任何主流学术会议/期刊的科学论文——从 Nature、Science 到 IEEE、NeurIPS、AMIA 等。

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
├── README.md                          # 本文件
├── SKILL.md                           # 主技能定义
└── references/
    ├── venue-conventions.md           # 12 个 venue 家族的详细规范
    └── writing-principles.md          # 通用学术写作原则与参考
```

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
