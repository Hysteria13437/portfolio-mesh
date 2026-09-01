# Portfolio Mesh

A centralized index and architectural breakdown of my active web deployments,
community hubs, open hardware reference platforms, and browser-based game
systems. Everything here is self-hosted, tracking-light, and built to keep
running on modest hardware for years rather than quarters.

---

## 🌐 Project Catalog & Deep Dives

### ⚔️ [hellasonline.xyz](https://hellasonline.xyz/)
A persistent, text-and-map strategy MMO set in a stylized ancient Greek world.
Heavily inspired by the slow-burn web strategy games of the 2000s (Travian,
Ikariam, OGame), it is built around a strict anti-pay-to-win, zero-FOMO,
ad-free philosophy: permanently free, no premium queues, and no server resets
that wipe a player's progress.

*   **Core Systems & Gameplay Loops:**
    *   *Sovereignty & Production:* Players found cities on islands and grow
        micro-economies across 6 resource streams (Sawmill, Marble Quarry,
        Crystal Mine, Sulfur Pit, Vineyard, and Marketplace Gold), with
        research trees that modify output, military capacity, and map vision.
    *   *Strategic Commitment:* A multi-tier military spanning a 20+ ground
        unit roster and a separate naval branch. Movement runs on real-world
        hour scales, so long-range attacks, colonizations, and reinforcement
        orders are genuine commitments rather than instant actions.
    *   *The Political Layer:* Kingdoms, territory control, menhirs, robber
        camps, formal war declarations, and kingdom-wide votes. A custom
        community node at `forum.hellasonline.xyz` carries treaties,
        recruitment, and post-battle analysis.
*   **The Technical Architecture:**
    *   *The Stack:* Written end-to-end in TypeScript, React on the front end,
        Fastify + Prisma on the API layer, PostgreSQL for durable state.
    *   *The Ticking Core:* A background architecture on Redis and BullMQ
        orchestrates high-concurrency asynchronous work: resource-generation
        curves, construction and training queues, movement resolution, and
        combat. Every economy-mutating path is transaction-guarded with row
        locks and delta writes, hardened across repeated multi-agent security
        and race-condition audits.
    *   *Real-time Sync:* Socket.io pushes construction-complete, battle-report,
        and messaging events to the client the moment a worker finishes. The
        whole system runs on a single unmanaged VPS in Helsinki, Finland.

---

### 🚀 [standingorders.xyz](https://standingorders.xyz/)
A persistent, browser-based space MMO sandbox and economy simulation built
around a living server. Markets drift, asteroid belts deplete, and pirate and
police factions keep acting whether or not the player is logged in.

*   **The Sector & Faction Architecture:** A hand-charted 15-system universe
    connected by jump gates and split into security zones:
    *   *Core Worlds (Sol, Vega, Ceres):* High-security, low-margin industrial hubs.
    *   *The Frontier (Kepler, Helios, Tortuga):* High-yield mining systems with
        active pirate raiding.
    *   *The Reaches (Erebus, Styx, Nyx):* Low-security fringe sectors seeded
        with deep-space signals and scrap wrecks.
    *   *The Blackreach (Scourge, Malice, Wraith, Blight, Ruin, Husk):* A
        lawless six-system ring with no station authority. It is the only place
        to harvest volatile *Umbral Ore*, which then has to be smuggled back to
        policed space to sell.
*   **The Gameplay Loop Engines:**
    *   *Dynamic Commerce:* Per-station supply-and-demand pricing that moves
        with aggregate trade.
    *   *Space Mining & Combat:* Direct flight with directional thrusters,
        mining lasers, and cargo collection, against continuously generated
        sector threats.
*   **Technical Implementation:** Zero-install in the browser. A Vite +
    TypeScript + Three.js client renders the sector over WebGL; a Fastify +
    WebSocket server runs a 15 Hz authoritative tick, with the same physics
    integrator on both ends for client-side prediction and soft server
    reconciliation. Credits and cargo persist per pilot name.

---

### 💻 [vbuilds.xyz](https://vbuilds.xyz/)
*Formerly CoreChronicle.* A zero-bloat, ad-free reference manual and parts
sandbox for PC builders. It is a lightweight alternative to retail spec pages,
prioritizing clean data and functional clarity, and is fully localized in
five languages (English, Finnish, Hebrew, Spanish, French).

*   **The Component Engine:** An expanding database across 8 categories (GPUs,
    CPUs, Motherboards, RAM, Storage, PSUs, Coolers, Cases), with architectural
    breakdowns that track current pipelines such as AMD's Zen 5 3D V-Cache
    (Ryzen 7 9800X3D) and NVIDIA's Blackwell (RTX 5090).
*   **The Compatibility Checker:** A slot-by-slot configurator that
    cross-references physical, electrical, and thermal dependencies in real
    time. It flags socket mismatches (for example Arrow Lake against LGA1851),
    runs cooler-clearance and case form-factor checks, and tallies cumulative
    system power draw against a target PSU.
