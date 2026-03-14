# Scientific Writing Skill for Claude Code

A comprehensive [Claude Code](https://claude.ai/claude-code) skill that analyzes, critiques, restructures, and polishes scientific manuscripts for any major academic venue — from Nature and Science to IEEE, NeurIPS, AMIA, and beyond.

> **[中文版说明 / Chinese Version](README_CN.md)**

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
├── README.md                          # English documentation
├── README_CN.md                       # Chinese documentation
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
