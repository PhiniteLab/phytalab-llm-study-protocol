# Theorem → Implementation → Production Pipeline (AI & RL)

This is a practical pipeline that connects theory to working, production-grade code.

---

## Stage 0 — Problem specification
Write:
- problem statement
- success criteria
- constraints (compute, latency, dataset, safety)
- assumptions

Artifacts:
- `templates/json/topic_card.template.json` (fields: goal, constraints, assumptions)

---

## Stage 1 — Formalization
### RL
Define the MDP:
- state space \(\mathcal{S}\), action space \(\mathcal{A}\)
- transition \(P(s'\mid s,a)\)
- reward \(r(s,a)\)
- discount \(\gamma\)
- policy \(\pi(a\mid s)\)

### AI/ML
Define:
- data distribution and split
- model family and parameterization
- objective function
- evaluation metrics

---

## Stage 2 — Theory (theorems, proofs, invariants)
Minimum output:
- One theorem statement with assumptions
- Proof outline (or full proof if needed)
- Invariants that the algorithm relies on

Artifacts:
- `templates/json/theorem_record.template.json`

---

## Stage 3 — Derivation to algorithm
Convert the math to pseudocode:
- clearly define inputs/outputs
- state complexity and memory costs
- list failure modes (numerical instability, divergence)

Artifacts:
- `templates/md/Topic_DeepDive_Template.md` (Algorithm section)
- `templates/json/implementation_plan.template.json`

---

## Stage 4 — Implementation (professional structure)
Recommended Python layout:
```
src/<project_name>/
  __init__.py
  configs/
  data/
  models/
  algorithms/
  losses/
  envs/
  utils/
  train.py
  eval.py
tests/
pyproject.toml
README.md
```

Minimum engineering requirements:
- type hints everywhere
- deterministic seeding
- config system (YAML/JSON)
- logging to JSONL
- unit tests for critical functions (gradients, tensor shapes, numerical stability)

---

## Stage 5 — Debug mode vs release mode
### Debug mode (local dev)
- enable assertions and shape checks
- log intermediate statistics more frequently
- detect NaNs/inf early
- run on small toy problems first (e.g., tiny MDP, tiny dataset)

### Release mode (shared/reproducible)
- minimal logs but complete run metadata (seed, config, commit)
- stable CLI
- reproducible environment (lockfile)
- clean error handling and informative messages

---

## Stage 6 — Evaluation and experiments
### RL
- evaluate with multiple seeds
- separate training vs evaluation policy
- track: return, episode length, entropy/KL, Q-value stats, grad norm
- perform ablations: reward scaling, exploration, network size

### AI/LLM
- strict train/val/test split with leakage checks
- baselines + ablations
- track: loss curves, accuracy/F1, calibration, perplexity (if LM)

Artifacts:
- `templates/json/experiment_log.template.json`

---

## Stage 7 — Productionization mindset
Even if you don’t deploy, think like production:
- stable interfaces
- versioning of configs and data
- monitoring signals (drift, instability)
- documentation (README + docstrings)

---

## Final check
Before you claim understanding:
- Can you re-derive the key equation without the LLM?
- Can you implement a minimal version from scratch?
- Can you explain the failure modes and how to diagnose them?
