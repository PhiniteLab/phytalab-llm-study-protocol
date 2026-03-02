# LLM Study Protocol for AI & RL (Student-Facing)

This protocol defines *how to use general LLMs* (ChatGPT/Claude/Gemini, etc.) to learn AI & RL **rigorously**:
- The LLM is a *tutor and research assistant*.
- The student is responsible for **verification**, **understanding**, and **original writing/coding**.

---

## 0) Core principles
1) **Triangulate**: ask at least two models (or the same model twice with different prompts) and compare.  
2) **Verify**: do not accept “facts” without primary sources (papers/books).  
3) **Constrain format**: force structured output (headings / JSON schema).  
4) **Show your work**: keep a paper trail (prompts, notes, sources, experiments).  
5) **Iterate**: use the LLM in short cycles: question → answer → check → refine.

---

## 1) Workflow overview (repeat this loop)
### Step 1 — Define the question precisely
Write a 3–5 line specification:
- What do you want to understand?
- What prerequisite knowledge do you assume?
- What output do you want (proof? algorithm? code? experiment plan?)
- What constraints (notation, environment, dataset, compute)?

Use `templates/md/Topic_DeepDive_Template.md`.

### Step 2 — Gather primary sources *before* asking the LLM
Minimum:
- 1 textbook chapter OR 1 survey paper
- 1–2 original papers (if the topic is “paper-level”)

Record sources in:
- `templates/json/paper_record.template.json`
- `templates/md/Paper_Reading_Template.md`

### Step 3 — Ask the LLM using a strict format
Use `prompts/Deep_Dive_Prompt.md`.  
Request:
- Definitions & notation
- Theorem statement(s)
- Step-by-step proof (with equations)
- Algorithmic blueprint (pseudocode)
- Implementation plan (module layout)
- Tests & sanity checks
- Failure modes + debugging plan

### Step 4 — Verify and correct
You must verify:
- Theorems (statement, assumptions, proof outline)
- Key equations and gradients
- Complexity claims
- Implementation details (tensor shapes, sign conventions, off-by-one issues)

Create a **verification checklist** in your notes and tick items only after checking sources.

### Step 5 — Build an “understanding artifact”
Convert the result into:
- A topic card: `templates/json/topic_card.template.json`
- A theorem record: `templates/json/theorem_record.template.json`
- A 1–2 page explanation in your own words (no copy/paste)

### Step 6 — Implement and test
Follow `protocol/Theorem_to_Production_Pipeline.md`.  
Minimum standards:
- `pytest` unit tests
- fixed seeds + deterministic eval
- run logs stored as JSONL
- reproducible environment (`pyproject.toml` + lockfile)

### Step 7 — Evaluate and reflect
For RL:
- learning curves with confidence intervals (multiple seeds)
- evaluation policy separate from training
- check reward hacking & unsafe behaviors

For AI/LLM:
- clear dataset split and leakage checks
- compare against baselines
- report failure cases

---

## 2) Output formatting standard (Markdown)
When you ask an LLM for an answer in Markdown, require this exact header order:

## Quick Summary
## Assumptions and Notation
## Concept Glossary
## Theoretical Foundations
## Derivation and Algorithmic Blueprint
## Math-to-Code Mapping
## Engineering and MLOps
## Complete Reference Implementation
## Evaluation Protocol and Metrics
## Validation Checklist
## Next Steps

If the model fails, ask it to **rewrite** and strictly follow the header order.

---

## 3) Output formatting standard (JSON)
For difficult topics, prefer “JSON-wrapped markdown”:
- JSON is used for structure and metadata.
- The main explanation stays in Markdown for readability.

Use `templates/json/answer_envelope.template.json`.

---

## 4) Triangulation protocol (practical)
1) Ask Model A for a structured answer.  
2) Ask Model B *the same prompt*.  
3) Compare:
   - any disagreement → mark as “uncertain”
   - request sources from each model
4) Check primary sources.
5) Update your topic card with corrected facts.

---

## 5) What to do when you get stuck
- Reduce scope: ask for *one lemma* only.
- Ask the model to list missing prerequisites and propose a learning path.
- Ask for a counterexample / edge case.
- Ask for a minimal working code example with tests.

---

## 6) What you must NOT do
- Do not submit LLM text as your writing.
- Do not fabricate citations.
- Do not use LLM output without verification for high-stakes decisions.

See also: `protocol/Ethics_Academic_Integrity.md`.
