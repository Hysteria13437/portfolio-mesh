# Portfolio Mesh

A centralized index and architectural breakdown of my active web deployments, community hubs, open hardware reference platforms, and browser-based multiplayer systems.

---

## 🌐 Project Catalog & Deep Dives

### ⚔️ [hellasonline.xyz](https://hellasonline.xyz/)
A persistent, text-and-map strategy MMO set in a stylized ancient Greek world. Heavily inspired by classic slow-burn web strategy games of the 2000s (Travian, Ikariam, OGame), it is explicitly designed around a strict anti-pay-to-win, zero-FOMO, ad-free philosophy with persistent progression.

*   **Core Systems & Gameplay Loops:** 
    *   *Sovereignty & Production:* Players found, expand, and manage micro-economies utilizing 6 basic resource streams (Sawmill, Marble Quarry, Crystal Mine, Sulfur Pit, Vineyard, and Marketplace Gold).
    *   *Strategic Commitment:* Features a multi-tier military structure comprising a 20+ ground unit roster alongside a separate naval branch. Movement mechanics operate on real-world hour scales, making long-distance attacks or reinforce orders deep commitments.
    *   *Diplomatic Subdomains:* Integrates a custom community node at `forum.hellasonline.xyz` handling kingdom treaties, recruitment records, formal war declarations, and tactical post-mortems.
*   **The Technical Architecture:**
    *   *The Stack:* Written end-to-end in TypeScript using React on the frontend, Fastify + Prisma on the backend API layer, and PostgreSQL for structural database state.
    *   *The Ticking Core:* Employs a robust background architecture using Redis and BullMQ to orchestrate high-concurrency, asynchronous long-running worker tasks (resource generation curves, construction queues, combat vector calculations, and real-time battle resolution). 
    *   *Real-time Sync:* Implements Socket.io for immediate server-to-client notifications and messaging states. It runs entirely on a single unmanaged VPS hosted out of Helsinki, Finland.

---

### 🚀 [standingorders.xyz](https://standingorders.xyz/)
A persistent, browser-based space MMO sandbox and economy simulation built around a living server environment. Markets fluctuate, resource nodes deplete, and faction mechanics continuously compute whether the player is actively logged in or away.

*   **The Sector & Faction Architecture:** Manages a hand-charted 15-system universe split into distinct security zones:
    *   *Core Worlds (Sol, Vega, Ceres):* High-security, lower-margin industrial hubs.
    *   *The Frontier (Kepler, Helios, Tortuga):* High-yield mining systems with active pirate raiding protocols.
    *   *The Reaches (Erebus, Styx, Nyx):* Low-security fringe sectors containing deep-space signals and scrap wrecks.
    *   *The Blackreach (Scourge, Malice, Wraith, Blight, Ruin, Husk):* A lawless 6-system ring containing zero station authority. This acts as a high-risk loop—the only place to harvest volatile *Umbral Ore*, which must then be smuggled back to policed sectors to liquidate.
*   **The Gameplay Loop Engines:** 
    *   *Dynamic Commerce:* Real-time supply-and-demand market spreadsheets calculated per station.
    *   *Space Mining & Combat:* Direct vector interaction loops utilizing directional thrusters, mining lasers, and cargo collection mechanics alongside real-time sector threat generation tracking pirate raiders and faction police.
*   **Technical Implementation:** Engineered for zero-install deployment, running an optimized canvas-driven rendering pipeline optimized heavily for Chromium-based hardware acceleration.

---

### 💻 [vbuilds.xyz](https://vbuilds.xyz/)
*Formerly CoreChronicle.* A zero-bloat, ad-free digital reference manual and parts sandbox built specifically for PC enthusiasts and system builders. It serves as a lightweight alternative to retail tracking pages by prioritizing clean specifications and absolute functional clarity.

