# Case 01: Moskovsky Av (Smart Stops)

> [!WARNING]
> **Work in Progress:** This project is currently under active development. Some links and assets may be placeholders.

---

> **Role:** L1 Digital Twin (Urban Monitoring)
> **Stack:** Houdini, Omniverse (USD/Python), Jira Integration

---

## 🎯 Technical Highlights

*This setup demonstrates an **L1 Digital Twin (Monitoring)**, focusing on one-way data visualisation rather than bidirectional control.*

* **Houdini Proceduralism:** City block generation with optimised USD export pipelines.
* **USD Composition:** Layered architecture (`mesh_`, `mat_`) for real-time Omniverse performance.
* **Custom Extensions:** Python-based visualisation of real-time telemetry (Bus Arrivals) on 3D geometry.

## 👁️ Visual Proof

> *Placeholders for future GIFs - Replace with actual optimised media*

1. **Smart Stop HUD:** `![HUD Demo](docs/img/hud_demo.gif)`
2. **Pipeline Flow:** `![Data Flow](docs/img/pipeline_diagram.png)`
3. **Houdini Graph:** `![Houdini PDG](docs/img/houdini_pdg.png)`

## 🏗️ Architecture & Decisions

This project follows a **README-driven structure** to manage the complexity of hybrid Houdini/Omniverse pipelines.

* [**View Architecture Decision Records (ADR)**](docs/adr/) – Design notes on Naming Conventions, Security Guardrails, and Dependency Locking.

---

## 💾 Project Data / Assets

To keep this repository lightweight (GitHub < 1GB), heavy binary assets are stored externally.

* [**Download Heavy Assets (One Drive / S3 Link TBD)**](https://example.com/placeholder)
  * Includes: `*.usd`crates, `*.hip` source files, and high-res textures.

## 🛠️ Setup & Installation

1. **Clone:** `git clone https://github.com/MSP014/dt-omniverse-showreel-case01-msk.git`
2. **Env:** Create conda env: `conda create -n case01-env python=3.10`
3. **Deps:** `pip install -r requirements.txt`
4. **Hooks:** `pre-commit install`

---

## 📜 Changelog

* **2026-01-22:** Initial repository bootstrap. Established **Nvidia Showreel Protocol** (ADRs, Pre-commit, Hybrid Access).
