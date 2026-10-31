# PYTHALAB — Student Protocol Kit for Learning AI & RL with General LLMs

**Version:** 1.0  
**Date:** 2026-03-02

This kit is meant to be shared with students who will study **AI** and **Reinforcement Learning (RL)** using general-purpose LLMs (e.g., ChatGPT, Claude, Gemini) *as research assistants*, while keeping work academically rigorous, ethical, and reproducible.

## What this kit contains
- A **study protocol** (how to ask questions, verify answers, and build understanding)
- An **ethics & academic integrity** guideline
- A **deep-dive prompt template** optimized for theorem/proof/equations → algorithm → code → production
- A workflow for using **online tools** (papers, citations, baseline code, reproducibility)
- A pipeline that connects **theory → implementation → experiments → production**
- **Reusable templates** in `.md` and `.json`
- Starter topic lists for **AI** and **RL**

## Recommended folder workflow (per student project)
Create a new project folder and copy the templates:
```
my_project/
  00_admin/
  01_questions/
  02_sources/
  03_notes/
  04_math/
  05_code/
  06_experiments/
  07_reports/
```

## How students should use this kit (high-level)
1) Pick a topic from `starter_kits/` and create a `topic_card.json` in `04_math/`.  
2) Use `prompts/Deep_Dive_Prompt.md` to query an LLM and request a **strictly structured** answer.  
3) Verify: follow the **verification checklist** and only trust claims backed by primary sources.  
4) Translate math into code using `templates/json/implementation_plan.template.json`.  
5) Implement in a professional layout and track experiments with `templates/json/experiment_log.template.json`.  
6) Write a final report in `07_reports/` and include citations.

## Minimal standard for academic use of LLMs
- You must **not** treat LLM outputs as authoritative.
- You must **log prompts** (what you asked) and **log sources** (what you verified).
- You must cite original sources (papers/books), not the LLM.

See: `protocol/LLM_Study_Protocol.md` and `protocol/Ethics_Academic_Integrity.md`.
