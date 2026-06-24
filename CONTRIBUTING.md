# Contributing to iLayerFrame

Thanks for wanting to make this better. Builders are welcome — this project gets stronger
with more hands on it.

## Ground rules

- **Be world-class.** Every choice is the best available one, not the default one. If it
  looks like a template, it's not ready.
- **Dark-first design.** Match the existing aesthetic: island navigation, glass-gel
  controls, editorial typography, cinematic restraint.
- **Single file, where reasonable.** The web app ships as one `index.html`. Keep it
  self-contained unless a feature genuinely needs more (e.g. the native desktop apps).
- **Never break the engine's promise.** Layer decomposition must stay *lossless and
  faithful* — preserve brightness, glass/alpha, glow and tiny detail.

## Workflow

1. Fork and branch from `main`: `git checkout -b feat/<short-name>` or `fix/<short-name>`.
2. Make focused commits with clear messages.
3. Test in the browser before opening a PR — load an image and exercise the path you changed
   (Split, AI Auto-Layer, Description merge, Merge/compose, My Layers, export).
4. Open a pull request that explains **what** changed and **why**.

## Security hygiene (required)

- **Never commit secrets**: keys, tokens, wallet material, private IPs, `.env` files, or
  personal data. The `.gitignore` blocks the common cases; do not bypass it.
- A `gitleaks` GitHub Action runs on every push and PR. PRs that trip it will be blocked.
- If you accidentally commit a secret, treat it as compromised: rotate it and tell a
  maintainer privately (see `SECURITY.md`).

## Good first contributions

- Selection-tool refinements (snapping, edge detection, performance).
- Export presets for specific marketplaces / aspect ratios.
- Internationalisation (the UI mixes EN/PT today).
- Accessibility (keyboard nav, ARIA, contrast).
- Unit tests for the decomposition functions.
- The native desktop shells (macOS / Windows / Linux).

## Code style

- Vanilla JS, no framework for the web app. Match the surrounding code's idioms.
- Keep functions small and readable; comment the *why*, not the *what*.
- Prefer clarity over cleverness.

By contributing, you agree your contributions are licensed under the project's
[MIT License](LICENSE).
