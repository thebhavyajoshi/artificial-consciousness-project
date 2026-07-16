# Organism-0 Technology Stack, Build Plan, and Success Criteria
## Stage 2 Design Specification — Version 0.1

## 16. Technology stack

### Core language

- Python 3.11 for broad compatibility and straightforward scientific development.

### Environment API

- Gymnasium custom environment interface.
- Environment ID: `ArtificialOrganism/Organism0-v0`.
- Vectorised environments for parallel training after single-environment correctness is verified.

### Learning system

- PyTorch for neural networks.
- TorchRL for recurrent reinforcement-learning components, data collection, replay or on-policy buffers, and experimental flexibility.
- Initial candidate: recurrent PPO. Recurrent DQN remains a fallback if PPO integration creates unnecessary complexity.

### Rendering

- Pygame for the live 2D world and internal-state dashboard.
- Training must also support `render_mode=None` for faster headless execution.

### Scientific tooling

- NumPy for numerical operations.
- pandas for experiment summaries.
- Matplotlib for plots.
- pytest for deterministic environment and dynamics tests.
- YAML configuration files for reproducible experiments.
- CSV or Parquet event logs; no database is needed initially.

### Multi-agent future

PettingZoo may be introduced only when the project reaches social interaction experiments. Organism-0 itself remains single-agent.

## 17. Proposed repository structure

```text
artificial-consciousness-project/
├── README.md
├── design/
│   └── organism-0/
│       ├── 01-world-body-and-valuation.md
│       ├── 02-cognitive-architecture-and-experiments.md
│       └── 03-stack-build-plan-and-success-criteria.md
├── organism0/
│   ├── envs/
│   │   ├── organism0_env.py
│   │   ├── world.py
│   │   ├── body.py
│   │   └── objects.py
│   ├── agents/
│   │   ├── external_reward_agent.py
│   │   ├── reactive_homeostatic_agent.py
│   │   ├── organism_agent.py
│   │   ├── self_model.py
│   │   └── episodic_memory.py
│   ├── training/
│   │   ├── train.py
│   │   └── evaluate.py
│   ├── metrics/
│   │   ├── logger.py
│   │   └── dashboard.py
│   └── configs/
├── experiments/
│   ├── E0_environment_validation/
│   ├── E1_basic_regulation/
│   ├── E2_delayed_need/
│   ├── E3_body_perturbation/
│   ├── E4_memory_intervention/
│   ├── E5_acquired_preference/
│   └── E6_novelty_risk/
├── tests/
└── results/
```

## 18. Build order

### Milestone 1: Deterministic world

Build the grid, objects, body dynamics, observation space, action space, rendering, and tests. No learning agent yet.

**Completion condition:** A scripted organism can move, consume resources, take damage, rest, lose viability, and produce fully reproducible logs.

### Milestone 2: Baseline learning

Train the external-reward and reactive homeostatic agents.

**Completion condition:** Both agents learn behaviour that is clearly better than random, and results can be reproduced across seeds.

### Milestone 3: Recurrent organism

Add recurrent integration and the predictive self-model.

**Completion condition:** Internal-state prediction error decreases and the organism adapts to body perturbations more quickly than matched baselines.

### Milestone 4: Autobiographical memory

Add salient-event storage, retrieval, and memory-intervention tests.

**Completion condition:** Disabling or altering relevant memories produces specific, repeatable behavioural changes.

### Milestone 5: Stage 2 research report

Run initial comparisons and document both positive and negative findings.

**Completion condition:** The repository contains reproducible code, saved configurations, tests, result plots, and a report that makes no unsupported consciousness claims.

## 19. Definition of success for Organism-0

Organism-0 Version 0.1 succeeds if it demonstrates all of the following:

1. It maintains its own internal variables better than random control.
2. It anticipates at least one future bodily need.
3. It predicts the effects of its actions on its own internal state.
4. It adapts after an unannounced change to its body.
5. Its particular autobiographical memories causally influence later behaviour.
6. Identical starting agents develop measurable differences after different experiences.
7. Ablation studies identify which architectural components contribute to these effects.

This would not prove consciousness. It would establish a rigorous platform for studying persistent self-regulating artificial agents and justify moving toward richer embodiment, social interaction, and self-report in later stages.

## 20. Immediate next implementation task

Build only the deterministic `Organism0Env` environment and its automated tests. Do not begin neural-network training until the world and body dynamics are correct, inspectable, and reproducible.

## References for implementation

- Gymnasium custom environment documentation: https://gymnasium.farama.org/main/introduction/create_custom_env/
- TorchRL documentation: https://docs.pytorch.org/rl/stable/
- TorchRL recurrent-policy tutorial: https://docs.pytorch.org/rl/main/tutorials/dqn_with_rnn.html
- Pygame documentation: https://www.pygame.org/docs/
- PettingZoo documentation for later multi-agent stages: https://pettingzoo.farama.org/
