# Code Review Checklist (AI & RL Projects)

## Correctness
- [ ] All critical math is represented in code without sign/shape errors.
- [ ] Deterministic seeding is implemented.
- [ ] Unit tests cover the core logic.
- [ ] No silent NaNs/inf (guards exist).

## Reproducibility
- [ ] Configs are versioned and logged.
- [ ] Git commit hash and environment info are logged.
- [ ] Runs can be reproduced with a single CLI command.

## Engineering quality
- [ ] Type hints used consistently.
- [ ] Clear module boundaries (no giant script).
- [ ] Helpful error messages and assertions.
- [ ] Minimal, well-documented dependencies.

## RL-specific
- [ ] Training and evaluation are separated.
- [ ] Multiple seeds and confidence intervals are reported.
- [ ] Reward scaling / normalization decisions documented.
- [ ] Safety constraints (if any) are monitored.

## AI/LLM-specific
- [ ] Data leakage checks exist.
- [ ] Tokenization and label shift are correct.
- [ ] Baselines and ablations are clear.
- [ ] Evaluation metrics match the task.
