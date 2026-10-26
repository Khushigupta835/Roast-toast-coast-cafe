# Roast Toast Coast Cafe — Project Documentation

A static single-page website for the **Roast Toast Coast Cafe**, built with plain HTML, CSS, and vanilla JavaScript. No build tools, frameworks, or package managers are used.

\---

## Project Files

|File|Description|
|-|-|
|`index.html`|Original cafe landing page|
|`KhushiGupta.html`|Revised version of the landing page with all bugs fixed|
|`README.md`|Project documentation (this file)|
|`Requirments.txt`|Requirements notes file|

\---

## Dependencies

This project has **no installable dependencies**. Everything runs directly in the browser.

### External Resources (loaded at runtime)

|Resource|Type|Source|
|-|-|-|
|Bogart Light|Web font (`woff2` / `woff`)|`fonts.cdnfonts.com`|
|Cafe hero image|JPEG|`images.unsplash.com`|

> \*\*Internet connection required\*\* — both the custom font and the background image are served from third-party CDNs. If either CDN is unreachable, the page falls back to `sans-serif` text and a plain black background panel.

\---

## Browser Requirements

No polyfills or transpilation needed. The following native browser features are used:

|Feature|Minimum browser support|
|-|-|
|CSS Grid (`display: grid`)|Chrome 57+, Firefox 52+, Safari 10.1+, Edge 16+|
|CSS Flexbox (`display: flex`)|Chrome 29+, Firefox 28+, Safari 9+, Edge 12+|
|`@font-face` with `woff2`|Chrome 36+, Firefox 35+, Safari 10+, Edge 14+|
|`document.querySelector`|All modern browsers|
|`classList.toggle()`|Chrome 8+, Firefox 3.6+, Safari 5.1+, Edge 12+|

\---

## Setup \& Usage

No build step required. Open either HTML file directly in any modern browser:

```bash
# Windows — open directly
start index.html
start KhushiGupta.html

# macOS
open index.html

# Linux
xdg-open index.html
```

Or serve locally to avoid any `file://` protocol quirks:

```bash
# Requires Node.js
npx serve .

# Requires Python 3
python -m http.server
```

Then visit `http://localhost:3000` (npx serve) or `http://localhost:8000` (Python).

\---

## Features

* **Two-column layout** — content panel on the left, full-height hero image on the right.
* **Collapsible menu** — clicking "Our Menu" toggles the menu list via a CSS `.is-open` class.
* **Custom web font** — Bogart Light via CDN with `woff2` + `woff` format fallback.
* **Responsive meta viewport** — prevents mobile browsers from scaling the layout incorrectly.

\---

## Known Limitations

* No responsive breakpoints — the two-column layout is not optimised for screens narrower than \~600 px.
* Hero image URL is pinned to a specific Unsplash crop; the image may change if Unsplash rotates the asset.
* Font is served by a third-party CDN with no uptime guarantee.

#Roast-toast-coast-cafe