*   **The Resource Hub:** Multi-chapter tutorials covering the full lifecycle
    of hardware ownership: physical assembly, thermal paste, BIOS navigation,
    memory tuning (XMP/EXPO), and conservative overclocking.

---

### 🐢 [talkativeturtles.club](https://talkativeturtles.club/)
A community discussion board built around a high-signal, zero-algorithm ethos:
a place for software engineers, hobbyist hackers, hardware builders, and
sysadmins to talk shop without corporate tracking or engagement farming.

*   **The Infrastructure Stack:** A tuned MyBB install behind a text-first,
    responsive dark theme aimed at night-mode terminal users, with optimized
    asset loading and a fast, accessible archive layout. Self-hosted, no
    third-party forum SaaS.
*   **The Technical Forums:** Partitioned by dense technical domain:
    **Programming & Development** (algorithms, debugging, version control),
    **Operating Systems & Linux** (shell scripting, configuration),
    **Microcontrollers & Electronics** (ESP32 deployments, custom PCBs,
    Raspberry Pi), and **Networking & Cybersecurity** (self-hosting, home
    labs, firewalls).

---

### 🖼️ [wallpapertrove.org](https://wallpapertrove.org/)
A high-throughput media directory and image discovery platform built around
fast content delivery. It organizes a curated catalog of over 38,000 HD and 4K
assets with no tracking scripts and no aggressive sign-up wall.

*   **Categorization & Asset Sorting Engine:** Indexes backgrounds into 22
    specific genres (Cyberpunk, Steampunk, Pixel Art, Minimalist, Sci-Fi,
    Surrealism, and more). The platform reads image dimensions and separates
    widescreen desktop ratios from vertical mobile viewports so visitors can
    filter cleanly between them.
*   **Storage & Ingestion Pipeline:** Community uploads up to 50MB per file,
    stored losslessly (.jpg, .png) with a minimum 1920x1080 quality threshold.
*   **Real-Time UI Updates:** An asynchronous front-end layer pushes new
    entries to active clients through a subtle banner, with no full-page
    refresh.

---

### 🧰 [toolbit.online](https://toolbit.online/)
A developer dashboard hosting web-accessible utilities, parsers, and network
diagnostics, so you can reach for a quick tool without pulling untrusted
packages onto a local machine. Express.js and SQLite behind account auth.

*   **Web Utilities Array:** Standalone client-side tools with instant output:
    cron-expression building and explanation, encoding and decoding (Base64,
    URL, JWT inspection), hashing, text and JSON manipulation, QR-code
    generation, and a URL shortener.
*   **Feeds & Tracking:** A built-in RSS reader, plus lightweight monitoring
    and metrics utilities for keeping an eye on your own services.

---

### 🕹️ [Arcade](https://arcade.vercel.app/)
A single static site collecting the browser games I build on the side. No
launcher, no account, nothing to install; each game runs entirely client-side
and saves progress to local storage on the device. Two titles are finished
enough to sit down with, the rest are in active development and published so
their progress is visible.

*   **Playable Now:**
    *   *Foundry of Fate:* A turn-based fantasy RPG plus city management. Run
        one hero and one walled city day by day: staff the foundry, train an
        army, take quests, survive the seasons. Vanilla JS, no build step, with
        the game rules isolated in a pure engine the presentation layer only
        reads from.
    *   *Kebab Tycoon:* An idle tycoon. Compound a single grill into a
        franchise through recipes, upgrades, and staff automation; it keeps
        earning while the tab is closed.
*   **In Development:**
    *   *Foundry of Fate 3D:* the Foundry city rebuilt as a low-poly Three.js
        world placed building by building, with day/night and seasons.
    *   *NEON VOID:* a Babylon.js cyberpunk block to drive and walk around,
        with a wanted system, pedestrians, and flying traffic.
    *   *Brainrot Launcher:* a cabinet of 20 short arcade games behind one menu.
    *   *Stellar Mandate:* a text and ASCII space 4X rendered in the browser
        through xterm.js.
*   **Technical Implementation:** Every game folder is served at its own path
    from one static deployment on Vercel; `main` deploys on push. Uncommitted
    work is snapshotted to a dedicated branch every few minutes with a secret
    scan in the loop, so nothing local is ever more than one interval from
    being backed up off-machine.

---

## 🛡️ Privacy, Sovereignty & Design Philosophy
*   **Data Ownership:** No Google Analytics, no Facebook Pixels, no
    behavioral-ad SDKs. GDPR-aligned by construction, with zero-retention
    infrastructure and immediate account purging on request. (The Arcade uses
    Vercel's cookieless, non-fingerprinting page-view counts and nothing else.)
*   **Infrastructure Minimalism:** No sprawling opaque cloud tiers. The core
    platforms are deployed directly to bare metal or single virtual private
    servers, managed with plain Linux sysadmin practice. The static Arcade is
    the one exception, and only because static hosting has no server to own.
*   **No Pay-To-Win, No FOMO:** Software should respect a user's time and
    money. No microtransactions, premium queues, time-gated grind, or
    engineered scarcity anywhere in the catalog.

---
*Maintained with coffee and Linux terminals.*
