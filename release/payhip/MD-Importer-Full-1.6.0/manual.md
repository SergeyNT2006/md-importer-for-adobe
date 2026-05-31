# MD Importer — User Manual

**Product:** Markdown Importer for Adobe InDesign and Illustrator  
**Short name:** MD Importer  
**Version:** 1.6.0  
**Tagline:** Minimum settings. Maximum speed.

**Video overview:** https://youtu.be/qtHSx2Y0sso

This manual covers the **CEP panel** (installed from the ZXP) and the **standalone** script (`MD-Importer.jsx`) included in your download.

---

## 1. Purpose

MD Importer reads Markdown (`.md`, `.markdown`, `.txt`) and places structured, styled text into the active **InDesign** or **Illustrator** document:

- Headings, body text, lists, emphasis, code, tables, links, and more
- Paragraph and character styles created or mapped automatically or manually
- One new text frame per import (area text in Illustrator)

The panel is a convenient front end; the import engine lives in `MD-Importer.jsx` (also bundled inside the extension).

---

## 2. Installation

### 2.1 CEP panel (ZXP)

1. Quit InDesign and Illustrator.
2. Install **MD-Importer-1.6.0.zxp** using a ZXP installer.
3. Restart the host application.
4. Open **Window → Extensions → MD Importer**.

If the panel does not appear, confirm the ZXP installed without errors and restart the app once more.

### 2.2 Standalone script

No installation required. Run **MD-Importer.jsx** via **File → Scripts → Other Script…** (or place it in the host Scripts folder if you prefer).

---

## 3. Panel overview

### 3.1 Host status

Shows whether the panel runs in InDesign or Illustrator and whether a document is open.

### 3.2 Markdown file

- Path field for the `.md` file.
- **Browse…** opens the file picker.

### 3.3 Document target

Choose where to import:

- **Active document** — current open document
- **Open document…** — pick from open documents (InDesign)
- **Create new** — new document before import

### 3.4 Mode

| Mode | Behavior |
|------|----------|
| **Automatic** | Creates/applies styles from Markdown roles found in the file (e.g. H1–H6, Body, lists). |
| **Manual** | Uses the mapping table (☰ menu → **Manual mapping…**). Roles, style names, fonts, and sizes can be edited. |

Use **Create default mapping** in the mapping dialog after selecting a Markdown file to fill the table from file content.

### 3.5 Silent mode

When enabled, completion alerts are suppressed. Errors may still appear in the status area.

### 3.6 Colored (Adobe InDesign only)

**Colored** is a **proofing and markup aid**, not a final-design mode.

**What it does**

- Assigns a **distinct color** to each imported paragraph/character style.
- Creates **`MD-Color-*`** swatches in the Swatches panel so you can see which semantic role is applied at a glance.

**Why use it**

When you build or check document structure manually, color-coded styles make it **immediately obvious** whether a paragraph is H2, Body, a list, code, etc.—before you apply final typography (font, size, black text).

**Important notes**

- **InDesign only.** The checkbox is disabled in Illustrator; the panel shows a hint that Colored is unavailable in the current host.
- Import is **slower** with Colored enabled (extra swatch and color operations).
- Turn **Colored off** before final layout, print, or PDF export if you need default black text throughout.
- Colored does not replace proper style names—it adds visual feedback on top of normal `MD-*` (or prefixed) styles.

### 3.7 Menu (☰)

- **Style prefix** — prefix for generated style names (default `MD`, up to 4 characters)
- **Heading / Body font** — Serif or Sans Serif presets
- **Manual mapping…**
- **Ping host** — test connection to ExtendScript
- **Clear settings** — reset panel preferences
- **Help / About**

### 3.8 Import

**Browse…** selects the file; **Import** runs the pipeline. Settings are saved in the panel automatically.

---

## 4. Recommended workflow

1. Open or create a document in InDesign or Illustrator.
2. Select the Markdown file.
3. Choose **Automatic** for a first pass, or **Manual** if you map to existing document styles.
4. In **InDesign**, optionally enable **Colored** while checking structure; disable it for final styling.
5. Click **Import**.
6. Review the new text frame, paragraph/character styles, and (if Colored was on) **MD-Color-*** swatches.

---

## 5. Supported Markdown (core)

