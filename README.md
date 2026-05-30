# Markdown Importer for Adobe InDesign and Illustrator

**MD Importer** · v1.6.0 · *Minimum settings. Maximum speed.*

Import **Markdown** into **Adobe InDesign** and **Adobe Illustrator** with automatic paragraph and character style mapping — from a CEP panel, in a few clicks.

| | |
|---|---|
| **Product website & purchase** | **[sergeynt2006.github.io/md-importer-for-adobe](https://sergeynt2006.github.io/md-importer-for-adobe/)** |
| **Buy full version ($25)** | **[PayPal checkout ($25) →](https://www.paypal.com/cgi-bin/webscr?cmd=_xclick&business=lgphonemar24@gmail.com&item_name=MD+Importer+Full+License&amount=25.00&currency_code=USD&no_shipping=1&return=https%3A%2F%2Fsergeynt2006.github.io%2Fmd-importer-for-adobe%2Fthanks.html&cancel_return=https%3A%2F%2Fsergeynt2006.github.io%2Fmd-importer-for-adobe%2F)** · [Product page #buy](https://sergeynt2006.github.io/md-importer-for-adobe/#buy) |
| **Free demo (standalone .jsx)** | **[Download MD-Importer-Demo.jsx](https://sergeynt2006.github.io/md-importer-for-adobe/demo/MD-Importer-Demo.jsx)** — max 80 lines per file · [GitHub folder](demo/) |
| **Sample Markdown** | [samples/demo.md](samples/demo.md) |

**Contact:** ryzl@hotmail.com · sergeynt2006@yandex.ru

---

## What it does

MD Importer reads a `.md` file, detects structure (headings, lists, tables, emphasis, footnotes, and more), creates or applies **InDesign/Illustrator styles**, and places formatted text in a new frame in the active document.

You stay in Adobe — no copy-paste from a browser, no manual style tagging line by line.

---

## Why MD Importer

| Advantage | Details |
|-----------|---------|
| **Native Adobe workflow** | CEP panel inside InDesign & Illustrator — not a standalone converter |
| **Style mapping built in** | Automatic roles (H1–H6, Body, lists, code, tables…) or manual table editor |
| **Both hosts, one tool** | Same panel for InDesign and Illustrator |
| **InDesign tables** | Markdown tables become **native Table objects** (full frame width) |
| **Footnotes** | Markdown `[^id]` footnotes become real InDesign footnotes |
| **Colored mode** | Optional visual markup with `MD-Color-*` swatches *(InDesign only)* — see below |
| **Prefix & fonts** | Optional `MD-` style prefix; Serif/Sans Serif presets for headings and body |
| **Fast setup** | Choose file → Import. Manual mapping only when you need full control |

Compared to generic Markdown tools or paste-from-HTML workflows, MD Importer is built for **production layout**: styles are first-class, mapping is explicit, and the result is editable in the host app.

---

## Colored mode (Adobe InDesign only)

**Colored** assigns a **distinct swatch color** to each imported style and creates **`MD-Color-*`** entries in the Swatches panel.

**Why use it:** when you mark up a document manually, color-coded styles let you **see instantly** which style is applied to each paragraph or inline run — ideal for proofing structure before final typography.

**Notes:**

- Available in **InDesign only** (disabled in Illustrator).
- Import takes **longer** with Colored enabled (extra swatch and color operations).
- Turn Colored **off** before final layout or export if you need default black text.

---

## Features (v1.6.0)

- **Document target:** import to active document, open existing, or create new
- **Automatic mode** — styles from Markdown roles
- **Manual mode** — mapping table (Role · Style name · Font · Size) + *Create default mapping*
- **Style prefix** — e.g. `MD-H1`, `MD-Body` (custom prefix up to 4 characters)
- **Base fonts** — Serif / Sans Serif presets for headings and body
- **Silent mode** — no alert dialogs on completion
- **Lists** — bullet, numbered, and task lists with indents
- **Inline markup** — bold, italic, code, strikethrough, superscript, subscript, links
- **Images** — linked placeholders when files are found next to the `.md` file

---

## Quick start (demo)

1. Download **[MD-Importer-Demo.jsx](https://sergeynt2006.github.io/md-importer-for-adobe/demo/MD-Importer-Demo.jsx)** (standalone script, no install). If the browser opens the file instead of saving, use **Right‑click → Save link as…** or download from the [product page #demo](https://sergeynt2006.github.io/md-importer-for-adobe/#demo).
2. Open **Adobe InDesign** or **Illustrator** with a document.
3. **File → Scripts → Other Script…** and select `MD-Importer-Demo.jsx`.
4. Choose a Markdown file (try [samples/demo.md](samples/demo.md)) → **Import**.

**Demo limit:** only the **first 80 lines** of each `.md` file are imported. Full version: unlimited import + CEP panel ([purchase](https://sergeynt2006.github.io/md-importer-for-adobe/#buy)).

---

## Full version — $25 USD

The full license includes the complete ZXP, updates for the current major version, and email support.

**[→ PayPal checkout — $25 USD](https://www.paypal.com/cgi-bin/webscr?cmd=_xclick&business=lgphonemar24@gmail.com&item_name=MD+Importer+Full+License&amount=25.00&currency_code=USD&no_shipping=1&return=https%3A%2F%2Fsergeynt2006.github.io%2Fmd-importer-for-adobe%2Fthanks.html&cancel_return=https%3A%2F%2Fsergeynt2006.github.io%2Fmd-importer-for-adobe%2F)**

Or open the [product page buy section](https://sergeynt2006.github.io/md-importer-for-adobe/#buy) and click **Pay with PayPal — $25**.

After payment you receive the full installer and instructions by email (usually within 1–2 business days).  
If needed, send your PayPal receipt to **ryzl@hotmail.com**.

---

## Sample files

| File | Purpose |
|------|---------|
| [samples/demo.md](samples/demo.md) | Headings, lists, tables, footnotes, images |
| [samples/test-lists.md](samples/test-lists.md) | List indents and nesting |

---

## Repository contents

This public repository contains **product information and samples only**. Source code is not published.

| Path | Description |
|------|-------------|
| [docs/](docs/) | Product website — deploy **`/docs`** folder on GitHub Pages (see below) |
| [demo/](demo/) | **Free demo** — compiled standalone `MD-Importer-Demo.jsx` (80-line limit) |
| [samples/](samples/) | Sample Markdown files for testing the demo |

---

## GitHub Pages (product website)

The product page with the PayPal button lives in **`docs/`**. GitHub Pages can publish only **`/` (root)** or **`/docs`** — not other folders.

Configure once:

1. [Repository Settings → Pages](https://github.com/SergeyNT2006/md-importer-for-adobe/settings/pages)
2. **Source:** **Deploy from a branch**
3. **Branch:** `main` → folder **`/docs`** → **Save**
4. Wait 1–2 minutes, then open **https://sergeynt2006.github.io/md-importer-for-adobe/#buy**

Do **not** use **`/` (root)** — without `index.html` at repo root, GitHub shows this README and `#buy` links do nothing.

Alternative: **Source → GitHub Actions** (workflow `.github/workflows/pages.yml` deploys the same `docs/` folder).

---

## Author

**Inozemtsev Sergey**
