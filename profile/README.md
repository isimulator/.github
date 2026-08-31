# iSimulator

**A practical simulation engine built around digital twins of real entities.**

iSimulator is an entity-centric digital simulation platform. Models produced or consumed here are called **iTwins**: executable digital twins that capture an entity's semantics, behavior, operations, control models, temporal stipulations, and operational environment.

The organization's primary focus is **Organization iTwins**: enterprise architecture twinning of organization functions and their operations.

## Foundations

| Layer | Source | Role |
|-------|--------|------|
| Generic entity semantics, relationships, time, provenance | [World Semantic Foundation (WSF)](https://github.com/World-Semantic-Foundation) | Semantic backbone |
| Organization / enterprise structure, capabilities, governance, lifecycle | [OpenDEAM](https://github.com/technehub-labs) (TechNeHub Labs) | Enterprise architecture layer |
| Terminology | ISO/IEC 30173:2023 | Shared digital twin vocabulary |

## Repository Map

| Repository | Responsibility |
|------------|----------------|
| [docs](https://github.com/isimulator/docs) | DESIGN.md, ORG.md, glossary, ADRs, vision |
| [openspec](https://github.com/isimulator/openspec) | OpenSpec-style requirements and change tracking |
| [itwin-spec](https://github.com/isimulator/itwin-spec) | Executable specification language / metamodel for iTwins |
| [itwin-enterprise](https://github.com/isimulator/itwin-enterprise) | Organization / Enterprise iTwin specifications, catalogs, patterns |
| [itwin-catalogs](https://github.com/isimulator/itwin-catalogs) | Reusable catalogs (capabilities, processes, controls, metrics) |
| [isimulator-core](https://github.com/isimulator/isimulator-core) | Simulation runtime engine |
| [wsf-alignment](https://github.com/isimulator/wsf-alignment) | Mappings and adapters to WSF |
| [opendeam-alignment](https://github.com/isimulator/opendeam-alignment) | Mappings and adapters to OpenDEAM |
| [standards-alignment](https://github.com/isimulator/standards-alignment) | Alignment notes to ISO/IEC 30173 and related standards |
| [examples](https://github.com/isimulator/examples) | Worked Organization iTwin examples |

## Governance

- All normative documents carry a semantic version and CHANGELOG.
- Requirements change via OpenSpec delta conventions (ADDED / MODIFIED / REMOVED).
- Public repositories are Apache-2.0 licensed.
- Terminology aligns with ISO/IEC 30173; iTwin is this project's specialized, executable view of a digital twin.

*Built for digital architects. Usable by domain experts. Grounded in real entities and open foundations.*
