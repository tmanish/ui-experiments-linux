# UI Experiments

> Pixel-perfect, high-fidelity user interfaces — built entirely in the browser, obsessed over to the last detail.

This is a **design-first** repository: a showcase of user interface experiments built to a standard of **perfectionist user experience**. Every pixel, every transition, every interaction is deliberate. The interest here isn't features — it's *fidelity*. How close can a browser get to the real thing, and how good can it feel getting there. And none of it is a mockup — open a shell and the commands actually run.

Each piece is a self-contained, browser-native interface. Nothing to install, nothing to clone — open the live link and use it.

**Built by a Linux fanboy, for Linux fanboys.** Once a Linux fanboy, always a Linux fanboy.

## ▸ View live

- **Home** — https://tmanish.github.io/ui-experiments/
- **Nebula OS** — https://tmanish.github.io/ui-experiments-linux/ui/nebula-os.html
- **Aurora OS** — https://tmanish.github.io/ui-experiments-linux/ui/aurora-os.html
- **Nebula Terminal** — https://tmanish.github.io/ui-experiments-linux/ui/nebula-terminal.html
- **Ubuntu Terminal** — https://tmanish.github.io/ui-experiments-linux/ui/ubuntu-terminal.html

## The experiments

Two original desktops, a real machine emulated in the browser, and a faithful recreation of an existing one — the collection is meant to cover the range.

### Nebula OS

A self-contained **desktop environment** with its own deep-space visual identity — a boot sequence, a starfield, a live-clock top bar, and a dock. A full window manager (draggable, resizable, focusable windows) hosts a suite of apps: a terminal, file manager, text editor, calculator, a sandboxed browser, and a system monitor. The terminal and file manager share one in-memory filesystem, so what you create in one shows up in the other. A complete, original **user interface** that doesn't imitate any existing OS.

### Aurora OS

A desktop environment running an **actual Python interpreter** — CPython 3.12 compiled to WebAssembly via Pyodide. A genuine REPL you can program against, plus a file manager, editor, and system monitor, all inside a real window manager. Not a simulated shell printing canned output; the real interpreter, in a browser tab. (Loads the Pyodide runtime on first launch.)

### Nebula Terminal

The real thing. An actual x86 Linux machine emulated in the browser via **v86** (WebAssembly), rendered through xterm.js over the emulated serial port. It boots a genuine Linux kernel (Buildroot / BusyBox) and drops you at a real shell. There's an actual kernel running behind the prompt.

**Running it:** the BIOS and Linux kernel load from a same-origin `assets/` folder first (most reliable — no third-party host), falling back to a CDN if they aren't there. Place `buildroot-bzimage.bin`, `seabios.bin`, and `vgabios.bin` in `ui/assets/` so the boot never depends on an outside server. It must be served over **http** — GitHub Pages, or locally with `python3 -m http.server 8000` (then `http://localhost:8000/ui/nebula-terminal.html`). Opening it from a `file://` path won't work, because browsers block downloads from local files.

### Ubuntu Terminal

A **pixel-perfect** recreation of the Ubuntu 22.04 LTS GNOME Terminal — the iconic aubergine surface, Yaru-dark chrome, the exact green-and-blue bash prompt. Underneath sits a simulated bash with ~70 commands over an in-memory filesystem: `neofetch` with the Ubuntu logo, `apt install` with streaming download output, animated `htop`, pipes, redirection, Tab completion, and history. A high-fidelity simulation tuned for feel. *(Honest scope: not a kernel — `curl` / `ssh` report no network, and `vim` isn't a full-screen editor.)*

## The standard

- **Pixel-perfect.** Spacing, color, type, and chrome are matched to reference, not approximated.
- **Perfectionist UX.** Interactions are tuned until they feel right — timing, focus, motion, keyboard behavior.
- **Actually runs.** Not screenshots — type a command and it responds. A real Python interpreter and an emulated Linux kernel run live in the page, with faithful simulations elsewhere.
- **Real where it counts.** Where the browser can genuinely do it, it does; where something is a simulation, that's stated plainly.
- **Single file.** Each experiment is one self-contained `.html` — the whole design, in one place.

## License

GPL-3.0.
