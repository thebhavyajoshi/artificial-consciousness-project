# Organism-0

## Status

**Role:** Replication and engineering baseline  
**Originality claim:** None for the basic energy–integrity–fatigue design  
**Immediate objective:** Build a deterministic, tested artificial body and world

## Purpose

Organism-0 is the Artificial Consciousness Project's first runnable digital organism.

It will inhabit a partially observable 24 × 24 simulated world and regulate three internal variables:

- energy;
- structural integrity; and
- fatigue.

It will initially have no language model, no internet access, no external tools, and no physical-world control.

## Scientific classification

The literature review shows that Organism-0's foundations have substantial precedents:

- homeostatic reinforcement learning;
- vulnerable and homeostatically regulated machine proposals;
- artificial agents driven by energy, structural-damage avoidance, and rest;
- recurrent embodied agents;
- robot body self-modelling; and
- probing learned self and world representations.

Organism-0 is therefore not presented as an original theory of consciousness.

It is a controlled baseline for:

1. reproducing established mechanisms;
2. validating the project's engineering and experiment infrastructure;
3. creating deterministic checkpoints and interventions;
4. measuring the limits of simpler agents; and
5. providing the body and environment on which Organism-1 will be built.

## Proposed architecture

Organism-0 combines:

- homeostatic valuation;
- recurrent integration across time;
- a predictive model of its own future body state;
- limited event memory;
- measurable functional precursors such as threat, relief, curiosity, frustration, and confidence; and
- matched baselines and ablation experiments.

Any autobiographical memory implemented in Organism-0 will remain minimal. The full identity-continuity memory system belongs to Organism-1.

## Blueprint

1. [World, body, senses, actions, and homeostatic valuation](01-world-body-and-valuation.md)
2. [Cognitive architecture, comparison agents, experiments, and metrics](02-cognitive-architecture-and-experiments.md)
3. [Technology stack, repository structure, build order, and success criteria](03-stack-build-plan-and-success-criteria.md)

## Immediate implementation objective

Build a deterministic Gymnasium environment called `ArtificialOrganism/Organism0-v0`, together with automated tests and a Pygame renderer.

Neural-network training begins only after the world's mechanics are reproducible and fully validated.

The first implementation must support later intervention research by preserving:

- exact seeds;
- deterministic state transitions;
- structured logs;
- serialisable body and world state;
- reproducible action sequences; and
- versioned configurations.

## Completion condition

Organism-0 is complete as a baseline when:

- the world and body mechanics are deterministic and tested;
- conventional and homeostatic agents can be compared fairly;
- internal-state prediction can be measured;
- controlled body changes can be applied;
- checkpoints can reproduce trajectories; and
- results can be generated across multiple seeds without manual intervention.

## What comes next

[Organism-1](../organism-1/README.md) will add the project's identity-continuity research layer:

- autobiographical memory;
- memory provenance;
- persistent self-modelling;
- deterministic cloning;
- memory transplantation;
- body replacement;
- false memories;
- selective memory deletion; and
- causal module lesions.

## Scientific boundary

Organism-0 is designed to reproduce and test consciousness-related functions. Successful results would not prove subjective experience, sentience, personhood, or an inner life.