- ATX headings `#` … `######`
- Setext headings (title + `===` / `---`)
- Paragraphs
- **Bold**, *italic*, `inline code`, ~~strikethrough~~
- Bullet, numbered, and task lists (`- [ ]`, `- [x]`)
- Blockquotes (`>`)
- Fenced code blocks (<code>```</code>)
- Horizontal rules (`---`, `***`, `___`)
- GFM tables (`| col | col |`)
- Links `[text](url)` and autolink literals (`https://…`)
- `<sup>` / `<sub>` (controlled inline HTML)
- Images `![alt](path)` — host-dependent (see below)
- Footnotes `[^id]` + `[^id]: text` — **InDesign only** (real footnotes)

Complex nested Markdown may simplify to plain text. See section 7 for host-specific behavior.

---

## 6. Adobe InDesign — capabilities

InDesign is the **primary** target for production imports:

| Feature | Behavior |
|---------|----------|
| **Tables** | Native **Table** objects; tables span the text frame width when applicable |
| **Footnotes** | Markdown footnotes become real InDesign footnotes |
| **Images** | Linked frames when the image path resolves (relative to the `.md` folder) |
| **Lists** | Indents and tab stops derived from list style size |
| **Colored mode** | Available (see section 3.6) |
| **Styles** | Paragraph and character styles created/applied and linked to text |

---

## 7. Adobe Illustrator — limitations

Illustrator import is **supported and tested for v1.6.0**, with a **stability-first** pipeline optimized for reliable text placement—not full parity with InDesign.

Use Illustrator for **quick content placement and typography prep**. Use **InDesign** for editorial layout, tables as objects, footnotes, and linked images.

### 7.1 What works well in Illustrator

- Automatic and Manual import via the CEP panel
- Headings, body, lists (including task lists), blockquotes, code blocks
- Inline emphasis (bold, italic, code, strikethrough, sup/sub)
- Links (text + URL in parentheses)
- Manual mapping table and Serif/Sans Serif font presets
- Style prefix; paragraph and character styles are **created** in the document
- Single **area text** frame per import
- **Colored** is correctly **unavailable** (UI disabled; not applicable to AI workflow)

### 7.2 Known limitations (Illustrator)

| Feature | InDesign | Illustrator |
|---------|----------|-------------|
| **GFM tables** | Native Table objects | **Tab-separated lines** with tab stops—not Table objects |
| **Footnotes** | Real footnotes | **Not supported** — reference/definition text stays in body flow as plain text |
| **Images** | Linked placed objects when found | **Text placeholder line** only (e.g. missing or unresolved paths); no equivalent linked frame workflow |
| **Colored mode** | Yes | **Not available** (by design) |
| **Complex nesting** | Better fidelity | May flatten lists or mixed blocks |

### 7.3 Illustrator stability notes

- The import path avoids fragile style-binding operations that have caused crashes in some Illustrator versions when assigning `paragraphStyle` on every run.
- Styles appear in the Paragraph/Character Styles panels; text is formatted for reliable rendering.
- For repeated imports, prefer **Manual** mode if you map to existing document styles.

If you need tables as objects, footnotes, linked images, or Colored proofing, **use InDesign**.

---

## 8. General limitations (both hosts)

- One new text frame per import (Illustrator: one area text frame).
- Not a full CommonMark/GFM implementation (no math, no raw HTML blocks, limited nested lists).
- Links are text + URL; interactive PDF link objects are not created.
- Image paths are resolved relative to the Markdown file folder.

---

## 9. Troubleshooting

| Problem | What to try |
|---------|-------------|
| Import does nothing | Click **Ping host**; confirm a document is open. |
| Panel missing after install | Reinstall ZXP; restart host; check ZXP installer log. |
| Empty or partial content | Check UTF-8 encoding; simplify nested Markdown. |
| Manual mode ignores roles | Run **Create default mapping** with a valid `.md` path. |
| Colored still on in swatches | Turn off Colored before import, or remove unused **MD-Color-*** swatches manually. |
| Illustrator table columns misaligned | Adjust tab stops on table row styles, or re-create table in InDesign. |

Status messages appear at the bottom of the panel. For standalone script issues, note the alert text and contact support with host app version and sample `.md` (if possible).

---

## 10. Support

**Email:** ryzl@hotmail.com  

Include: host app (InDesign / Illustrator), version, OS, MD Importer **1.6.0**, and steps to reproduce.

---

*Markdown Importer for Adobe InDesign and Illustrator · MD Importer v1.6.0 · © Inozemtsev Sergey*
