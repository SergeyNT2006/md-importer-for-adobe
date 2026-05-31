# MD-Importer Demo

Sample document for testing import into **InDesign** or **Illustrator**.

## Features

- Bullet list item one
- Bullet list item two

1. Numbered entry
2. Second entry

> Blockquote: typography and layout start with text.

Inline `code` and **bold** with *italic* and a [link](https://example.com).

---

### Tables (InDesign: native Table objects; Illustrator: tab-separated)

**3 columns** — with header row (separator line below).

| Name | Role | Size |
|------|------|------|
| Alpha | H1 | 24 |
| Beta | Body | 11 |
| Gamma | Code | 10 |

**2 columns** — no header row (one data row only, no separator).

| Key | Value |
| Author | MD-Importer |

**5 columns** — with header row.

| A | B | C | D | E |
|---|---|---|---|---|
| 1 | 2 | 3 | 4 | 5 |
| red | green | blue | black | white |
| short | medium text | x | y | z |

**4 columns** — separate table after the 5-column block.

| Quarter | Revenue | Cost | Margin |
|---------|---------|------|--------|
| Q1 | 120 | 80 | 40 |
| Q2 | 150 | 95 | 55 |

```text
Fenced code block
line two
```

![Sample alt](placeholder.png)

## Footnote (InDesign)

Text with a footnote reference[^demo] in the paragraph.

[^demo]: This becomes a real InDesign footnote when imported into InDesign.

## New v1 Features

This section validates newly enabled markdown elements in the importer.

### Strikethrough

Use ~~deprecated text~~ and keep active text unchanged.

Mixed inline sequence: **bold**, *italic*, `code`, ~~strike~~, and [normal link](https://github.com).

### Task Lists (GFM)

- [ ] Prepare import mapping for article
- [x] Import first chapter into document
- [ ] Verify styles and spacing after import
- [X] Export review PDF for approval

### Setext Headings

Setext Heading Level 1
======================

Setext Heading Level 2
----------------------

Paragraph after setext headings for spacing validation.

### Superscript and Subscript (controlled inline)

Chemistry example: H<sub>2</sub>O and CO<sub>2</sub>.  
Math example: x<sup>2</sup> + y<sup>2</sup> = z<sup>2</sup>.  
Publication note: 1st edition can be written as 1<sup>st</sup>.

### Autolink Literals

Raw URL with protocol: https://example.org/docs/importer  
Raw URL with www prefix: www.adobe.com  
Second URL in sentence: See details at https://github.com/commonmark/commonmark-spec for baseline behavior.

### Fallback-oriented checks

- Unsupported inline HTML should remain readable: <span class="note">inline span text</span>.
- Mixed task-like plain text (should stay plain if invalid): - [maybe] unresolved token.
- Nested task visual check (may flatten by design in v1):
  - [ ] Parent-looking item
    - [x] Child-looking item (expected same level in flat import path)

## Closing

Final paragraph after image placeholder.
