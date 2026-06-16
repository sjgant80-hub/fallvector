# FallVector

Sovereign single-file vector editor. The Illustrator wedge of **FallStudio** (phase 1).

One HTML file. No server. No build. No telemetry. Works from `file://`. Your work lives in IndexedDB on your machine.

**Prime: 439 · Seal: MIT · ◊·κ=1**

---

## For the user

FallVector is a pure-SVG drawing surface. What you see on screen is the file — no proprietary format, no lock-in, no cloud.

**Tools** (keyboard shortcuts):
- `v` Select — pick a shape, drag to move, drag corner handles to resize
- `p` Pen — click to add path points, double-click to close
- `r` Rect — drag to draw
- `e` Ellipse — drag to draw
- `l` Line — drag to draw
- `t` Text — click to place, type to set

**Panels** (right side):
- Layers — full z-order, click to select, eye to hide, × to delete
- Properties — x, y, width, height, fill, stroke, stroke width, opacity, z-order buttons
- Palette — 12 estate colours, click to paint the selected shape

**Workflow**:
- Export `.svg` (the real file) or `.png` (rasterised)
- Paste SVG markup with `Ctrl+V` to import as a group
- `Ctrl+Z` / `Ctrl+Y` for 20-step undo
- Every edit auto-saves; reopens where you left off
- `Ctrl+K` opens **Ω autopilot** — type `rectangle 200x100 brass` or `circle red` and it draws

Bring your own key (Anthropic / Gemini / OpenAI / OpenRouter) in Settings if you want the autopilot to parse freeform intent. Offline T0 mode handles the common phrasings without any key.

## For the developer

Single `index.html`. Vanilla JS. Inline CSS. No npm, no bundler, no framework.

Architecture follows the FallStudio shared doctrine:
- **L1 FACE** — SVG canvas with checker bg, tool sidebar, layers + properties + palette
- **L2 SWARM** — Ω palette routes intents to named ops (add, edit, delete, export, paint)
- **L3 CASCADE** — T0 keyword router works offline; T3 BYOK adds Claude / GPT / Gemini / OpenRouter for freeform intent
- **L5 PERSIST** — IndexedDB primary; SVG/PNG export covers everything
- **L6 SKIN** — estate dark palette, brass mark, mobile-responsive at <760px
- **Konomi** sovereign shim baked inert
- **fallmesh** BroadcastChannel on `fall-signal` channel, prime 439
- **postMessage** API: `{target:'fallvector', action:'ping'|'add'|'export'}`
- **PWA** manifest via data: URL

Fork the file. Modify the script. That's it. No build step.

### Siblings (FallStudio phase 1)

FallVector is one wedge of seven planned sovereign creative tools:
- FallVector — vector graphics (this file) — replaces Illustrator
- FallRaster — pixel painting — replaces Photoshop
- FallStage — page layout — replaces InDesign
- FallReel — video timeline — replaces Premiere
- FallMotion — motion graphics — replaces After Effects
- FallSheet — PDF — replaces Acrobat
- FallType — font workshop — replaces Fontlab

Each ships as one HTML file under the same doctrine.

### License

MIT. Copyright (c) 2026 Simon Gant · sjgant80-hub.
