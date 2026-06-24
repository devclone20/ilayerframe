# Security Policy

## Reporting a vulnerability

**Please do not open a public issue for security problems.**

If you find a vulnerability, report it privately:

- Use GitHub's **[Private vulnerability reporting](https://github.com/devclone20/ilayerframe/security/advisories/new)**
  (Security tab → "Report a vulnerability"), or
- Open a minimal GitHub issue asking a maintainer to contact you, **without** any exploit
  details.

We'll acknowledge as soon as we can and work with you on a fix and coordinated disclosure.

## Scope

iLayerFrame is a **100% client-side** application — there is no backend, no database, and no
telemetry. Images, layers and the local library never leave the user's browser
(stored in IndexedDB on the device).

Relevant areas for reports:

- Cross-site scripting (XSS) through filenames, descriptions, imported content, or layer
  names rendered into the DOM.
- Unsafe handling of imported files (images / PDF / SVG).
- Supply-chain risk from the CDN-loaded dependencies.
- Any path that could exfiltrate user data off-device.

## Our hygiene commitments

- **No secrets in the repo.** No keys, tokens, wallet material, private IPs, or personal
  data are ever committed. A `gitleaks` GitHub Action scans every push and pull request.
- **Least exposure.** The app requests no permissions it doesn't need and makes no network
  calls beyond loading its open-source CDN libraries and fonts.
- **Dependencies are pinned** to explicit versions and are all open-source (see the README).

Thank you for helping keep users safe.
