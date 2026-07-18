<div align="center">

<img src="https://silcrate.com/favicon.svg" width="96" alt="Silcrate app icon — green tile with three terminal bars" />

# Silcrate

**The native Mac home for Apple containers.**

A calm, precise macOS GUI for Apple's open-source [`container`](https://github.com/apple/container) CLI —
containers, Linux machines, images, volumes and networks, all without Docker Desktop.

[![Latest release](https://img.shields.io/github/v/release/keenhatch/silcrate?label=latest&color=1B9A4B)](https://github.com/keenhatch/silcrate/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/keenhatch/silcrate/total?color=14A44A)](https://github.com/keenhatch/silcrate/releases)
![Platform](https://img.shields.io/badge/macOS%2026%2B-Apple%20silicon-2BF06B)

**[Download the latest release](https://github.com/keenhatch/silcrate/releases/latest)** · **[silcrate.com](https://silcrate.com)**

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://silcrate.com/screenshots/hero/hero-dashboard-dark.webp" />
  <img src="https://silcrate.com/screenshots/hero/hero-dashboard-light.webp" alt="Silcrate dashboard: service health, workload tiles and four live resource charts" />
</picture>

</div>

## What it is

Apple quietly shipped a real container engine for macOS: every container runs in its own
lightweight VM on the Virtualization framework, in Swift, optimized for Apple silicon.
Silcrate is its native Mac home — SwiftUI throughout, no Electron, and a hard rule
inherited from day one: **every number on screen is real engine data**.

Docker is the incumbent, OrbStack the fast one, Podman the daemonless one —
**Silcrate is the native one.**

## Highlights

- **Containers** — full lifecycle, single and bulk, with partial-failure reporting;
  exhaustive inspect views; an in-app shell on a real PTY; instant search everywhere
- **Live stats** — CPU, memory, network and block I/O streamed from the engine,
  per container and fleet-wide, in 1m–1h windows
- **Create without flags** — the whole create surface as a form: registry autocomplete,
  resources, env, networks, ports, mounts, capabilities, Rosetta, labels
- **Machines** — persistent Linux environments that boot the image's own init and map
  your home directory in: edit on the Mac, build inside Linux
- **Images** — pull with platform selection, build with BuildKit, inspect decoded OCI
  config and layers
- **Networks** — NAT or host-only, IPv4/IPv6 subnets, delete guards
- **Menu bar mode** — service toggle, live per-container CPU/memory, logs, shell, stop
- **Your terminal** — open a shell in Terminal, iTerm2, Warp, Ghostty, WezTerm or kitty

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://silcrate.com/screenshots/wide/wide-container-stats-dark.webp" />
  <img src="https://silcrate.com/screenshots/wide/wide-container-stats-light.webp" alt="Live container stats: CPU, memory, network and block I/O charts" />
</picture>
</div>

## About this repository

This repository is Silcrate's release home: signed `.dmg` builds, checksums and the
Sparkle update feed ([`appcast.xml`](appcast.xml)). **Silcrate itself is closed
source** — the app's source is not published here. The open-source part is Apple's
[`container`](https://github.com/apple/container) runtime, which Silcrate drives.

Issues are open, and bug reports and feature requests belong here.

## Requirements

- macOS 26 or later, Apple silicon (nested virtualization additionally needs M3+)
- Each Silcrate release is built for and pinned to one `container` CLI release
  for compatibility — currently `1.1.0`

## Install

1. Download the `.dmg` from the [latest release](https://github.com/keenhatch/silcrate/releases/latest)
2. Open it and drag **Silcrate** to Applications

The app is signed and notarized; no account needed. To verify a download, grab the
matching `.sha256` asset and run:

```sh
shasum -a 256 -c Silcrate-<version>.dmg.sha256
```

**Updates** are built in: Silcrate checks the signed Sparkle feed hosted in this
repository ([`appcast.xml`](appcast.xml)) and updates in place.

## Beta

Silcrate is in public beta — expect rough edges, and please report them. The app is free
and the free features stay free; an optional Premium tier for the background-service
features arrives later, and beta testers will get a discount on it. See the
[roadmap](https://silcrate.com/#roadmap) for what's landing next, free and Premium.

## Privacy

Diagnostics are opt-out. Logs are scrubbed of secrets on-device before anything is
written or attached. Crash reports are anonymized. No account system, no server of its
own. Details: [silcrate.com/privacy](https://silcrate.com/privacy)

## Feedback

Found a bug, or want to shape the beta?
[Open an issue](https://github.com/keenhatch/silcrate/issues) or write to
[feedback@silcrate.com](mailto:feedback@silcrate.com) — there's also **Send Feedback**
right inside the app.

---

<div align="center">

© 2026 Niosoft EOOD, trading as [Keenhatch](https://keenhatch.com) · Built by [Dionysios Karatzas](mailto:diokaratzas@gmail.com)

</div>
