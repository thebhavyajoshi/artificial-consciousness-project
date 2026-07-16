# Artificial Consciousness Project

**Founder:** Bhavya Joshi  
**Status:** Stage 2 — Organism-0 design complete; implementation next  
**Current version:** 0.1  
**Started:** 17 July 2026

## Mission

To investigate whether artificial systems can develop genuine consciousness, individual identity, emotions, and a continuous sense of existence.

This project does not assume that consciousness can be created simply by making language models larger or better at conversation. It explores whether consciousness-like properties could emerge in an artificial organism that:

- exists continuously;
- regulates its own internal condition;
- experiences a world through a persistent body or embodied simulation;
- distinguishes itself from its environment;
- maintains autobiographical memory;
- forms persistent preferences and relationships;
- integrates perception, memory, emotion, and planning;
- models itself as the subject of its experiences; and
- changes through its own history.

## Core research question

> Can a continuously operating artificial agent develop consciousness-like properties when its continued stability, self-model, embodied perspective, functional emotions, and autobiographical identity are causally connected?

## Stage 1: Foundational thesis

Stage 1 defines the project's working definition of consciousness, research hypothesis, first questions, falsification criteria, and ethical principles.

- [Foundational Research Thesis, Version 0.1](research/foundational-thesis-v0.1.md)
- [Research Ethics and Welfare Principles](ethics/research-principles.md)

## Stage 2: Organism-0 blueprint

Organism-0 is the project's first experimental digital organism. It will live in a partially observable 24 × 24 simulated world and regulate energy, structural integrity, and fatigue.

It will initially have no language model, internet access, external tools, or physical-world control.

Its proposed architecture combines:

- homeostatic valuation;
- recurrent integration across time;
- a predictive self-model;
- autobiographical event memory;
- measurable functional precursor states; and
- comparison agents and matched ablations.

Read the complete Stage 2 blueprint:

- [Organism-0 blueprint index](design/organism-0/README.md)
- [World, body, senses, actions, and valuation](design/organism-0/01-world-body-and-valuation.md)
- [Cognitive architecture and experiments](design/organism-0/02-cognitive-architecture-and-experiments.md)
- [Technology stack and build plan](design/organism-0/03-stack-build-plan-and-success-criteria.md)

## First implementation milestone

Build a deterministic Gymnasium environment called `ArtificialOrganism/Organism0-v0` with:

- reproducible seeded worlds;
- body and homeostatic dynamics;
- partial observations;
- seven discrete actions;
- a Pygame renderer;
- structured event logs; and
- automated tests.

Neural-network training will begin only after the world's mechanics are correct, inspectable, and reproducible.

## Scientific position

This project does **not** claim that current AI systems are conscious or that its proposed architecture will necessarily produce consciousness.

The working position is:

> Consciousness may require more than intelligence and language. It may arise from the interaction of self-regulation, embodiment, integrated processing, autobiographical identity, emotional valuation, and a persistent model of the self.

This is a research hypothesis to be tested, challenged, and revised.

## Repository structure

```text
artificial-consciousness-project/
├── README.md
├── research/
│   └── foundational-thesis-v0.1.md
├── ethics/
│   └── research-principles.md
├── design/
│   └── organism-0/
│       ├── README.md
│       ├── 01-world-body-and-valuation.md
│       ├── 02-cognitive-architecture-and-experiments.md
│       └── 03-stack-build-plan-and-success-criteria.md
└── experiments/
    └── README.md
```

## Collaboration

The project will eventually require contributors in machine learning, reinforcement learning, artificial life, robotics, cognitive science, computational neuroscience, philosophy of mind, and AI ethics.

The immediate priority is to build one measurable artificial organism before making broader claims.

## Author

**Bhavya Joshi**  
Founder and project lead
