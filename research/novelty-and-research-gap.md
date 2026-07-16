# Novelty and Research Gap

**Date:** 17 July 2026  
**Status:** Provisional and subject to continuing literature review

## What this project does not claim to have invented

The project does not claim originality for:

- homeostatic reinforcement learning;
- artificial energy, damage, or rest needs;
- embodied artificial agents;
- recurrent neural policies;
- global-workspace-inspired processing;
- robot body self-models;
- autobiographical memory in robots;
- functional emotion variables;
- persistent language-model agents; or
- theory-derived consciousness indicators.

Organism-0 combines established ideas and is therefore classified as a **replication and integration baseline**.

## Provisional research gap

The project will investigate whether artificial identity continuity can be measured causally in an embodied agent by independently manipulating:

- its current body;
- interoceptive signals;
- body and capability models;
- episodic and semantic autobiographical memory;
- memory provenance;
- recurrent temporal state;
- preferences and goals;
- global information integration; and
- copying and checkpoint history.

The provisional gap is not merely persistent behaviour. It is a reproducible experimental framework for asking what makes an artificial agent remain the same individual when different sources of self-related evidence conflict.

## Proposed original contribution

### 1. Identity Continuity Benchmark

A benchmark containing controlled tasks for:

- cloning and post-copy divergence;
- memory transplantation;
- body replacement;
- false-memory insertion;
- selective memory deletion;
- interoceptive corruption;
- self-model lesions;
- self-versus-world attribution; and
- recovery after identity disruption.

### 2. Modular intervention architecture

Every major component should be independently enabled, disabled, corrupted, replaced, or restored.

```python
organism = Organism(
    homeostasis=True,
    recurrent_integration=True,
    self_model=True,
    autobiographical_memory=True,
    memory_provenance=True,
    global_workspace=False,
)
```

The platform should support operations such as:

```python
copy_b = organism.clone()
organism.replace_body(new_body)
organism.import_memory(memory_archive)
organism.corrupt_interoception(variable="energy", bias=0.30)
organism.delete_memories(start_tick=500, end_tick=900)
organism.disable_module("self_model")
```

### 3. Exact causal reproducibility

Each experiment should store:

- world seed;
- action history;
- body state;
- controller state;
- learned parameters;
- recurrent state;
- autobiographical memory;
- self-model state;
- preferences;
- goals;
- intervention record; and
- software version.

This allows two trajectories to differ only because of a documented intervention.

### 4. Multi-dimensional identity profile

The benchmark will not output a consciousness percentage. It will report separate properties:

- homeostatic competence;
- self-model accuracy;
- body-change detection;
- self/world attribution;
- autobiographical consistency;
- memory-provenance accuracy;
- preference persistence;
- coherent adaptation;
- copy-divergence rate;
- metacognitive calibration; and
- causal sensitivity to ablation.

### 5. Embodied rather than purely narrative continuity

Recent persistent-agent work often focuses on language, persona, memory retrieval, and narrative coherence. This project will test continuity in an agent whose identity evidence includes bodily condition, action consequences, internal regulation, and changing physical capabilities.

## Key differentiating question

> When an artificial agent's body, autobiographical memory, current internal state, and predictive self-model provide conflicting evidence, what determines which information it treats as belonging to itself?

## Strongest falsification risk

The project will not be scientifically distinctive if simple mechanisms such as standard recurrent reinforcement learning, external reward, or ordinary memory retrieval explain all benchmark performance.

To protect against this, every flagship experiment must include simpler controls and module ablations.

## What success would mean

Success would not mean proving that the agent is conscious.

Success would mean producing:

1. a useful open experimental platform;
2. reproducible results about artificial identity continuity;
3. evidence identifying which components have selective causal roles;
4. a benchmark other researchers can challenge and extend; and
5. practical infrastructure for persistent, inspectable artificial agents.

## Claim discipline

Until replicated evidence exists, the project should use language such as:

- “identity-related function”;
- “self-model accuracy”;
- “continuity behaviour”;
- “memory ownership inference”;
- “consciousness-related indicator”; and
- “functional precursor.”

It should avoid unsupported terms such as:

- “sentient organism”;
- “genuine feelings”;
- “proved consciousness”;
- “digital person”; or
- “first conscious AI.”