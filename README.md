# UI Experiments

> Pixel-perfect, high-fidelity user interfaces — built entirely in the browser, obsessed over to the last detail.

This is a **design-first** repository: a showcase of user interface experiments built to a standard of **perfectionist user experience**. Every pixel, every transition, every interaction is deliberate. The interest here isn't features — it's *fidelity*. How close can a browser get to the real thing, and how good can it feel getting there.

Each piece is a self-contained, browser-native interface. Nothing to install, nothing to clone — open the live link and use it.

## ▸ View live

- **Aurora OS** — https://tmanish.github.io/ui-experiments/aurora-os.html
- **Ubuntu Terminal** — https://tmanish.github.io/ui-experiments/ubuntu-terminal.html

## The experiments

### Aurora OS

A complete desktop **user interface** rendered in a single browser tab — and beneath the surface, a real one. It runs an actual CPython 3.12 interpreter (compiled to WebAssembly), not a mock shell printing canned output. A high-fidelity window manager wraps it: draggable, resizable, focusable, minimizable windows, a virtual filesystem, and a hand-built SVG icon set drawn to match.

The design goal: a desktop that doesn't just *look* like a real environment, but behaves like one.

### Ubuntu Terminal

A **pixel-perfect** recreation of the Ubuntu 22.04 LTS GNOME Terminal — Yaru-dark window chrome on the iconic aubergine surface, Ubuntu Mono set at the right weight, the green-and-blue bash prompt exact to the original. Underneath sits a simulated bash with ~70 commands and an in-memory filesystem.

The **UX** is the point: `neofetch` renders the Ubuntu ASCII logo with live system info, `apt install` streams realistic download output, `htop` animates, `man` pages read true. Pipes, redirection (`>`, `>>`), Tab completion, command history, and `Ctrl+C` / `Ctrl+L` all behave the way muscle memory expects.

*Honest scope:* this is a **high-fidelity** *simulation* of bash, not a Linux kernel — there's no network layer (`curl` / `ssh` report no connection) and `vim` isn't a full-screen editor. The fidelity is in the feel. Start with `neofetch`, then `sudo apt install cowsay` → `cowsay hi`.

## The standard

- **Pixel-perfect.** Spacing, color, type, and chrome are matched to reference, not approximated.
- **Perfectionist UX.** Interactions are tuned until they feel right — timing, focus, motion, keyboard behavior.
- **High fidelity over breadth.** One interface done convincingly beats ten done halfway.
- **Real where it counts.** Where the browser can genuinely do it, it does; where something is a simulation, that's stated plainly.
- **Single file.** Each experiment is one self-contained `.html` — the whole design, in one place.

## License

GPL-3.0.
