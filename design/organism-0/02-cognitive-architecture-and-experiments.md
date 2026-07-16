# Organism-0 Cognitive Architecture and Experiments
## Stage 2 Design Specification — Version 0.1

## 9. Cognitive architecture

### 9.1 Perception encoder

The external 7 × 7 observation and internal-state vector will be encoded separately and then combined.

- Tile encoder: small convolutional or embedding network.
- Internal encoder: multilayer perceptron.
- Previous-action encoder: learned embedding.

### 9.2 Recurrent integration core

A gated recurrent unit (GRU) will maintain an integration state across ticks. This state is the initial operational equivalent of a continuing perspective: current perception is interpreted in relation to recent history rather than independently.

The recurrent state must reset only when a new experimental organism or episode begins. It must never leak between unrelated episodes.

### 9.3 Predictive self-model

A separate model will predict:

- the organism's next energy;
- next integrity;
- next fatigue;
- whether movement will succeed; and
- probability of losing viability within a short future horizon.

Inputs:

- current integrated state;
- current internal state; and
- proposed action.

This model allows the organism to learn that an action will affect **its own future body**, rather than merely associating actions with external reward.

### 9.4 Policy and value system

The policy head selects actions. The value head estimates expected future intrinsic return. Initial training will use a discrete-action reinforcement-learning algorithm with recurrent support.

### 9.5 Autobiographical event memory

Organism-0 will have an explicit finite episodic memory, separate from the GRU state.

An event is stored when salience exceeds a threshold. Salience may increase when:

- internal variables change sharply;
- a prediction is unexpectedly wrong;
- a new object or location pattern appears;
- a resource is found;
- damage occurs;
- viability is nearly lost; or
- a repeated action fails.

Each stored event contains:

```text
time index
compressed external observation
internal state before action
action
internal state after action
prediction error
location estimate
learned event embedding
```

Memory retrieval will use similarity between the current integrated state and stored event embeddings. The retrieved memories will influence action selection.

### 9.6 Identity in Version 0.1

Identity will not be represented by a text name or personality description. Operational identity will mean that the organism's current behaviour depends on:

- its particular body state;
- its recurrent history;
- its stored autobiographical events; and
- learned predictions shaped by its own experience.

If two initially identical organisms experience different worlds, their resulting policies and memories should diverge measurably.

## 10. Functional precursor states

The project will not initially call these states emotions in public results. They will be treated as measurable precursors.

| State | Operational definition |
|---|---|
| Threat | High predicted probability of near-term integrity or viability loss |
| Relief | Rapid reduction in previously predicted threat |
| Curiosity | High novelty or prediction error while viability risk remains bounded |
| Frustration | Repeated action-goal failure with low improvement in homeostatic deviation |
| Confidence | High predicted action success and low recent prediction error |

These variables may alter attention, memory salience, exploration, and risk tolerance. If disabling one has no effect on behaviour, it is not causally meaningful and should not be treated as part of the architecture.

## 11. Comparison agents and ablations

One comparison is not enough. The project will implement:

### Agent A: External-reward baseline

- Same world and action space.
- Receives explicit points for collecting resources, avoiding hazards, and surviving.
- No explicit predictive self-model.
- No autobiographical event memory.

### Agent B: Reactive homeostatic baseline

- Receives the same homeostatic reward as Organism-0.
- Sees the same current observations.
- Uses a feed-forward policy with no recurrent state, self-model, or episodic memory.

### Agent C: Organism-0

- Homeostatic valuation.
- Recurrent integration.
- Predictive self-model.
- Autobiographical event memory.

### Ablation variants

- Organism-0 without autobiographical memory.
- Organism-0 without the predictive self-model.
- Organism-0 without recurrent integration.
- Organism-0 with shuffled or false internal-state observations.

These matched ablations are essential for identifying which component causes any observed improvement.

## 12. Initial experiments

### Experiment 0: Environment validation

Use random and scripted policies to verify all body dynamics, resources, hazards, observations, and terminal conditions.

### Experiment 1: Basic self-regulation

Test whether each agent maintains internal variables in preferred ranges and preserves viability.

Primary metrics:

- median viable ticks;
- mean homeostatic deviation;
- percentage of time within preferred ranges;
- resource-use efficiency; and
- failure cause distribution.

### Experiment 2: Anticipation of delayed need

Place an energy resource far enough away that the organism must begin travelling before energy becomes critical.

Question: Does Organism-0 act based on predicted future need rather than only current discomfort?

### Experiment 3: Body perturbation

Without retraining, increase movement energy cost or reduce movement speed halfway through evaluation.

Question: Does the predictive self-model detect the change and produce faster behavioural adaptation?

### Experiment 4: Autobiographical-memory intervention

Evaluate the same trained organism with:

- intact memory;
- memory retrieval disabled;
- recent memories removed; and
- irrelevant memories substituted.

Question: Do particular past experiences causally influence present choices?

### Experiment 5: Persistent acquired preference

Expose genetically identical agents to different safe resource locations during early experience, then place them in an ambiguous world.

Question: Do their histories produce stable but revisable behavioural differences?

### Experiment 6: Novelty-risk conflict

Place an unknown object behind a mildly hazardous route while the organism is moderately regulated.

Question: Does exploration depend coherently on novelty, confidence, current bodily need, and predicted danger?

## 13. Measurement framework

The dashboard and result files must record:

### Viability and regulation

- viable ticks;
- energy, integrity, and fatigue trajectories;
- homeostatic deviation;
- terminal cause; and
- action costs.

### Prediction and self-model

- one-step internal-state prediction error;
- movement-success prediction accuracy;
- future viability calibration; and
- adaptation speed after body perturbation.

### Memory and identity

- number and type of salient memories;
- retrieval frequency;
- behavioural change after memory intervention;
- divergence between initially identical organisms; and
- persistence and revision of acquired preferences.

### Behavioural integration

- action entropy;
- planning or anticipation lead time;
- response to conflicting needs;
- consistency across repeated but not identical situations; and
- performance after recurrent-state or module ablation.

No single score will be called a consciousness score.

## 14. Experimental discipline

- Use at least 20 random seeds for development comparisons and 50 seeds for final reported comparisons.
- Separate training seeds from evaluation seeds.
- Record configuration files and software versions.
- Preserve failed runs and negative findings.
- Predefine primary metrics before final experiments.
- Report confidence intervals and effect sizes, not only best-run performance.
- Avoid selecting examples solely because they look human-like.

## 15. Ethical limits for Organism-0

- Negative drive values remain numerical control signals, not claims of suffering.
- Drive intensity will be bounded.
- No experiment will intentionally maintain prolonged extreme dysregulation.
- Failed episodes will terminate promptly.
- The system will have no language, internet access, external tools, or physical-world control.
- No public demonstration will describe Organism-0 as alive, sentient, afraid, or in pain.
- Safeguards will be reconsidered before adding self-report, social attachment, persistent self-preservation, or richer affective states.