*   **The Component Engine:** Features an expanding database of components across 8 categories (GPUs, CPUs, Motherboards, RAM, Storage, PSUs, Coolers, Cases). It handles specific architectural breakdowns, tracking modern pipelines like AMD's Zen 5 3D V-Cache (Ryzen 7 9800X3D) and NVIDIA's Blackwell architecture (RTX 5090).
*   **The Compatibility Checker:** A programmatic slot-by-slot configurator that cross-references physical, electrical, and structural dependencies in real-time. It actively flags socket mismatches (e.g., matching Arrow Lake to LGA1851), runs live thermal/cooling space calculations, maps form-factor limits, and tallies cumulative system power draws against target PSU efficiencies.
*   **The Resource Hub:** Hosts a library of multi-chapter tutorials covering the entire lifecycle of hardware ownership—from initial physical assembly and structural thermal paste application to low-level BIOS navigation, memory tuning (XMP/EXPO profiles), and targeted safe overclocking.

---

### 🐢 [talkativeturtles.club](https://talkativeturtles.club/)
A dedicated community discussion board engineered specifically around a high-signal, zero-algorithm ethos. It provides a sanctuary for software engineers, hobbyist hackers, hardware builders, and sysadmins to interact without corporate tracking, distraction, or artificial engagement farming.

*   **The Infrastructure Stack:** Powering the backend is a heavily modified, ultra-fast implementation of **MyBB**, customized via a highly efficient, text-first, responsive dark theme tailored for night-mode terminal users. It utilizes optimized asset loading and an accessible, fast-rendering archive layout.
*   **The Technical Forums:** Structured directly around dense technical domains. It explicitly partitions communities for **Programming & Development** (debugging algorithms, version control), **Operating Systems & Linux** (shell scripting, configuration tweaks), **Microcontrollers & Electronics** (ESP32 deployments, custom PCB design, Raspberry Pi setups), and **Networking & Cybersecurity** (self-hosting infrastructure, home labs, firewalls).

---

### 🖼️ [wallpapertrove.org](https://wallpapertrove.org/)
A massive, high-throughput media directory and image discovery platform designed around lightning-fast content delivery. It aggregates and organizes a catalog of over 38,000 highly curated HD and 4K digital assets without restricting access behind tracking scripts or aggressive sign-up curtains.

*   **Categorization & Asset Sorting Engine:** Dynamically indexes backgrounds into 22 highly specific genres (including Cyberpunk, Steampunk, Pixel Art, Minimalist, Sci-Fi, and Surrealism). The platform automatically reads and segregates dimensions, letting visitors filter seamlessly between widescreen desktop ratios and vertical mobile viewports.
*   **Storage & Ingestion Pipeline:** Supports secure community media uploads up to 50MB per file, ensuring lossless compressed storage formats (.jpg, .png) maintain strict quality standards with a minimum threshold of 1920x1080 resolution.
*   **Real-Time UI Updates:** Implements an asynchronous front-end notification layer where new database entries are pushed instantly to active clients via a subtle layout banner without demanding a full browser window refresh.

---

### 🧰 [toolbit.online](https://toolbit.online/)
An essential developer dashboard hosting web-accessible systems-utilities, parsing scripts, and network diagnostics modules. It serves as an on-demand toolbox for developers needing precise string manipulation, network inspection, or script verification tools without exposing local terminals to untrusted packages.

*   **Web Utilities Array:** Houses standalone client-side applications providing instant output for heavy tasks like secure cron-job formatting expression checking, raw layout manipulation, and localized encoding/decoding.
*   **Network & Automation Trackers:** Contains continuous diagnostics scripts, providing developers with reliable monitoring tools, active system metrics tracking, and live RSS feed management utilities.

---

## 🛡️ Privacy, Sovereignty & Design Philosophy
*   **Absolute Data Ownership:** Fully tracking-free ecosystem. No Google Analytics, no Facebook Pixels, and no behavioral-ad SDKs. True GDPR data compliance backed by zero-retention infrastructure and immediate physical account purging on user command.
*   **Infrastructure Minimalism:** Eschewing bloated, opaque third-party cloud tiers (AWS/GCP), the core platforms are direct-deployed to bare-metal or single virtual private environments via clean Linux systems-administration principles. 
*   **No Pay-To-Win / Anti-FOMO:** Built entirely on the belief that software should respect a user's time and financial boundaries. Core gameplay networks feature no microtransactions, premium queues, time-gated grind cycles, or engineered artificial scarcity.

---
*Maintained with ☕ and Linux terminals.*
