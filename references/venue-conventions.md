# Venue Conventions Reference

## 1. Nature / Nature Family

| Property | Value |
|---|---|
| Abstract | Unstructured, ~150 words. Pattern: context (1 sent) -> gap (1 sent) -> "Here we show/report..." -> key results (2-4 sent) -> significance (1 sent) |
| Title | <90 characters. Descriptive or mildly declarative. No colons preferred. No acronyms. |
| Introduction | 2-4 paragraphs, ~500 words. No labeled heading. Ends with "Here we..." |
| Methods | End of paper ("Methods" or "Online Methods"). Main text must be followable without reading Methods. |
| Results | Separate section. Narrative, claim-first. "We found X (Fig. 1a)" not "Fig. 1a shows X". |
| Discussion | 3-5 paragraphs. Interpret, don't restate. Summary -> mechanism -> prior work -> limitations -> broader impact. |
| Main text length | ~3,000 words (excluding abstract, methods, references, legends) |
| Figures | Up to 6-8 display items. Multi-panel (a,b,c...). Legends self-contained with title (bold), definitions, error bars, N, stats. |
| References | ~30, numbered superscript, order of appearance. Cite only essential references. |
| Voice | Active, "We". Short sentences (15-25 words average). Accessible to all scientists. |
| No contribution list. | No "Related Work" section. Literature woven into introduction. |
| Key phrase | "Here we show that..." |

## 2. Science / Science Family

| Property | Value |
|---|---|
| Abstract | Unstructured, ~125 words (one of the shortest). Science Translational Medicine uses structured. |
| Title | <100 characters. Slightly more declarative than Nature. Question titles occasionally used. |
| Introduction | 2-3 paragraphs. Among the shortest intros in top journals. |
| Methods | End of paper ("Materials and Methods"). |
| Results | Often no explicit heading — continuous narrative after intro. Claim-first. |
| Main text | ~2,500 words. Science Advances: ~5,000-8,000 words. |
| References | ~30-40, numbered superscript. |
| Voice | Active preferred. Extremely compressed prose. Editors heavily line-edit accepted papers. |

## 3. Cell / Cell Press

| Property | Value |
|---|---|
| Abstract | Unstructured, ~150 words. |
| Highlights | REQUIRED. 3-4 bullet points, each <85 characters. Summarize key findings. |
| eTOC blurb | REQUIRED. ~50 words for table of contents. |
| Title | 10-15 words. More declarative than Nature/Science. Colons common. |
| Introduction | 3-5 paragraphs. More thorough literature context than Nature/Science. |
| Methods | End of paper. STAR Methods format (Key Resources Table, Resource Availability, Experimental Model Details, Method Details, Quantification and Statistical Analysis). |
| Results/Discussion | Separate sections. |
| Main text | ~5,000-7,000 words. More generous than Nature/Science. |
| Figures | Up to ~7 main figures. More data-dense per panel. |
| References | ~50-70. |
| Limitations | Increasingly required as explicit subsection in Discussion. |

## 4. The Lancet

| Property | Value |
|---|---|
| Abstract | STRUCTURED: Background, Methods, Findings, Interpretation, Funding. 300 words. Note: "Findings" not "Results", "Interpretation" not "Conclusion". |
| Title | Descriptive, includes study design. 15-20 words. Never declarative. E.g., "Effect of X on Y in patients with Z: a randomised, double-blind, placebo-controlled trial" |
| Introduction | 2-3 paragraphs, ~300-400 words. (1) What is known, (2) What is not known, (3) What this study does. |
| Methods | After Introduction (standard IMRAD). CONSORT/STROBE/PRISMA compliance required. |
| Results | Systematic. Primary outcome first, then secondary. Effect sizes + CI required. |
| Discussion | Summary -> comparison -> strengths/limitations (REQUIRED) -> implications. ~1,500 words. |
| Main text | ~3,000-4,500 words. ~30 references. Up to 5 figures/tables. |
| Voice | Mixed active/passive. Formal, precise. British English. |
| Key convention | "Was associated with" (observational) vs. "resulted in" (causal/RCT). |

## 5. NEJM (New England Journal of Medicine)

