# RL Starter Project (Student Version)

## Goal
Implement and analyze **two** RL algorithms on a small benchmark suite:
- 1 value-based method (e.g., DQN)
- 1 policy-gradient method (e.g., PPO)

## Required deliverables
1) A topic card for each algorithm:
   - `04_math/<algo>/topic_card.json`
2) A minimal reproducible codebase with:
   - `pyproject.toml`
   - `pytest` tests
   - CLI: `train` and `eval`
3) Experiment logs:
   - multiple seeds
   - learning curves + variance

## Suggested environments
- CartPole
- LunarLander
- MountainCar
- (Optional) simple continuous control tasks if available

## Evaluation
- mean return over N episodes
- sample efficiency (return vs steps)
- stability: variance across seeds
- diagnostics: entropy/KL, Q stats, grad norm

## LLM usage
Use the protocol:
- ask for theorem/derivation, then verify in Sutton & Barto
- ask for implementation plan and tests
- ask for debugging checklists when training diverges

## Ethics
Do not submit LLM-generated code without understanding and attribution.
