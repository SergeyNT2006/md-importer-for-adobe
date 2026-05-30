# MD-Importer — test list indents (variant A)

Use this file to check **hanging indents** on bullet and numbered lists in **InDesign** and **Illustrator**.

Expected per list item: **left indent 10 pt**, **tab stop 10 pt** (after `•` or `1.`), **hanging −10 pt**; body lines align at the tab; **no** nested levels (leading spaces in MD are ignored).

---

## Bullet list

- First bullet item with enough text to wrap onto a second line so the hanging indent is visible.
- Second bullet item.
- Third bullet item with **bold** and *italic* inline.

## Body between lists

This paragraph uses the body style. It should have **no** list left indent — only normal body margins.

## Numbered list

1. First numbered item with longer text that may wrap to the next line in the frame.
2. Second numbered item.
3. Third numbered item.

## Another bullet block

- Alpha
- Beta
- Gamma

## Not nested (variant A)

These lines look nested in Markdown but import as **flat** list items (same indent):

- Top level item
  - Looks nested (two leading spaces) — same indent as others
    - Looks deeper — still same indent

## Closing

Final body paragraph after lists.
