# HP Connectivity Kit (Open Source)

A reliable, cross-platform, open-source alternative to the official HP Prime Connectivity Kit, written in Rust.

> **Project Status: Early Planning / Pre-v0.1**  
> This repository is currently a clean slate where the actual architecture and v1 codebase are being built from scratch.  
> Looking for the initial proof-of-concept? You can read the [early vibecoded prototype](https://github.com/RodrigoAroeira/hp-connectivity-kit-prototype).

## Why this project exists

The official HP Prime Connectivity Kit is closed-source, suffers from frequent UI crashes and random USB disconnects, lacks modern editor workflows, and has zero native Linux support (with USB functionality breaking under Wine). Because official updates are infrequent, the HP Prime community needs a fast, dependable, and maintainable alternative that works natively across Linux, Windows, and macOS.

## Goals

### Core Architecture & Code Quality

* **Built from scratch in Rust:** Clean, idiomatic, human made code with proper error handling, state management, and device lifecycle control.
* **Decoupled Core & UI:** Separate the low-level USB HID protocol library from the user interface so both a CLI tool and a desktop GUI can share the exact same backend.
* **True Cross-Platform Support:** First-class native builds for Linux, Windows, and macOS.

### Roadmap & Target Features (v1.0)

* [ ] **USB HID Communication Layer:** Reliable detection, connection handling, and clean disconnect recovery for HP Prime (G1 and G2).
* [ ] **File Inspection & Editing:** Read, create, and edit contents directly—including programs (`.hpprgm`), notes, app files (`.hpappdir`), and variables on the calculator.
* [ ] **Two-Way File Transfers:** Fast, reliable uploading and downloading of files between PC and calculator.
* [ ] **Full Device Backups & Restore:** One-click backup and restore of calculator state.
* [ ] **Modern Editor Integration:** Plain-text encoding/decoding for `.hpprgm` files so users can write HP PPL in external editors and sync via CLI or GUI, alongside built-in editing in the GUI.
* [ ] **Desktop GUI:** A lightweight, responsive interface replicating and improving upon the essential workflows of the official Connectivity Kit.

### Stretch Goals (Post-v1.0)

* [ ] Screen capture / live screen mirroring.
* [ ] Firmware update support.

## Contributing

Contributions are welcome! Whether you have experience with **Rust**, **USB HID protocols (`hidapi` / `rusb`)**, **GUI frameworks in Rust**, or **reverse-engineering**, feel free to jump in:

1. Check the **Issues** or **Discussions** tab to see current architectural planning and open tasks.
2. Reference the [prototype](https://github.com/RodrigoAroeira/hp-connectivity-kit-prototype) if you want to inspect the working USB packet logic already discovered.
3. Open an issue before submitting large PRs so we can align on architecture and module boundaries.
