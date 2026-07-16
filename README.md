# Artificial Consciousness Project

**Founder:** Bhavya Joshi  
**Status:** Research foundation revised; Organism-0 implementation next  
**Current research version:** 0.2  
**Started:** 17 July 2026

## Mission

To build a rigorous experimental science of artificial selfhood and investigate whether artificial systems can eventually develop consciousness, individual identity, emotions, and a continuous sense of existence.

The project does not assume that intelligence, fluent language, or self-reports demonstrate subjective experience.

## Current research focus

> What architectural processes allow an artificial agent to remain a coherent individual across time, learning, bodily change, memory disruption, copying, and conflicting self-related evidence?

The long-term subject remains artificial consciousness. The first tractable and potentially distinctive programme is **artificial identity continuity**.

This includes questions such as:

- What makes an artificial agent remain the same individual over time?
- What happens when its memories and current body disagree?
- Can it distinguish experienced memories from imported or fabricated memories?
- When one agent is copied, when do the copies become different individuals?
- Which continuity functions disappear when its self-model or autobiographical memory is removed?

## Scientific correction

The project's original thesis proposed combining homeostasis, embodiment, self-modelling, integrated processing, functional emotion, and autobiographical memory.

A literature review showed that these individual foundations already have substantial precedents, including:

- homeostatic reinforcement learning;
- vulnerable and homeostatically regulated machine proposals;
- continuous robot body self-modelling;
- autobiographical memory in the iCub robot;
- global-workspace cognitive architectures;
- affective artificial-agent programmes; and
- theory-derived consciousness indicators.

The project therefore does not claim to have invented these ingredients or the basic energy–damage–rest organism design.

## Research documents

- [Foundational Research Thesis, Version 0.2](research/foundational-thesis-v0.2.md)
- [Original Foundational Thesis, Version 0.1](research/foundational-thesis-v0.1.md)
- [Literature Review, Version 0.1](research/literature-review-v0.1.md)
- [Novelty and Research Gap](research/novelty-and-research-gap.md)
- [Research Questions, Version 0.2](research/research-questions-v0.2.md)
- [Research Ethics and Welfare Principles](ethics/research-principles.md)

Version 0.1 remains public to preserve the project's original history. Version 0.2 documents the correction made after reviewing prior work.

## Organism-0: replication and engineering baseline

Organism-0 will be the first runnable digital organism. It will inhabit a partially observable 24 × 24 simulated world and regulate:

- energy;
- structural integrity; and
- fatigue.

It will initially have no language model, internet access, external tools, or physical-world control.

Its purpose is to reproduce and integrate established foundations:

- deterministic embodiment;
- homeostatic valuation;
- recurrent integration;
- internal-state prediction;
- resource seeking;
- hazard avoidance;
- rest behaviour; and
- simple adaptation after body changes.

Organism-0 is essential infrastructure, not the project's main originality claim.

Read its blueprint:

- [Organism-0 index](design/organism-0/README.md)
- [World, body, senses, actions, and valuation](design/organism-0/01-world-body-and-valuation.md)
- [Cognitive architecture and experiments](design/organism-0/02-cognitive-architecture-and-experiments.md)
- [Technology stack and build plan](design/organism-0/03-stack-build-plan-and-success-criteria.md)

## Organism-1: identity-continuity research system

Organism-1 will extend the baseline with:

- autobiographical memory;
- memory provenance;
- an explicit self-model;
- body and capability ownership;
- exact checkpointing and deterministic cloning;
- memory transplantation;
- body replacement;
- false-memory insertion;
- selective memory deletion;
- interoceptive corruption; and
- modular causal lesions.

Read the initial design:

- [Organism-1 identity-continuity blueprint](design/organism-1/README.md)

## Flagship experiments

1. Exact cloning followed by identical or divergent experiences
2. Memory transplantation between bodies
3. Body replacement while preserving memory and controller state
4. False autobiographical memory insertion
5. Episodic versus semantic memory deletion
6. Interoceptive corruption
7. Self-model lesion
8. Global-integration lesion
9. Self-versus-world attribution under conflicting evidence
10. Recovery after restoring earlier checkpoints

## Measurement policy

The project will not create a single “consciousness score.”

It will separately measure properties such as:

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
- causal sensitivity to module ablation.

## Immediate implementation milestone

Build a deterministic Gymnasium environment called `ArtificialOrganism/Organism0-v0` with:

- reproducible seeded worlds;
- tested body and homeostatic dynamics;
- partial observations;
- seven discrete actions;
- a Pygame renderer;
- structured event logs; and
- automated tests.

Neural-network training begins only after the world's mechanics are correct, inspectable, and reproducible.

## Development roadmap

### Stage 3: Build Organism-0

Implement the deterministic world, body mechanics, renderer, logging, and tests.

### Stage 4: Reproduce established foundations

Train conventional and homeostatic agents, implement internal-state prediction, and run baseline body-change experiments.

### Stage 5: Build Organism-1

Implement modular autobiographical memory, self-modelling, checkpointing, cloning, provenance, and interventions.

### Stage 6: Identity Continuity Benchmark

Release experiments, baselines, exact seeds, checkpoints, datasets, metrics, visualisations, and ablations.

### Stage 7: Research and application

Publish technical results and investigate practical infrastructure for persistent, inspectable artificial agents.

## Scientific boundary

This project does **not** claim that current AI systems are conscious or that the proposed architecture will necessarily produce consciousness.

Its current position is:

> Before asking whether an artificial system is conscious, we can experimentally investigate whether it possesses a causally integrated, persistent, and revisable model of itself as one continuing individual.

Positive findings would demonstrate consciousness-related or identity-related functions, not subjective experience, personhood, or moral status.

## Repository structure

```text
artificial-consciousness-project/
├── README.md
├── research/
│   ├── foundational-thesis-v0.1.md
│   ├── foundational-thesis-v0.2.md
│   ├── literature-review-v0.1.md
│   ├── novelty-and-research-gap.md
│   └── research-questions-v0.2.md
├── ethics/
│   └── research-principles.md
├── design/
│   ├── organism-0/
│   │   ├── README.md
│   │   ├── 01-world-body-and-valuation.md
│   │   ├── 02-cognitive-architecture-and-experiments.md
│   │   └── 03-stack-build-plan-and-success-criteria.md
│   └── organism-1/
│       └── README.md
└── experiments/
    └── README.md
```

## Collaboration

The project will eventually require contributors in machine learning, reinforcement learning, artificial life, robotics, cognitive science, computational neuroscience, philosophy of mind, and AI ethics.

The immediate priority is to build a reproducible Organism-0 baseline before making broader claims.

## Author

**Bhavya Joshi**  
Founder and project lead