| Property | Value |
|---|---|
| Abstract | STRUCTURED: Background, Methods, Results, Conclusions. 250 words. Dense with specific numbers and CIs. |
| Title | Descriptive, never declarative. Study-design inclusive. Often concise: "Drug X for Condition Y". |
| Introduction | 2 paragraphs, ~200-300 words. Shortest intros among top journals. |
| Methods | After Introduction. Very detailed subsections (Study Design, Patients, Interventions, Outcomes, Statistical Analysis). |
| Results | Structured by pre-specified outcomes. Primary endpoint first. Tables heavily used. |
| Discussion | Short. Contextualization, limitations, clinical implications. |
| Main text | ~2,500 words. ~30 references. 4-5 figures/tables. |
| Voice | Formal but accessible to practicing clinicians. American English. |
| Statistical reporting | "Hazard ratio, 0.78; 95% CI, 0.65 to 0.93; P=0.004" |

## 6. BMJ (British Medical Journal)

| Property | Value |
|---|---|
| Abstract | STRUCTURED: Objective(s), Design, Setting, Participants, Main outcome measures, Results, Conclusions. 250-300 words. Most granular abstract format. |
| Title | Descriptive, study design in subtitle. Slightly more accessible/engaging than Lancet. |
| Introduction | 2-3 paragraphs. Ends with clear study aim. |
| Methods | After Introduction. Patient/public involvement (PPI) required. Reporting checklists mandatory. |
| Discussion | Highly structured: Principal findings -> Strengths/weaknesses -> Relation to other studies -> Meaning/implications -> Unanswered questions. |
| Required boxes | "What is already known on this topic" (3 bullets) + "What this study adds" (3 bullets). |
| Main text | ~2,500-3,000 words. ~30 references. Up to 6 figures/tables. |
| Voice | Accessible. "Write in short sentences. Use the simplest word. Avoid nominalisations." British English. |

## 7. IEEE Transactions (TPAMI, TMI, JBHI, etc.)

| Property | Value |
|---|---|
| Format | Two-column, 10pt Times Roman, IEEEtran.cls. |
| Abstract | Unstructured, max 250 words. Include performance numbers. |
| Title | 8-15 words. Pattern: "MethodName: A [Adj] Approach to [Problem]". Colons very common. |
| Introduction | 1-1.5 pages. Ends with bulleted contribution list (3-4 items): "The main contributions of this paper are as follows:" |
| Related Work | Standalone Section II, 0.5-1.5 pages. Thematic, not chronological. Each paragraph ends with contrast statement. |
| Methods | "Proposed Method" or "The Proposed Framework". Math-heavy: inline notation, numbered equations. Architecture figure expected. |
| Experiments | Datasets, Implementation Details, Comparison with SOTA, Ablation Study, (Qualitative Results). Bold best results. Ablation studies expected. |
| Page limits | Regular: 12-14 pages including references. Short/Correspondence: 4-5 pages. |
| References | Numbered [1], order of appearance. 40-60 typical. |
| Voice | Active, "We propose/design/evaluate". Inline math: "Given input $x \in \mathbb{R}^d$..." |
| Tables | Booktabs style: horizontal lines only (top, header, bottom). Bold best, underline second-best. |

## 8. IEEE Conferences (EMBC, BHI, CVPR, etc.)

| Property | Value |
|---|---|
| Format | Two-column IEEE. |
| Page limits | EMBC: 4 pages + 1 ref-only. BHI: 4 pages. CVPR/ICCV: 8 pages excl. references. |
| Key difference | Much more compressed. Related work shortened or merged into intro. Ablation in supplementary. |

## 9. ACM Conferences (CHI, KDD, CSCW, etc.)

| Property | Value |
|---|---|
| Format | Single-column acmart sigconf. |
| Page limits | CHI: ~10 pages + refs (now variable length). KDD: 9 + 1 ref. CSCW: journal format, ~20-30 pages. |
| Abstract | Unstructured, 150-250 words. CCS taxonomy + keywords required. |
| Title | CHI/CSCW: longer, more descriptive, may include methodology. KDD: more like IEEE. |
| Introduction | CHI: 1.5-2 pages (human/social motivation). Contribution list standard but may list empirical findings. |
| Related Work | Standalone, extensive. CHI/CSCW cite social science, psychology, design. |
| Methods | CHI/CSCW: "Study Design", qualitative terminology. KDD: "Problem Formulation", "Algorithm". |
| Results | CHI: Mix qualitative themes + quantitative stats. KDD: benchmark tables like IEEE. |
| Double-blind | Self-citations in third person. Anonymous repos. No identifiable URLs. |

## 10. ML Conferences (NeurIPS, ICML, ICLR, AAAI)

