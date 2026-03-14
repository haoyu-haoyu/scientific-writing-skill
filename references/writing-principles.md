# Scientific Writing Principles Reference

## 1. The Six Core Sentence Types in Scientific Writing

Every sentence in a scientific paper performs one of these rhetorical actions. A well-written sentence does exactly ONE.

### 1.1 Background Sentence
Sets the scene by stating what is known.
- "X is increasingly used in Y, but..."
- "Multimodal EHR data combine structured fields with unstructured clinical notes."
- Tense: present (established facts) or present perfect (recent developments)

### 1.2 Gap Sentence
Identifies what is missing, unresolved, or problematic.
- "Despite growing interest in X, no study has examined..."
- "However, these approaches assume temporal alignment across modalities — an assumption rarely met in practice."
- Tense: present perfect ("has not been") or present ("remains unclear")

### 1.3 Action Sentence (Contribution)
States what this paper does. The most important sentence in the paper.
- "Here we show that..." (Nature/Science)
- "We present / propose / evaluate / release..."
- "In this work, we construct a benchmark that..."
- Tense: present ("we present") or past ("we developed")

### 1.4 Design Sentence
Describes how the study was set up — objects, scope, methods.
- "We used [dataset] to construct [cohort], and evaluated [model] on [task]."
- "Using a retrospective cohort of 12,000 ICU admissions from MIMIC-IV..."
- Tense: past

### 1.5 Result Sentence
Reports what was found. ALWAYS lead with the finding, not the procedure.
- "Across tasks, performance gains were driven primarily by..."
- "The model achieved 0.87 AUROC (95% CI: 0.84-0.90) on 30-day readmission prediction."
- NOT: "We ran the model and found that the AUROC was 0.87" (buries the finding)
- Tense: past

### 1.6 Boundary Sentence
Qualifies a claim — states what the finding does NOT mean, or where it does NOT apply.
- "This improvement likely reflects X, but should not be generalized beyond Y."
- "These results are specific to tertiary-care ICU populations and may not transfer to primary care settings."
- Tense: present (for ongoing limitations) or conditional ("would need to be validated")

---

## 2. Information Flow: Known-to-New Principle

**Rule:** The beginning of each sentence (topic position) contains familiar information. The end (stress position) contains new, important information.

**The Chain Pattern:**
```
Sentence 1: [Known context] → [New concept A]
Sentence 2: [A as known] → [New concept B]
Sentence 3: [B as known] → [New concept C]
```

**Example (good):**
> Electronic health records store clinical data in structured and unstructured formats.
> These formats differ in how easily they can be processed by machine learning models.
> Such models require consistent feature representations, which structured data provides but clinical notes do not.

**Example (bad — new-to-known):**
> A novel deep-learning architecture was developed for segmenting retinal layers.
> OCT imaging data from 500 patients was used to train this architecture.
> State-of-the-art performance on three benchmarks was achieved.

---

## 3. Paragraph Architecture

### The Standard Scientific Paragraph
1. **Topic sentence** — states the paragraph's main claim
2. **Evidence/elaboration** — 2-5 sentences supporting the claim
3. **Wrap-up** (optional) — synthesizes, qualifies, or transitions

### Paragraph Unity Test
- Can you write a 5-word headline for this paragraph?
- If you need two headlines, you need two paragraphs.
- Does removing any sentence leave a gap? If not, it may not belong.

### Paragraph Length Norms
- Journal articles: 4-8 sentences
- Conference papers: 3-6 sentences
- Single-sentence paragraphs: acceptable for emphasis, but rare

---

## 4. Hedging Calibration

### The Hedging Continuum (weakest to strongest)

| Level | Expression | Use when |
|---|---|---|
| Very weak | "might possibly contribute to" | Never — stacking hedges destroys credibility |
| Weak | "may contribute to" | Exploratory, small sample, no prior evidence |
| Moderate-weak | "appears to contribute to" | Observational evidence, needs replication |
| Moderate | "The evidence suggests X contributes to" | Multiple studies, consistent direction |
| Moderate-strong | "X likely contributes to" | Strong observational or experimental evidence |
| Strong | "X contributes to" | Well-established experimental evidence |
| Very strong | "X is known to contribute to" | Textbook fact — requires citation |
| Assertion | "X causes Y" | Only for RCTs or proven causal mechanisms |

### Hedging Rules
- **Match hedge to evidence.** Correlational data = "associated with", "may". RCT = "resulted in".
- **Never stack hedges.** "could potentially possibly" = no. Pick one hedge.
- **Hedge claims, not data.** "The AUROC was 0.87" (no hedge needed — it's a number). "This suggests the model captures temporal dependencies" (hedge needed — it's interpretation).
- **Discipline variation:** Medical writing hedges more than CS writing. A claim that would be "we show" in NeurIPS might be "our findings suggest" in Lancet.

### Reporting Verbs by Stance

