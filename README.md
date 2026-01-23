# Case 01: Moskovsky Av (Urban Monitoring Digital Twin)

> [!WARNING]
> **Work in Progress:** This project is currently under active development. Some links and assets may be placeholders.

---

> **Role:** L1 Digital Twin (Urban Monitoring)
> **Stack:** Houdini, Omniverse (USD/Python), Jira Integration

---

## 📋 Project Overview

This repository showcases a prototype **Urban Digital Twin (Level L1)** focused on real-time monitoring and visualisation of urban infrastructure. The case study centres on Moskovsky Avenue 150, demonstrating how procedural workflows and real-time 3D environments can transform traditional city planning and operations.

**Key Use Case:**
The digital twin integrates live transport telemetry to display **real-time bus arrival information** via HUD overlays positioned above "smart" bus stops. This exemplifies how L1 Digital Twins enable one-way data visualisation for operational awareness without requiring bidirectional control systems.

**Project Focus:**

- **Large-Scale Architectural Scenes:** Optimised workflows for handling complex urban environments
- **Procedural Approach:** Houdini-based generation enabling rapid iteration and scalability
- **Smart Urban Fabric:** Integration of IoT-like data streams with 3D spatial context

---

## 🎯 Technical Highlights

*This setup demonstrates an **L1 Digital Twin (Monitoring)**, focusing on one-way data visualisation rather than bidirectional control.*

- **Houdini Proceduralism:** City block generation with optimised USD export pipelines.
- **USD Composition:** Layered architecture (`mesh_`, `mat_`) for real-time Omniverse performance.
- **Custom Extensions:** Python-based visualisation of real-time telemetry (Bus Arrivals) on 3D geometry.

## 👁️ Visual Proof: Moskovsky Av. 150

*Evolution of a Digital Twin: From original reference to procedural generation and final Omniverse integration.*

| Original Reference | Houdini Procedural Render | Omniverse Digital Twin |
| :--- | :--- | :--- |
| ![Original](docs/img/Moskovskiy_av_150/msk_150_original.jpg) | ![Houdini Render](docs/img/Moskovskiy_av_150/msk_150_render.jpg) | ![Omniverse](docs/img/Moskovskiy_av_150/msk_150_omniverse.jpg) |
| *Real-world urban context* | *Procedural geometry & shading* | *Real-time visualisation & FUI* |

## 🏗️ Architecture & Decisions

This project follows a **README-driven structure** to manage the complexity of hybrid Houdini/Omniverse pipelines.

- [**View Architecture Decision Records (ADR)**](docs/adr/) – Design notes on Naming Conventions, Security Guardrails, and Dependency Locking.

## 📂 Repository Structure

```text
.
├── docs/        # ADRs and knowledge base
├── plans/       # Implementation plans & tech debt
├── src/         # Core logic and scripts
├── tests/       # Validation and testing suite
└── tools/       # Internal pipeline utilities
```

---

## 💾 Project Data / Assets

To keep this repository lightweight (GitHub < 1GB), heavy binary assets are stored externally.

- [**Download Heavy Assets (One Drive / S3 Link TBD)**](https://example.com/placeholder)
  - Includes: `*.usd`crates, `*.hip` source files, and high-res textures.

## 🛠️ Setup & Installation

1. **Clone:** `git clone https://github.com/MSP014/dt-omniverse-showreel-case01-msk.git`
2. **Env:** Create conda env: `conda create -n case01-env python=3.10`
3. **Deps:** `pip install -r requirements.txt`
4. **Hooks:** `pre-commit install`

---

## 📜 Changelog

- **2026-01-22:** Initial repository bootstrap. Established **Nvidia Showreel Protocol** (ADRs, Pre-commit, Hybrid Access).
