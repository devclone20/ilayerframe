<div align="center">

# iLayerFrame

**Decompose any artwork into clean, on-chain-ready layers — right in the browser.**

A single-file, zero-backend studio for turning a flat image into a structured, mint-ready
layer stack: colour separation that preserves brightness, glass and glow, a complete
background floor, an embedded iQR, an immutable description block, and a permanent local
library.

[![License: MIT](https://img.shields.io/badge/License-MIT-3ad07e.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-5ba3d0.svg)](CONTRIBUTING.md)
[![No backend](https://img.shields.io/badge/backend-none%20·%20100%25%20client--side-8b93a0.svg)](#privacy--security)
[![Made for builders](https://img.shields.io/badge/builders-welcome-e0b341.svg)](#-contributing)

</div>

---

## What it is

iLayerFrame is part of the **CLONE FRAME · iCLONE** toolkit. It runs entirely in your
browser — **no server, no account, no data leaves your device** — and helps you turn one
image into a coherent set of layers that compose back into a richer, collection-grade NFT.

It is intentionally shipped as **one HTML file** (`index.html`). Open it and it works.

## ✦ Features

- **Split & AI Auto-Layer** — colour decomposition that *preserves the original* brightness,
  glass/transparency and anti-aliased edges. Tiny figures and glints survive (Detail mode),
  instead of being smoothed away.
- **✨ Glow layer** — an adaptive highlight/bloom pass extracts the light into its own soft
  layer so the glow reads on the final composite.
- **Background / Floor** — auto-detects the backdrop colour and lays a full-canvas solid
  rectangle as the base, so the collection always has a complete, clean background.
- **Precise selection tools** — pick, paint, pen (Apple-Pencil lasso), box, points, edge
  select, magic erase, despeckle, with edge snapping and feathering.
- **iQR** — generate a QR linked to your site and merge it into a layer slot.
- **Description iNFT** — cyberpunk text templates with auto-fit (always fits its box,
  centred and faithful) and neon font styles.
- **Merge & compose** — a draggable board to arrange, merge and export the final iNFT.
- **My Layers** — a permanent local library (IndexedDB) to save, reload and export
  collections. Nothing is uploaded; it stays on your device.
- **Apple-style UI** — dark-first, island navigation, glass-gel controls, and a top-bar
  notification island.

## 🚀 Quick start

No build step. No dependencies to install.

```bash
git clone https://github.com/devclone20/ilayerframe.git
cd ilayerframe
# then just open index.html in a browser:
open index.html        # macOS
# xdg-open index.html  # Linux
# start index.html     # Windows
```

Or serve it locally (recommended, so the browser allows everything):

```bash
python3 -m http.server 8123
# open http://localhost:8123/
```

> Once GitHub Pages is enabled for this repo, the app is also usable straight from the web.

## 🗺️ Roadmap

- [x] World-class layering engine (fidelity-preserving Split / AI / Glow / Floor)
- [x] My Layers permanent library
- [x] Definições / Settings hub (appearance, engine, licence & rights)
- [ ] **Native desktop apps — macOS, Windows, Linux** (next focus)
- [ ] Drag-and-drop collection batching
- [ ] Pluggable export presets per marketplace

## 🤝 Contributing

**Builders are welcome — come improve and perfect this.** Whether it's the layering math,
the UI polish, performance, accessibility, new export formats, or the upcoming native apps:
your PRs are wanted.

1. Read **[CONTRIBUTING.md](CONTRIBUTING.md)**.
2. Fork the repo and create a branch: `git checkout -b feat/your-idea`.
3. Keep it a single-file app where reasonable, and match the existing dark-first design.
4. **Never commit secrets** (see [Privacy & security](#privacy--security)).
5. Open a pull request describing the change and the reasoning.

Good first areas: selection-tool refinements, export presets, i18n, native-app shells,
test coverage for the decomposition functions.

## 🔒 Privacy & security

- The app is **100% client-side** — there is no backend and no telemetry. Your images and
  layers never leave your browser (the library lives in local IndexedDB).
- This repository is kept **sterile**: no keys, tokens, wallets, IPs or personal data.
  A `gitleaks` GitHub Action scans every push and pull request.
- Found a vulnerability? Please read **[SECURITY.md](SECURITY.md)** for responsible
  disclosure — don't open a public issue for security reports.

## 🧱 Built with

Pure HTML + CSS + vanilla JS canvas, plus a few open-source libraries loaded from CDN:

| Library | License |
| --- | --- |
| [JSZip](https://github.com/Stuk/jszip) | MIT |
| [PDF.js](https://github.com/mozilla/pdf.js) | Apache-2.0 |
| [qrcode.js](https://github.com/davidshimjs/qrcodejs) | MIT |
| [Tabler Icons](https://tabler.io/icons) | MIT |
| [Google Fonts](https://fonts.google.com) (Orbitron, Rajdhani, Chakra Petch, Audiowide…) | OFL-1.1 |

## 📄 License

Released under the **[MIT License](LICENSE)** — free to use, copy, modify and distribute,
including commercially, as long as the copyright notice is kept. Use the code **and** the
website freely.

<div align="center">

— built for the open. © 2026 CLONE FRAME · iCLONE

</div>