| Stance | Verbs |
|---|---|
| Neutral | describe, report, present, state, note, observe |
| Tentative | suggest, propose, hypothesize, speculate |
| Assertive | demonstrate, show, establish, confirm, reveal |
| Critical | claim, assert, allege, contend, assume, overlook |

---

## 5. Active vs. Passive Voice

### What style guides actually say
- APA 7th ed.: "Use the active voice as much as possible"
- AMA 11th ed.: "In general, authors should use the active voice"
- Nature: Explicitly encourages active voice and first person
- IEEE: "The active voice is generally preferred"

### When to use each

| Situation | Voice | Example |
|---|---|---|
| Reporting what you did | Active | "We recruited 200 participants" |
| Agent unknown/irrelevant | Passive | "Samples were stored at -80C" |
| Maintaining topic continuity | Passive | "The protein was phosphorylated, washed, and eluted" |
| Stating conclusions | Active | "We conclude that..." |
| Describing established facts | Either | "X is associated with Y" / "Researchers have shown..." |

### The real rule
Use passive to manage information flow (keeping the topic in subject position), not out of false modesty. Default to active.

---

## 6. Precision Toolkit

### Vague Words to Replace

| Vague | Precise alternative |
|---|---|
| several | state the number (3, 5, 12) |
| recently | state the year or timeframe |
| significant | statistically significant (p < 0.05) / clinically significant / substantial |
| better | higher AUROC by 0.03 / lower error rate / faster by 2x |
| novel | [describe what is actually new — the novelty should be self-evident] |
| robust | specify: robust to what? (noise, missing data, distribution shift) |
| effective | effective at what? measured how? compared to what? |
| state-of-the-art | cite the specific prior SOTA and the margin of improvement |

### Conciseness Replacements

| Wordy | Concise |
|---|---|
| In order to | To |
| Due to the fact that | Because |
| It is important to note that | [delete] |
| A total of N | N |
| It has been shown that X (ref) | X (ref) |
| Has the ability to | Can |
| In the event that | If |
| Prior to / Subsequent to | Before / After |
| In close proximity to | Near |
| At the present time | Now / Currently |
| In a manner similar to | Like |
| With regard to / With respect to | About / For |
| On the basis of | Based on |
| For the purpose of | To / For |
| In light of the fact that | Because / Since |
| It is worth noting that | [delete, or state the thing directly] |
| As a matter of fact | [delete] |
| Serves as | Is |
| Plays a crucial role in | Affects / Influences / Determines |

---

## 7. Cohesion Devices

### The "This + Noun" Rule
ALWAYS follow "this" with a noun. Bare "this" is the most common source of ambiguity.
- Bad: "This has important implications."
- Good: "This finding has important implications."
- Bad: "This was unexpected."
- Good: "This discrepancy was unexpected."

### Logical Connectors

| Function | Connectors |
|---|---|
| Addition | Furthermore, Moreover, In addition, Also |
| Contrast | However, Nevertheless, In contrast, Conversely, By contrast |
| Cause/Effect | Therefore, Consequently, Thus, Hence, As a result |
| Concession | Although, While (caution: ambiguous), Whereas, Despite |
| Exemplification | For example, For instance, Specifically |
| Summary | In summary, Overall, Taken together, Collectively |
| Sequence | First, Second, Finally, Subsequently, Next |

### Anti-pattern: Over-connector Syndrome
Do NOT start every sentence with a connector. If more than 40% of sentences begin with a connector, you have a problem. Let the logic flow from sentence content, not from connector words.

### Lexical Cohesion Rule
Repeat key terms consistently. Do NOT use "elegant variation" (calling the same thing by different names). If it's "deep learning" in sentence 1, do not call it "machine intelligence" in sentence 2.

---

## 8. Tense Quick Reference

| Section | Tense | Example |
|---|---|---|
| Introduction (established facts) | Present | "Cancer is a leading cause..." |
| Introduction (gap) | Present perfect | "No study has examined..." |
| Introduction (this paper) | Present | "We present..." or "Here we show..." |
| Methods | Past | "We recruited 200 participants" |
| Results (your data) | Past | "The model achieved 0.87 AUROC" |
| Results (figures/tables) | Present | "Table 2 shows..." |
| Discussion (your findings) | Past | "We observed a significant..." |
| Discussion (interpretation) | Present | "This finding suggests..." |
| Discussion (established knowledge) | Present | "Prior work has shown..." |
| Conclusion | Present | "Our findings indicate..." |

---

## 9. Common Mistakes Catalogued by Editors

### Structural Mistakes (Most Common Rejection Reasons)

1. **No clear contribution** (~50-60% of desk rejections). Reader cannot determine what is new.
2. **Poor logical flow** (~40-50%). Paper reads as fact collection, not argument.
3. **Overclaiming** (~30-40%). Conclusions beyond what data support.
4. **Unfocused / too long** (~30-40%). Tangential material dilutes the message.
5. **Unintelligible to target audience** (~20-30%). Assumes knowledge readers lack.
6. **Abstract mismatches paper** (~15-20%). Promises what paper does not deliver.

