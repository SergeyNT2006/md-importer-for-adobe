# Markdown Importer for Adobe InDesign and Illustrator

**MD Importer** · v1.6.0 · *Minimum settings. Maximum speed.*

Import **Markdown** into **Adobe InDesign** and **Adobe Illustrator** with automatic paragraph and character style mapping — from a CEP panel, in a few clicks.

| | |
|---|---|
| **Product website & purchase** | **[sergeynt2006.github.io/md-importer-for-adobe](https://sergeynt2006.github.io/md-importer-for-adobe/)** |
| **Video demo** | **[Watch on YouTube](https://youtu.be/qtHSx2Y0sso)** |
| **Buy full version ($15)** | **[Payhip — $15](https://payhip.com/b/mwhab)** · [Product page #buy](https://sergeynt2006.github.io/md-importer-for-adobe/#buy) |
| **Free demo (standalone .jsx)** | **[Download ZIP](https://sergeynt2006.github.io/md-importer-for-adobe/demo/MD-Importer-Demo.zip)** (unzip → run script) — max 80 lines · [GitHub folder](demo/) |
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

Watch the **[product overview on YouTube](https://youtu.be/qtHSx2Y0sso)** or follow the steps below.

1. Download **[MD-Importer-Demo.zip](https://sergeynt2006.github.io/md-importer-for-adobe/demo/MD-Importer-Demo.zip)** and extract `MD-Importer-Demo.jsx`. Or use the [product page #demo](https://sergeynt2006.github.io/md-importer-for-adobe/#demo).
2. Open **Adobe InDesign** or **Illustrator** with a document.
3. **File → Scripts → Other Script…** and select `MD-Importer-Demo.jsx`.
4. Choose a Markdown file (try [samples/demo.md](samples/demo.md)) → **Import**.

**Demo limit:** only the **first 80 lines** of each `.md` file are imported. Full version: unlimited import + CEP panel ([purchase](https://sergeynt2006.github.io/md-importer-for-adobe/#buy)).

---

## Full version — $15 USD

The full license includes the complete ZXP, updates for the current major version, and email support.

**[→ Buy on Payhip — $15 USD](https://payhip.com/b/mwhab)**

Or open the [product page buy section](https://sergeynt2006.github.io/md-importer-for-adobe/#buy).

Instant digital download after checkout.  
If needed, contact **ryzl@hotmail.com**.

---


## Author

**Inozemtsev Sergey**
