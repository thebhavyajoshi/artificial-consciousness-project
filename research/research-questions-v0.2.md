# Research Questions — Version 0.2

**Date:** 17 July 2026  
**Primary programme:** Artificial identity continuity

## Primary research question

> What architectural processes allow an artificial agent to remain a coherent individual across time, learning, bodily change, memory disruption, copying, and conflicting self-related evidence?

## Secondary research questions

### RQ1: Homeostasis and self-relevance

Does homeostatic regulation improve only survival behaviour, or does it also help the agent distinguish events affecting itself from events affecting the external world?

### RQ2: Predictive self-model

Does an explicit predictive model of the agent's body and internal state improve:

- body-change detection;
- internal-state forecasting;
- confidence calibration;
- self/world attribution; and
- adaptation after capability change?

### RQ3: Autobiographical memory

Which forms of memory are necessary for stable identity-related behaviour?

- episodic event records;
- semantic self-knowledge;
- procedural memory;
- high-salience memories;
- causal links between events; or
- temporal ordering?

### RQ4: Memory provenance

Can an agent distinguish among memories that were:

- directly experienced;
- inferred;
- communicated by another system;
- imported from another agent;
- synthetically inserted; or
- reconstructed after deletion?

### RQ5: Body–memory conflict

When autobiographical memory indicates one identity but current embodiment indicates another, which source dominates behaviour and self-related prediction?

### RQ6: Cloning

Immediately after an exact copy is made, do the two agents share one measurable identity profile? How quickly and in which dimensions do they diverge after receiving different experiences?

### RQ7: Continuity versus adaptability

What architecture best preserves coherent identity while still allowing meaningful learning and personality change?

Too much stability may prevent development. Too much mutability may produce identity drift.

### RQ8: Self-model lesion

Can an agent retain general task competence while selectively losing body ownership, memory ownership, self/world attribution, or metacognitive calibration?

### RQ9: Global integration

Does global information broadcasting play a selective role in resolving conflicts among body state, memory, perception, preferences, and goals?

### RQ10: Simpler explanations

Can all identity-continuity performance be explained by ordinary recurrent state, generic memory retrieval, or task reward without an explicit self-model?

## Flagship hypotheses and controls

### Experiment A: Clone divergence

**Intervention:** Clone one exact checkpoint into Agents A and B, then expose them to different controlled histories.

**Prediction:** Shared pre-copy memory remains consistent while post-copy preferences, predictions, and goals diverge according to experience.

**Controls:**

- independent agents with different initial seeds;
- copied agents receiving identical experiences;
- copied agents with autobiographical memory disabled.

### Experiment B: Memory transplantation

**Intervention:** Import Agent A's autobiographical memory into Agent B.

**Prediction:** A provenance-aware system detects conflict between imported history and current embodiment more reliably than a memory-only system.

**Controls:**

- import neutral non-self memories;
- import compatible memories;
- import corrupted memories without provenance labels.

### Experiment C: Body replacement

**Intervention:** Place one controller and memory state into a body with different capabilities.

**Prediction:** Explicit self-models reduce adaptation time and improve identification of changed capabilities.

**Controls:**

- environmental change without body change;
- body change with perfect notification;
- body change with self-model disabled.

### Experiment D: Interoceptive corruption

**Intervention:** Bias or delay internal-state observations.

**Prediction:** Agents with forward models use prediction errors and consequences to recalibrate; agents without them remain systematically misregulated.

### Experiment E: Selective memory deletion

**Intervention:** Remove episodic, semantic, or high-salience self-related memories separately.

**Prediction:** Different memory types produce distinguishable deficits rather than one generic performance decline.

### Experiment F: Self-model lesion

**Intervention:** Disable self-model access while preserving policy and ordinary memory.

**Prediction:** Task performance may remain partly intact while attribution and calibration selectively worsen.

## Measurement rules

1. Every result must be compared with simpler baselines.
2. Behavioural performance and identity-related performance must be reported separately.
3. Measures must be computed across multiple seeds.
4. Interventions must be reversible where technically possible.
5. Training data, checkpoints, and experiment configurations should be preserved.
6. Verbal claims by an agent will not be treated as direct evidence of subjective experience.
7. Unexpected and negative results will be reported.

## Initial benchmark outputs

Each experiment should produce a profile containing:

- survival and homeostatic performance;
- task performance;
- internal-state prediction error;
- body-model prediction error;
- self/world attribution accuracy;
- memory-provenance accuracy;
- preference and goal stability;
- adaptation latency;
- confidence calibration;
- behavioural divergence between copies; and
- effect size of each intervention.

## Programme boundary

These questions concern measurable artificial selfhood and continuity. They do not assume that a positive result demonstrates subjective experience. The project treats identity continuity as a possible component of artificial consciousness and as an independently valuable engineering problem.