### Sentence-Level Mistakes

| Mistake | Example | Fix |
|---|---|---|
| Dangling modifier | "Using deep learning, the accuracy improved" | "Using deep learning, we improved accuracy" |
| Pronoun ambiguity | "We compared A and B. It was superior." | "Model A was superior." |
| Tense inconsistency | Switching past/present without reason | Follow the tense reference above |
| Misplaced "only" | "We only measured blood pressure" | "We measured only blood pressure" |
| Noun stack | "patient blood pressure measurement protocol" | "protocol for measuring patients' blood pressure" |
| Nominalization | "The implementation of the algorithm was performed" | "We implemented the algorithm" |

### The "Deadly Sins" of Scientific Writing

1. **Passive Pileup:** Five consecutive passive sentences with unclear agents
2. **Citation Avalanche:** Eight citations supporting one generic claim — pick 2-3
3. **Zombie Introduction:** Background but no gap, no purpose, no reason to care
4. **Data Dump Results:** Tables/figures with no narrative thread
5. **Mirror Discussion:** Restates each result with "consistent with..." but never synthesizes
6. **Bait-and-Switch Abstract:** Frames as solving problem X; paper addresses problem Y

---

## 10. AI-Pattern Vocabulary Blocklist

These words/phrases are statistically overrepresented in LLM-generated text and should be avoided in scientific writing:

### High-Risk Words (replace immediately)
- delve / delve into
- tapestry / rich tapestry
- landscape (metaphorical — "the AI landscape")
- multifaceted
- pivotal / pivotal role
- crucial / crucial role (overused — use "important" or be specific)
- underscores (the importance)
- realm
- noteworthy
- cutting-edge
- revolutionize
- leverage (as verb — use "use" or "exploit")
- foster
- holistic
- pave the way
- shed light on
- a testament to
- in the rapidly evolving field of
- harness (the power of)
- paradigm shift

### High-Risk Patterns (restructure)
- "Not only X, but also Y" — state the point directly
- Starting paragraphs with "Additionally" / "Furthermore" / "Moreover" mechanically
- Rule of three (forced triplets)
- Exhaustive enumeration instead of selective focus
- Uniform paragraph length (all paragraphs 4-5 sentences)

---

## 11. Cross-Discipline Register Differences

### CS/Engineering Register
- "We propose..." (active, first person)
- "Our method achieves..." (possessive for system)
- "Note that..." (direct reader address)
- Inline math: "where $\alpha \in [0,1]$ controls..."
- Terse: "We use ResNet-50 pretrained on ImageNet."

### Medical/Clinical Register
- "It was observed that..." (passive, impersonal — acceptable in clinical)
- "Further studies are warranted..." (cautious)
- Effect sizes with CI: "HR 0.78, 95% CI 0.65-0.93"
- Patient-first language: "patients with diabetes" not "diabetic patients"
- Ethics statements required

### Natural Science Register
- "Here we show that..." (Nature signature)
- "Taken together, these data suggest..." (biology signature)
- Figure-driven narrative
- Minimal jargon for broad audience

### Interdisciplinary (Health Informatics)
- Must bridge CS and clinical registers
- Define CS terms for clinicians; explain clinical context for CS readers
- "Layered" strategy: accessible main text, technical details in methods
- Common failure: too technical for clinicians AND too clinical for computer scientists

---

## 12. The Swales CARS Model for Introductions

**Move 1 — Establishing a territory:**
- Claim centrality of the research area
- Make topic generalizations
- Review prior research (selectively)

**Move 2 — Establishing a niche:**
- Counter-claim (previous work is flawed/limited)
- Indicate a gap (no one has done X)
- Raise a question (it remains unclear whether...)
- Continue a tradition (extending prior work to new setting)

**Move 3 — Occupying the niche:**
- Outline purpose / state research aim
- Announce present research ("Here we..." / "In this work, we...")
- Announce principal findings (optional in intro, mandatory in abstract)
- Indicate paper structure (optional, more common in CS than life sciences)

---

## 13. Key Reference Works

| Work | Key Contribution |
|---|---|
| Gopen & Swan (1990), "The Science of Scientific Writing" | Known-to-new principle, topic/stress positions |
| Williams & Bizup, "Style: Lessons in Clarity and Grace" | Nominalization diagnosis, clarity principles |
| Pinker, "The Sense of Style" (2014) | Curse of Knowledge, classic style |
| Schimel, "Writing Science" (2012) | Story structure, OCAR framework |
| Swales, "Genre Analysis" (1990) | CARS model for introductions |
| Hyland, "Hedging in Scientific Research Articles" (1998) | Hedging taxonomy |
| Sword, "Stylish Academic Writing" (2012) | Data-driven readability analysis |
| Glasman-Deal, "Science Research Writing" (2010) | Section-by-section rhetorical moves |
| Day & Gastel, "How to Write a Scientific Paper" (2022) | Comprehensive practical guide |
