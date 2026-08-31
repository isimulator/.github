# iSimulator

**A practical open source enterprise architects simulation simulation engine built to leverage digital twin models of real enterprise architecture entities.**

iSimulator is a generic, extensible platform that lets digital architects (and domain experts) model, contextualize, and simulate the behavior, operations, and control of specific entities—without requiring deep programming expertise.

---

## What is iSimulator?

iSimulator is an **entity-centric digital simulation engine**.

You start with a **digital twin** of a real-world entity (a machine, a process, a vehicle, a facility, an organisation, a system of systems, etc.). You then describe:

- How that entity behaves
- What operations it performs
- How it is controlled
- The temporal rules and constraints that govern it
- The operational environment and semantics that give those behaviors meaning

From there, iSimulator lets you run simulations that respect the entity’s real semantics, timing, and control logic.

It is deliberately designed as a **friendly, utilitarian platform**—not a research toy or a heavyweight enterprise system. The goal is to make serious simulation accessible to people who understand the domain, even if they are not software engineers.

---

## Core Intent

iSimulator exists to help people **contextualize problem spaces** through simulation.

Most simulation tools either:

- Force users into low-level code and mathematical formalisms, or
- Abstract everything into generic “agents” and “events” that lose the real meaning of the entity being studied.

iSimulator takes a different path:

1. **Anchor everything in a digital twin of a concrete entity.**
2. **Capture the entity’s own semantics, behavior, operations, and control models.**
3. **Add temporal stipulations and operational constraints** that reflect how the entity actually works in its environment.
4. **Enable simulation that remains faithful to that context.**

The platform is intended as an **ongoing project**—a living foundation that digital architects can continually refine as their understanding of the problem space deepens.

---

## Foundational Sources

iSimulator does not invent its semantic or organisational foundations from scratch. It draws deliberately on two complementary open efforts that address different layers of the problem space:

### World Semantic Foundation (WSF)

