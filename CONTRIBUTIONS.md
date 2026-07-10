# Contributing to Portfolio Mesh

Thank you for your interest in contributing! This ecosystem encompasses open reference libraries, developer utilities, and persistent multi-user network simulations. Because some architectures are closed-source to protect against exploit development, contributions are handled differently depending on the project.

---

## 🗺️ Project Governance & Source Models

Before writing any code, verify the source model of the specific platform you are targeting:

| Project Node | Source Visibility | Direct Code Contributions | Acceptable Pull Requests |
| :--- | :--- | :--- | :--- |
| **vbuilds.xyz** | Open Component / UI | Yes | Bug fixes, component data additions, UI scaling adjustments |
| **toolbit.online** | Open Utilities | Yes | New client-side conversion modules, text parsers, script helpers |
| **talkativeturtles.club** | Custom Modifications | Theme/Styles Only | CSS tweaks, accessibility repairs, layout asset styling |
| **hellasonline.xyz** | Private Core | No (Beta Feedback Only) | Security reports, game balance feedback, bug tracking logs |
| **standingorders.xyz** | Private Core | No (Beta Feedback Only) | Flight vector mechanics analysis, economy bugs, UI edge cases |
| **wallpapertrove.org** | Asset Catalog | Content Submissions | Media uploads are handled directly via the live application interface |

---

## 🛠️ General Contribution Workflow

For the open-source subsystems (UI layers, utility modules, data parsers):

1. **Fork the Repository:** Create a personal fork of the repository and branch off from the main branch.
2. **Implement Local Changes:** Run your code variations locally. Ensure your scripts are written cleanly in native TypeScript/JavaScript ecosystems matching the directory profiles.
3. **Keep Commits Declarative:** Write concise, atomic commit messages detailing exactly what changed (e.g., `fix(vbuilds): correct socket allocation array for LGA1851`).
4. **Issue a Pull Request (PR):** Submit your branch to the staging directory. Clearly articulate the intent, scope of modifications, and verification steps.

---

## 📐 Development & Engineering Standards

To ensure consistency across the mesh nodes, all code contributions must conform to the following architectural benchmarks:

*   **Absolute Minimalism:** No heavy, redundant third-party modules or tracker injections. If a string parsing task or layout element can be written using native Web APIs or lightweight dependencies, do it.
*   **Strict UI Scannability:** Interfaces must remain highly readable, ad-free, responsive, and completely dark-mode accessible for terminal-centric users.
*   **TypeScript Types:** Any modifications touching open TypeScript branches should contain strict data mapping. Avoid falling back to bare `any` declarations.

---

## 🐛 Bug Reports & Issue Tracking

If you find a mechanical failure, rendering bug, or data discrepancy:
*   Open a structured issue inside this repository's tracer tracking board.
*   Provide your exact runtime environment (OS, browser type/version, and hardware acceleration status if reporting simulation performance on `standingorders.xyz`).
*   Include clear step-by-step reproduction instructions and error dumps from the browser console.

---

## 🛡️ Responsible Security Disclosures

Because this network runs live user data, persistent economies, and localized infrastructure nodes, **do not open public issues for security vulnerabilities.**

If you discover a vector for remote code execution, database leakage, authentication bypass, duplication exploits, or script manipulation within any of the live platforms:
1. Document the exploit vector privately.
2. Send an encryption-shielded or direct disclosure report to **privacy@hellasonline.xyz**.
3. Allow reasonable time for internal patch triage and infrastructure hardening before releasing any public post-mortems.

---
*Thank you for helping maintain a sovereign, tracker-free digital space.*
