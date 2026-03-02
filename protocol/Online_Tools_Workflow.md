# Online Tools Workflow (AI & RL)

The goal is to use online tools to build *your own understanding* instead of outsourcing thinking to an LLM.

---

## 1) Finding primary sources
- **arXiv**: search by keywords; record the arXiv ID; check version history.
- **Semantic Scholar**: explore citation graphs; identify surveys and “most cited” work.
- **Google Scholar**: locate newer follow-ups and critique papers.
- **OpenReview**: for ICLR/NeurIPS/ICML reviews and discussion.
- **SCI-ex database**: for writing the scientific journal.

**Practice:** For any claim the LLM makes, try to locate the corresponding paper (or textbook).

---

## 2) Reading efficiently (paper reading protocol)
Use `templates/md/Paper_Reading_Template.md`:
1) First pass: abstract → figures → conclusion  
2) Second pass: method + assumptions + experiments  
3) Third pass: math details + proofs + ablations  
4) Replication pass: implement minimal reproduction or sanity checks

---

## 3) Baselines and implementations
- **Papers With Code**: find standard benchmarks and baseline code.
- **GitHub**: assess code quality:
  - does it have tests?
  - does it specify environment?
  - is it reproducible?

**Rule:** Treat GitHub code as a hint, not a source of truth.

---

## 4) Citation management
- **Zotero** (or similar): store PDFs and BibTeX keys.
- Use consistent citation keys: `AuthorYearVenue_ShortTitle`.

---

## 5) Reproducible experiments
- Log every run with:
  - seed, config hash, git commit, environment version
- Use one tracking system:
  - simple: JSONL logs + Matplotlib
  - advanced: Weights & Biases / MLflow

---

## 6) LLMs as “active reading assistants”
Good uses:
- Ask for a roadmap before reading (prerequisites, definitions).
- Ask for alternative derivations, then verify.
- Ask for test plans and sanity checks.
- Ask for “what would fail if assumption X is violated?”

Bad uses:
- Asking the LLM to “summarize” without reading the paper.
- Accepting citations without checking they exist.
