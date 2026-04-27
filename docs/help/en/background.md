# Background

This page is a bridge. Phylax stands on an idea ("Living Health"), an architecture (browser-only, encrypted), and an open roadmap. If you want more depth, the substance lives in three places.

## The idea: Living Health

Phylax implements the Living Health concept, a four-part article series by Asterios Raptis. The core thesis: health is a process led by a person, not a state managed by the system.

- Part 1: [Living Health: From Patient to Partner](https://asterios-raptis.medium.com/living-health-from-patient-to-partner-9fff311a8c45)
- Part 2: [Living Health in Practice](https://asterios-raptis.medium.com/living-health-in-practice-d53964053500)
- Parts 3 and 4: translation in progress. The complete German series is at [Lebende Gesundheit, Die Serie](https://asterios-raptis.medium.com/lebende-gesundheit-die-serie-0193f66df9a3).

The four parts cover:

1. Health as a user-led process
2. Self-application: observe, recognize patterns, self-regulate
3. Proxy profiles (older relative, dependent child)
4. AI as a structuring partner, not a diagnostician

## The architecture

Phylax is a pure browser application. No backend, no cloud sync, no telemetry.

- **Data storage:** IndexedDB in the browser, fully encrypted with AES-256-GCM.
- **Key derivation:** PBKDF2 with SHA-256, 1,200,000 iterations, from your master password.
- **Key lifetime:** In memory only, never persisted. Auto-lock after 5 minutes of inactivity (configurable) clears the key.
- **Tech stack:** React 18, TypeScript, Dexie.js (IndexedDB wrapper), Web Crypto API, Tailwind CSS, vite-plugin-pwa.

Architectural decisions are documented as ADRs (Architecture Decision Records) in the repository.

## Threat model in one sentence

Phylax protects against: a stolen device with the app locked, curious bystanders, cloud breaches (no cloud), telemetry leaks (no telemetry).

Phylax does not protect against: keyloggers on the device, a compromised operating system, a weak master password, physical coercion, browser exploits.

## Why no backend

Data sovereignty. As soon as data is stored anywhere that is not your own device, it is potentially accessible to others (database leaks, vendor access, compelled disclosure). Phylax avoids this by having no backend at all.

That has costs: no automatic device sync, no cross-device login, no centralized recovery. These costs are intentional and inseparable from the concept.

## Source code and roadmap

Phylax is open source.

- Repository: [github.com/astrapi69/phylax](https://github.com/astrapi69/phylax)
- License: MIT
- Current status and phase plan: [ROADMAP.md](https://github.com/astrapi69/phylax/blob/main/docs/ROADMAP.md)
- Concept document: [CONCEPT.md](https://github.com/astrapi69/phylax/blob/main/docs/CONCEPT.md)
- Architecture decisions: [docs/decisions/](https://github.com/astrapi69/phylax/tree/main/docs/decisions)

## This documentation

The documentation you are reading lives in its own repository:

- [github.com/astrapi69/phylax-docs](https://github.com/astrapi69/phylax-docs)

Corrections, missing topics or translation requests are taken there as issues or pull requests.

Status: 2026-04-27 (Iteration 1, first content)
