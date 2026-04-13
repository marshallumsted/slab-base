# [S] slab

A brutalist desktop environment. Pure Rust. Wayland native.

Sharp edges. Flat blocks. Zero rounded corners. One compositor. Your desktop, your workflow.

## What is slab

A native Linux desktop environment built from scratch in Rust. Not a theme on top of KDE. Not a web app in a browser. A real Wayland compositor that renders your desktop, manages your windows, and runs your apps.

### Design principles

- **0px border-radius.** No exceptions.
- **Flat solid colors.** No gradients, no shadows.
- **Bold type.** Instrument Sans + Space Mono. High contrast.
- **Dense and information-heavy.** No wasted whitespace.
- **Sharp, blocky, unapologetic.**

### What makes slab different

- **Tiles are not apps.** Tiles are the relevant pieces of apps, composed into a surface that fits your workflow.
- **Workspaces are not virtual desktops.** They change everything — files, bookmarks, terminals, toolbar tools — not just which windows are visible.
- **Build an app for your task.** Workflows are custom apps assembled from tiles, scoped folders, pinned bookmarks, and terminals.
- **Two bars.** Top: contextual app settings + system icons. Bottom: open apps + quick-spawn tools.

## Architecture

- **Compositor:** Smithay (pure Rust Wayland compositor)
- **Rendering:** wgpu (GPU-accelerated)
- **Input:** libinput (keyboard, mouse, touch)
- **Apps:** Native Rust crates implementing a common `SlabApp` trait
- **Native apps:** Any Wayland client (Firefox, VS Code, Steam, etc.)
- **Config:** `~/.config/slab/`

## Related

- [slab-web](https://github.com/marshallumsted/slab-web) — Remote access module. Access the slab desktop from any browser. Runs standalone on headless servers/VMs, or alongside the native DE for remote access.

## Status

Design phase. See [DESIGN.md](DESIGN.md) for the full architecture.

## License

TBD