[World Semantic Foundation](https://github.com/World-Semantic-Foundation) provides a rigorous, type-safe semantic engine and a 38-concept vocabulary spanning Entity, Concept, Relationship, Event, State, Time, Space, Organisation, Process, Function, Activity, Goal, Policy, Rule, Constraint, Actor, and more.

WSF supplies:

- A formal upper ontology and relationship model suitable for digital twins
- Validation (SHACL), inference, provenance, and audit capabilities
- Explicit architectural attention to digital twins and simulation (ADR-WSF-27)
- A clean separation of concepts, relationships, assertions, and temporal validity

For iSimulator, WSF is the natural candidate for the **generic semantic backbone**: the shared language in which entity identity, semantics, behavior, control logic, and temporal stipulations can be expressed and validated.

### OpenDEAM (Open Digital Enterprise Architecture Model)

[OpenDEAM](https://github.com/technehub-labs), from TechNeHub Labs, is an open reference framework for Digital Enterprise Architecture and Digital Business Ecosystem Architecture.

It supplies:

- Architecture layers (L1–L5), building blocks, and entity allocation
- A rich set of reference catalogs (Actors, Business Capabilities, Business Objects, Controls, Metrics, Blueprints, Guardrails, Concepts, etc.)
- Strong temporal and lifecycle modelling (Baseline / Current / Target / Transition / Scenario states, snapshots, deltas)
- A governance and decision loop (Intent → Objective → Policy → Decision → Action → Change → Outcome)
- Machine-readable metamodels and conformance levels

When the entity being modelled is an **organisation** or a digital business ecosystem, OpenDEAM provides the specialised vocabulary, catalogs, and lifecycle patterns that make organisational simulation concrete and usable by enterprise architects.

### How they fit together

| Layer | Primary source | Role in iSimulator |
| --- | --- | --- |
| Generic entity semantics, relationships, time, provenance | **WSF** | Semantic backbone for any digital twin |
| Organisation / enterprise structure, capabilities, governance, lifecycle | **OpenDEAM** | Specialised organisational and ecosystem modelling |
| Simulation runtime, scenarios, accessibility | **iSimulator** | Friendly engine that makes the above operational for digital architects and domain experts |

Together they address the core problem iSimulator sets out to solve: enabling meaningful, context-preserving simulation of real entities (including organisations) without forcing users into low-level code or losing domain meaning.

---

## Who It’s For

- **Digital architects** who need to model real entities and their operational realities
- **Domain experts** (operators, engineers, planners, process owners) who understand how something works but are not programmers
- **Enterprise and solutions architects** working with organisational or ecosystem digital twins
- **Teams** that want to explore “what if” scenarios grounded in actual entity behavior rather than abstract models
- Anyone who needs a **practical, readable, and maintainable** way to simulate systems based on digital twins

---

## What You Can Model

iSimulator is built to support:

| Concern | Description |
| --- | --- |
| **Entity semantics** | The meaning, roles, states, and identity of the specific entity |
| **Behavior** | How the entity acts and reacts under different conditions |
| **Operations** | The concrete actions and processes the entity can perform |
| **Control models** | Rules, policies, feedback loops, and decision logic that govern the entity |
| **Temporal stipulations** | Timing, durations, sequences, deadlines, and time-dependent constraints |
| **Operational environment** | The context, resources, interactions, and external conditions that shape behavior |
| **Organisation & ecosystem** | Structure, capabilities, governance, lifecycle, and decision loops (drawing on OpenDEAM) |

These are not bolted-on features. They are first-class concepts in the engine so that simulations remain meaningful and inspectable.

---

## Design Principles

- **Entity-first** — Everything starts from a digital twin of a real entity.
- **Semantic fidelity** — Behavior and operations carry the meaning of the domain, not just abstract state transitions.
- **Accessible** — Non-technical users should be able to configure and run simulations once the digital twin and operational understanding exist.
- **Utilitarian** — Focus on usefulness over theoretical purity. Prefer clarity and practical power.
- **Contextual** — Simulation is a way to deepen understanding of a problem space over time, not a one-shot calculation.
- **Extensible** — The engine is generic so that digital architects can specialize it for different classes of entities and domains.
- **Grounded** — Build on open semantic and architectural foundations (WSF, OpenDEAM) rather than inventing parallel vocabularies.

---

## High-Level Approach

1. **Define or import a digital twin** of the target entity (optionally grounded in WSF concepts and, for organisations, OpenDEAM catalogs).
2. **Describe its operational semantics** — states, behaviors, operations, and control logic in terms that domain experts recognize.
3. **Specify temporal and environmental constraints** that reflect real-world operating conditions (and organisational lifecycle states where relevant).
4. **Configure scenarios** — initial conditions, external events, control inputs, “what-if” variations.
5. **Simulate** and observe outcomes while remaining grounded in the entity’s actual model.
6. **Iterate** — refine the twin, the semantics, or the scenarios as understanding grows.

The platform is meant to support this loop as an ongoing activity, not a single experiment.

---

## Project Status

iSimulator is an **active, evolving platform**.

The current focus is establishing a clean, coherent foundation that:

- Treats digital twins of specific entities as the primary modeling unit
- Makes entity semantics, behavior, operations, control, and temporal rules first-class
- Remains approachable for non-technical domain participants
- Draws on WSF for generic semantic structure and OpenDEAM for organisational / enterprise modelling
- Serves as a reusable engine that digital architects can apply across different problem spaces

This README frames the intent and direction. Concrete architecture, APIs, modeling languages, and tooling will grow from this foundation.

---

## Vision in One Sentence

**iSimulator is a friendly, entity-centric simulation platform that lets people who understand real-world systems explore those systems through digital twins—capturing semantics, behavior, operations, control, and time—so that problem spaces can be contextualized, reasoned about, and improved.**

---

*Built for digital architects. Usable by domain experts. Grounded in real entities and open foundations (WSF + OpenDEAM).*
