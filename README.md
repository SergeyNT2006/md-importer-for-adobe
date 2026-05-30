# Markdown Importer for Adobe InDesign and Illustrator

**MD Importer** · v1.6.0 · *Minimum settings. Maximum speed.*

Import **Markdown** into **Adobe InDesign** and **Adobe Illustrator** with automatic paragraph and character style mapping — from a CEP panel, in a few clicks.

| | |
|---|---|
| **Product website & purchase** | **[sergeynt2006.github.io/md-importer-for-adobe](https://sergeynt2006.github.io/md-importer-for-adobe/)** |
| **Buy full version ($25)** | **[PayPal checkout →](https://sergeynt2006.github.io/md-importer-for-adobe/#buy)** |
| **Free demo (ZXP)** | [GitHub Releases](https://github.com/SergeyNT2006/md-importer-for-adobe/releases) |
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

1. Download the **demo ZXP** from [Releases](https://github.com/SergeyNT2006/md-importer-for-adobe/releases) *(when published)*.
2. Install with your CEP/ZXP installer (e.g. Anastasiy Extension Manager).
3. Restart **InDesign** or **Illustrator**.
4. Open **Window → Extensions → MD Importer**.
5. Select a Markdown file (try [samples/demo.md](samples/demo.md)) → **Import**.

---

## Full version — $25 USD

The full license includes the complete ZXP, updates for the current major version, and email support.

**[→ Purchase on the product website (PayPal)](https://sergeynt2006.github.io/md-importer-for-adobe/#buy)**

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
| [storefront/](storefront/) | Product website (deployed via GitHub Actions) |
| [samples/](samples/) | Demo Markdown files (also bundled in ZXP) |

---

## Author

**Inozemtsev Sergey**
