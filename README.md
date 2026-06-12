# ⚛️ ex-nihilo-matter-factory

> **SINGULARITY-CATALYST Domain · OMNISCIENT CIVILIZATION NEXUS (OCN)**  
> Research framework for first-principles matter synthesis — from quantum field theory to experimental particle generation.

[![CI](https://github.com/GALACTIC-UNION/ex-nihilo-matter-factory/actions/workflows/ci.yml/badge.svg)](https://github.com/GALACTIC-UNION/ex-nihilo-matter-factory/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## Overview

`ex-nihilo-matter-factory` is the research and simulation framework for matter-synthesis processes within the SINGULARITY-CATALYST domain. It models particle generation pathways, tracks energy budgets per synthesis event, and provides a pluggable pipeline for integrating experimental hardware drivers.

> **Safety Dependency:** All synthesis operations are gated on a `NOMINAL` or `ADVISORY` status from [`vacuum-field-monitor`](https://github.com/GALACTIC-UNION/vacuum-field-monitor). No synthesis pipeline may execute without an active, healthy monitor signal.

---

## Core Modules

| Module | Responsibility |
|--------|---------------|
| `SynthesisPipeline` | Orchestrates end-to-end particle generation workflows |
| `EnergyBudgetTracker` | Monitors energy consumption per synthesis event vs. allowance |
| `ParticleRegistry` | Catalogs generated particle types, yields, and decay constants |
| `HardwareDriver` | Abstraction layer for physical synthesis apparatus interfaces |
| `SimulationEngine` | Monte Carlo and QFT-based synthesis path simulation |
| `SafetyGate` | Polls `vacuum-field-monitor` before authorizing any synthesis run |

---

## Directory Structure

```
ex-nihilo-matter-factory/
├── src/
│   ├── pipeline/           # Synthesis pipeline orchestration
│   ├── energy/             # Energy budget tracking
│   ├── particles/          # Particle registry and decay models
│   ├── hardware/           # Hardware driver abstraction
│   ├── simulation/         # Monte Carlo / QFT simulators
│   └── safety/             # SafetyGate — vacuum-field-monitor client
├── docs/
│   ├── synthesis-pathways.md
│   ├── energy-budget-spec.md
│   ├── hardware-interface.md
│   └── api-reference.md
├── tests/
│   ├── unit/
│   ├── integration/
│   └── simulation/         # Simulation validation tests
├── config/
│   ├── synthesis.yaml      # Pipeline configuration
│   ├── energy-limits.yaml  # Per-run energy caps
│   └── hardware.yaml       # Hardware driver config
├── .github/workflows/ci.yml
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

---

## Getting Started

```bash
git clone https://github.com/GALACTIC-UNION/ex-nihilo-matter-factory.git
cd ex-nihilo-matter-factory
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

# Verify vacuum-field-monitor connectivity
python src/safety/check_monitor.py

# Run simulations
pytest tests/simulation/ -v

# Launch pipeline (monitor must be NOMINAL)
python src/pipeline/run.py --config config/synthesis.yaml
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Energy budget overrides and hardware driver changes require `[SAFETY]` review.

## License

MIT — see [LICENSE](LICENSE).

---

*Part of the [OMNISCIENT CIVILIZATION NEXUS (OCN)](https://github.com/GALACTIC-UNION) · SINGULARITY-CATALYST domain*
