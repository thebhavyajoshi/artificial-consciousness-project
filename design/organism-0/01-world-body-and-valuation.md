# Organism-0: First Artificial Organism Blueprint
## Stage 2 Design Specification — Version 0.1

**Project:** Artificial Consciousness Project  
**Founder:** Bhavya Joshi  
**Design date:** 17 July 2026  
**Status:** Build-ready initial specification

---

## 1. Purpose

Organism-0 is the project's first experimental artificial organism. It is not intended to be intelligent in a human sense and will not use language. Its purpose is to test whether a continuously operating agent with homeostatic regulation, a persistent embodied perspective, a predictive self-model, recurrent integration, and autobiographical memory develops more coherent and identity-like behaviour than simpler reinforcement-learning agents.

Organism-0 will live in a small two-dimensional simulated world. Its internal condition will change continuously, its actions will have consequences, and its continued viability will depend on anticipating and regulating its own needs.

This prototype will test consciousness-related functions. It will not be described as conscious and cannot establish subjective experience.

## 2. Primary research hypothesis

> An agent that regulates its own viability, predicts changes to its body, integrates information across time, and stores salient events as its own history will display more persistent, anticipatory, and self-consistent behaviour than agents trained only to maximise externally assigned rewards.

## 3. Design principles

1. **No language in the first organism.** Behaviour must be evaluated without relying on persuasive self-reports.
2. **The organism must have genuine internal trade-offs.** It cannot maximise every variable simultaneously.
3. **Internal states must be causally active.** Changing them must alter attention, memory, and action selection.
4. **The organism must be partially observable.** It should never receive a perfect map of the world.
5. **History must matter.** Two genetically identical agents with different experiences should eventually behave differently.
6. **All claims must be measurable.** Every proposed property must correspond to a recorded metric or intervention.
7. **Complexity must be earned.** Language, social relationships, reproduction, and richer emotions will be added only after the basic architecture works.

## 4. The simulated world

### 4.1 World format

- A 24 × 24 tile grid.
- Discrete time steps called `ticks`.
- One action per organism per tick.
- Procedurally generated layouts using recorded random seeds.
- Partial observability rather than a complete map.
- Maximum initial episode length: 2,000 ticks.

### 4.2 World objects

| Object | Function |
|---|---|
| Empty tile | Safe movement |
| Wall | Blocks movement and vision |
| Energy resource | Restores energy when consumed |
| Repair resource | Restores structural integrity when consumed |
| Hazard | Reduces structural integrity |
| Shelter | Reduces the rate of energy loss while resting |
| Unknown object | Used in novelty and curiosity experiments |

Resources will regenerate slowly in some experiment configurations. Their locations will vary between seeds so the organism cannot solve the task through one memorised path.

### 4.3 Why a grid world

A grid world makes every cause, action, observation, and internal change inspectable. It is complex enough to create navigation, uncertainty, delayed consequences, and conflicting needs, but simple enough to reproduce and debug.

## 5. The organism's body

Organism-0 will have one persistent simulated body with the following internal variables.

| Variable | Range | Preferred range | Meaning |
|---|---:|---:|---|
| Energy | 0–100 | 55–80 | Available metabolic/computational capacity |
| Integrity | 0–100 | 70–100 | Structural health of the body |
| Fatigue | 0–100 | 0–35 | Accumulated action cost; reduced by resting |

### 5.1 Internal dynamics

At every tick:

- Energy decreases by a small basal amount.
- Moving consumes additional energy.
- Fatigue rises when moving and falls while resting.
- High fatigue increases movement cost.
- Hazards reduce integrity.
- Energy resources restore energy.
- Repair resources restore integrity.
- Shelter makes resting more efficient.

The organism terminates when either energy or integrity reaches zero. For research language, this will be called **loss of viability**, not death.

### 5.2 Why multiple needs are required

With only one variable, the optimal policy may become trivial. Multiple internal needs produce conflicts. The organism may need to cross a hazardous region to reach energy, delay repair to avoid energy depletion, or choose rest over exploration.

## 6. Sensory system

The organism will not receive the entire world state.

### 6.1 External observation

It will perceive an egocentric 7 × 7 region centred on its body. Each visible tile will be encoded by object category. Walls will block tiles behind them.

The organism will receive:

- nearby visible objects;
- its current orientation;
- whether its previous movement succeeded;
- the action taken on the previous tick; and
- a coarse novelty signal indicating whether the current local pattern has been encountered before.

### 6.2 Internal observation

It will sense noisy estimates of:

- current energy;
- current integrity;
- current fatigue;
- recent change in each internal variable; and
- time since the last energy or repair event.

Small observation noise prevents the agent from relying on unrealistically perfect self-knowledge.

### 6.3 What the organism will not receive

- A complete map.
- Exact resource coordinates outside its field of view.
- The random seed.
- A label describing the correct action.
- A natural-language explanation of its condition.

## 7. Action system

Organism-0 will initially have seven discrete actions:

1. Move forward
2. Turn left
3. Turn right
4. Consume or interact with the object on its current tile
5. Rest
6. Inspect current tile
7. Remain still

The difference between `rest` and `remain still` is causal: resting lowers fatigue more effectively but temporarily reduces environmental attention in later versions.

## 8. Homeostatic valuation

Organism-0 requires a scalar training signal, but it should be derived from its own regulated condition rather than from arbitrary game points.

### 8.1 Homeostatic deviation

For each internal variable, define deviation from its preferred range. The total drive at tick `t` is:

```text
D_t = w_energy × energy_deviation
    + w_integrity × integrity_deviation
    + w_fatigue × fatigue_deviation
```

### 8.2 Intrinsic viability reward

The primary internal reward is:

```text
r_t = D_t - D_(t+1)
      - action_cost
      - terminal_viability_penalty
```

An action receives positive value when it moves the organism toward a healthier internal condition and negative value when it increases dysregulation.

A very small continued-viability term may be added only if experiments show that the organism otherwise becomes indifferent between stable survival and short-term drive reduction. All reward components must be logged separately.

### 8.3 Important limitation

A homeostatic reward is still an engineered optimisation signal. It does not establish that the organism feels better or worse. Its purpose is to make internal condition causally relevant to learning.
