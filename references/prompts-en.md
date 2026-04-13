# Prompt Template Library (English)

Based on Mizumoto (2025) guide. Prompts are designed to be used with any L1 background.

---

## 1. L1 → English Conversion

### 1.1 Basic Conversion (Stage 1)

```
Convert the following text into English, prioritizing accuracy of meaning
over stylistic elegance. Do not add new content.

[L1 text]
```

### 1.2 Style Adjustment (Stage 2)

```
Adjust the following English text to conform to academic writing conventions.
Improvements:
- Shorten long subjects
- Add appropriate hedging (but do not over-hedge)
- Use [past tense / passive voice / etc.] as standard for [Section name]
Do not change the meaning. Mark all changes in bold.

[English text]
```

### 1.3 Deviation Check

```
Compare this English text against the original and list any deviations
in meaning, emphasis, or scope.

Original: [L1 text]
English: [generated English text]
```

---

## 2. Diagnosis and Checking

### 2.1 Five-Point Comprehensive Check

```
Check the following paragraph on five dimensions.
For each, state "OK" if no issues, or give a specific diagnosis.

(1) Tense: Consistent and appropriate for this section?
(2) Information structure: Does it follow Given-New ordering?
(3) Logical flow: Any jumps between sentences?
(4) Transitions: Appropriate in number and formality?
(5) Paragraph structure: Clear topic sentence? One topic per paragraph?

Section: [section name]
[paragraph]
```

### 2.2 Reporting Verb Audit

```
Extract all reporting verbs from the following text and list them.

Check:
(1) Is any verb repeated 3+ times?
(2) Are strong verbs (proved, demonstrated) used for neutral reporting?
(3) Are any verbs inappropriate for the context?

Suggest one alternative for each issue found.

[text]
```

### 2.3 Methods Vagueness Detection

```
Identify vague expressions in the following Methods section.
Criterion: "Could another researcher replicate the study from this description alone?"

For each issue:
(1) The vague expression
(2) Why it is vague
(3) What information should be added (mark [TO BE ADDED] if unknown)
```

---

## 3. Section-Specific Support

### 3.1 Introduction Structure Check (CARS Model)

```
Analyze the following Introduction using the CARS model:
(1) Establishing the territory (importance + prior work)
(2) Establishing the niche (gap)
(3) Occupying the niche (purpose of this study)

Is each element present? Is the order appropriate?
Is the gap specific enough?
Flag missing elements. Do not add content.

[Introduction]
```

### 3.2 Discussion Structure Check (6 Moves)

```
Check whether the following Discussion contains all six moves:
(1) Summary of results  (2) Interpretation  (3) Comparison with prior work
(4) Implications  (5) Limitations  (6) Future research

Flag missing moves or unnatural ordering. Do not add content.

[Discussion]
```

### 3.3 Abstract Check (5 Moves)

```
Check the following Abstract:
(1) Does it contain all five moves (Background, Purpose, Method, Results, Conclusion)?
(2) Does it include information not in the main text?
(3) Is word count within the target journal's limit?

Flag issues only. Do not provide revised text.

[Abstract]
```

---

## 4. Proofreading

### 4.1 Intensity Levels

- **Minimal:** `Proofread this (minimal requirements only).`
- **Light:** `Lightly proofread this.`
- **Standard:** `Proofread this, improving clarity and flow.`
- **Deep:** `Proofread this, significantly improving clarity and flow.`

### 4.2 Paraphrase Options

```
Paraphrase the TARGET below without changing the meaning.
Provide 3 options. For each:
1) Suitable context (one line)
2) Formality level (high / medium / low)
3) Why this option works

TARGET: [expression]
CONTEXT: [surrounding text]
```

---

## 5. AI-Use Disclosure Templates

### Decision Flow

```
What did you use AI for?
├─ Grammar/proofreading only → Template A
├─ Outlining, paraphrase suggestions too → Template B
├─ Converting L1 Methods to English → Template C
├─ Generating analysis code → Template D
└─ Multiple tools → Template E
```

### Templates

**A (proofreading only):**
> The author(s) used a generative AI tool ([TOOL]) to improve clarity and readability of the manuscript, including proofreading and wording suggestions. All content, analyses, interpretations, and final decisions remain the author(s)' responsibility.

**B (outlining + paraphrasing):**
> The author(s) used a generative AI tool ([TOOL]) for language editing and drafting support, such as outlining, paraphrasing options, and grammar checking. The author(s) verified all statements and references and is fully responsible for the final manuscript.

**C (L1 → English conversion):**
> The author(s) used a generative AI tool ([TOOL]) to assist in converting technical procedures into natural-language descriptions and to refine wording. The author(s) ensured accuracy of all methodological descriptions and verified all factual claims and citations.

**D (code generation):**
> The author(s) used a generative AI tool ([TOOL]) for drafting support and for generating initial analysis code in R/Python. All generated code was reviewed, tested, and verified by the author(s). The author(s) is fully responsible for the accuracy of all analyses, interpretations, and the final manuscript.

**E (multiple tools):**
> The author(s) used the following AI tools during manuscript preparation: [TOOL1] for [PURPOSE1], [TOOL2] for [PURPOSE2]. All content, analyses, and interpretations are the author(s)' own. The author(s) verified all factual claims and references and takes full responsibility for the final manuscript.

---

## 6. Peer Review Support

### 6.1 Mock Review

```
You are a rigorous journal reviewer. Read the following manuscript
and produce a mock review report.

- Major concerns: max 3
- Minor concerns: max 5
- Positive aspects: max 3

Include specific locations (section, paragraph) for each point.

[manuscript]
```

### 6.2 Response to Reviewers

```
Draft a response to the following reviewer comment in English.

Requirements:
- Professional but confident tone
- Structure: gratitude → response → location of changes
- Mark page/line numbers as [TO BE FILLED]
- If declining the suggestion, state the rationale clearly

Reviewer comment: [comment]
Your plan (brief): [accept / partially accept / decline + reason]
```

---

## 7. Work Log

### Log Format

| Date | Section | AI usage | Input type | Output handling | Author verification |
|------|---------|----------|------------|----------------|-------------------|
| YYYY-MM-DD | [section] | [purpose] | [input type] | [adoption status] | [verification done] |
