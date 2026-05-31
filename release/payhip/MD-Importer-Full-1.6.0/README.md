# Markdown Importer for Adobe InDesign and Illustrator

**MD Importer** · version **1.6.0** · *Minimum settings. Maximum speed.*

Thank you for purchasing the full license. This archive contains everything you need to import Markdown into **Adobe InDesign** and **Adobe Illustrator** with paragraph and character style mapping.

**Video overview:** https://youtu.be/qtHSx2Y0sso

---

## What is in this archive

| File | Purpose |
|------|---------|
| **MD-Importer-1.6.0.zxp** | CEP panel installer (primary workflow) |
| **MD-Importer.jsx** | Standalone ExtendScript — run without the panel |
| **manual.md** | Full user guide (panel UI, Colored mode, host differences) |
| **samples/demo.md** | Sample Markdown file for testing |

---

## Requirements

- **Adobe InDesign** or **Adobe Illustrator** (CC recommended)
- UTF-8 Markdown files (`.md`, `.markdown`, or `.txt`)
- **Windows or macOS** (same as your Adobe apps)
- For the ZXP: a ZXP installer such as [Anastasiy Extension Manager](https://install.anastasiy.com/) or Adobe Exchange / UPIA tooling

---

## Quick start — CEP panel (recommended)

1. **Close** InDesign and Illustrator.
2. Install **MD-Importer-1.6.0.zxp** with your ZXP installer.
3. Restart the host app and open a document (or create a new one from the panel).
4. Open **Window → Extensions → MD Importer**.
5. Choose a Markdown file (**Browse…**) and click **Import**.

See **manual.md** for Automatic vs Manual mode, style prefix, Serif/Sans Serif fonts, and **Colored** mode (InDesign only).

---

## Quick start — standalone script

Use this if you prefer **File → Scripts** or need a one-off import without installing the panel:

1. Open InDesign or Illustrator with a document.
2. **File → Scripts → Other Script…**
3. Select **MD-Importer.jsx** from this folder.
4. Follow the dialog → **Import**.

The standalone script uses the same import engine as the CEP panel.

---

## InDesign vs Illustrator

**InDesign** is the primary target: native tables, real footnotes, linked images, and optional **Colored** markup mode.

**Illustrator** uses a stability-focused import path. Tables, footnotes, and images behave differently. See **manual.md → “Adobe Illustrator — limitations”** for the full list (verified for v1.6.0).

---

## Support

- **Email:** ryzl@hotmail.com  
- **Updates:** included for the current major version (1.x)  
- **License:** single-user license; commercial use in your own projects is allowed. Do not redistribute this archive or the ZXP to third parties.

---

**Author:** Inozemtsev Sergey
