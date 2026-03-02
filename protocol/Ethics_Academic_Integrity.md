# Ethics & Academic Integrity for Using LLMs in AI/RL Study

This document defines acceptable and unacceptable use of LLMs in academic learning and research.

---

## 1) Academic integrity
### Allowed
- Using LLMs as a **tutor**: explanations, examples, analogies
- Generating **practice problems** and solutions *for self-study*
- Getting help with **debugging**, code review, and test planning
- Brainstorming research questions and experiment designs
- Summarizing a paper **after you have read it** (to compare understanding)

### Not allowed (typical course standards)
- Submitting LLM-generated text as your own writing
- Submitting LLM-generated code as your own without attribution and understanding
- Using LLMs to bypass learning objectives (e.g., “write my assignment”)
- Fabricating citations or claiming you read a paper you did not read

**Rule of thumb:** If the work product is graded, your contribution must be clearly identifiable and defensible.

---

## 2) Transparency & attribution
- Keep a `prompts_log.md` for important interactions:
  - date, model, prompt, short summary of what was used
- In reports, cite primary sources (papers/books) and disclose LLM assistance at a high level:
  - “Used LLMs to propose alternative derivations, then verified against sources.”

Do **not** cite LLMs as primary scientific references.

---

## 3) Data privacy and confidentiality
Do not paste:
- private student data, grades, personal identifiers
- unpublished internal research
- proprietary code or datasets
- exam solutions or restricted course materials

If you must discuss sensitive data, **abstract** it:
- replace with synthetic examples
- describe statistics instead of raw records

---

## 4) Responsible research practice (AI/RL specifics)
- **Safety:** RL agents can learn unsafe policies; do not deploy without safeguards.
- **Bias & fairness:** be mindful of dataset biases and evaluation blind spots.
- **Dual-use:** avoid generating harmful instructions or unsafe systems.
- **Reproducibility:** log seeds, configs, commits, and environment versions.

---

## 5) Verification: your non-negotiable responsibility
LLMs can hallucinate:
- theorems, equations, citations, and code details

Therefore you must:
- check equations against sources
- reproduce key results (even small-scale)
- explicitly list limitations

---

## 6) A short ethical checklist before you submit work
- [ ] I can explain every key step without the LLM.
- [ ] I verified equations and claims against primary sources.
- [ ] I did not fabricate citations.
- [ ] I disclosed LLM use appropriately (if required).
- [ ] I did not share confidential information with the model.