| Property | Value |
|---|---|
| Format | NeurIPS/ICML/ICLR: single-column, custom .sty. AAAI: two-column. |
| Page limits | NeurIPS: 9 pages + unlimited refs/appendix. ICML: 8 + unlimited. ICLR: 10 + unlimited. AAAI: 7 + 1 ref + 1 ethics. |
| Abstract | Unstructured, 150-200 words. Include SOTA numbers. Assumes reader knows the field. |
| Title | Often catchy acronym + colon + description. Puns/wordplay common. 5-10 words ideal for high-impact. |
| Introduction | 1-2 pages. Teaser/motivating figure on page 1 near-mandatory. Contribution list (3 items) at end. |
| Related Work | Often at END of paper (before/after Conclusion) to save space. |
| Methods | "Method" or "Approach" or "[MethodName]". Begins with "Preliminaries/Background". Algorithm pseudocode expected. Extremely notation-heavy. |
| Experiments | Tables dominate (3-6 per paper). Ablation studies critical. Computational cost reporting increasingly expected. |
| Citations | Author-year (Vaswani et al., 2017) for NeurIPS/ICML/ICLR. Numbered for AAAI. |
| Voice | Very direct, almost terse: "We use AdamW with lr 3e-4." Present tense for method description. |
| Double-blind | NeurIPS, ICML, ICLR, CVPR. Self-cite in third person. Anonymous GitHub. |
| Reproducibility | NeurIPS checklist mandatory. Report random seeds, hardware, training time. |

## 11. Health Informatics Venues (AMIA, CHIL, MLHC, ML4H, BHI, ICHI, MedInfo)

| Property | AMIA | CHIL | MLHC | ML4H | ICHI |
|---|---|---|---|---|---|
| Paper length | 5-10 pages | 10+ pages | 10-15 pages (full) | 8 pages (proceedings) | Regular paper |
| Abstract | 125-150 words | Standard | Standard | Standard | Standard |
| Special reqs | Inclusive language, GenAI disclosure | Data/Code availability, Author contributions, IRB | "Generalizable insights" in intro, complete problem/cohort/features/methods/results | Welcomes negative results, critiques (findings track) | No supplementary materials |
| Style | Applied clinical informatics accepted | Methodological rigor, ML-heavy | Must explain why insights transfer beyond this dataset | Proceedings + findings tracks | Self-contained main text |

## 12. Elsevier / Springer Journals

| Property | Elsevier | Springer/LNCS |
|---|---|---|
| Format | Single-column elsarticle.cls (submission) | svjour3 (journals), llncs (proceedings) |
| Page limits | Usually no strict limit (10-20 published pages) | LNCS: 12-16 pages including refs |
| Abstract | Unstructured, 100-300 words. Highlights required (3-5 bullets, <85 chars). Graphical abstract may be required. | Unstructured |
| Style | More expansive writing. Longer related work, detailed methods, more baselines. | LNCS is dense due to page limits |
| Data availability | Increasingly required | Increasingly required |

---

## Cross-Venue Comparison: Key Structural Differences

### Where Methods Go
- **End of paper:** Nature, Science, Cell
- **After Introduction (IMRAD):** Lancet, NEJM, BMJ
- **Section 2-3 (prominent):** IEEE, ACM, NeurIPS, ICML, ICLR, AMIA, CHIL, MLHC

### Contribution Lists
- **Never used:** Nature, Science, Cell, Lancet, NEJM, BMJ
- **Mandatory:** IEEE, ACM, NeurIPS, ICML, ICLR, AAAI
- **Recommended:** AMIA, CHIL, MLHC, Elsevier, Springer

### Related Work
- **Woven into Introduction:** Nature, Science, Cell, Lancet, NEJM, BMJ
- **Standalone Section 2:** IEEE Transactions, ACM CHI/CSCW, Elsevier
- **At end of paper:** NeurIPS, ICML (common), ICLR (varies)

### Title Style
- **Short, no method name:** Nature, Science
- **Declarative (states finding):** Cell
- **Descriptive + study design:** Lancet, NEJM, BMJ
- **MethodName: Subtitle:** IEEE, NeurIPS, ICML
- **Long, includes methodology:** ACM CHI, CSCW

### Citation Format
- **Numbered superscript:** Nature, Science, Cell, Lancet, NEJM, BMJ
- **Numbered brackets [1]:** IEEE, AAAI, Springer LNCS
- **Author-year (Author, Year):** NeurIPS, ICML, ICLR, some Elsevier, some ACM
