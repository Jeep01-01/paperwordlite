# OfflineWord

A lightweight, MS Word–style word processor that runs **100% offline** in any modern browser.
No server, no build step, no dependencies — just open `index.html`.

## Features
- Formatting: font, size, bold/italic/underline/strike, sub/superscript, text & highlight colour
- Paragraph settings: alignment, line spacing, indents, first-line, spacing before/after, lists
- Insert: table, picture, text box, shapes (rectangle, rounded, ellipse, triangle, diamond, line, arrow, star), horizontal line
- Edit: undo, redo, cut, copy, paste
- Zoom (25–300 %, Ctrl +/−, Ctrl + wheel, Fit)
- **Open and save Microsoft Word `.docx` files** (no libraries needed – custom offline reader/writer in `docx.js`), plus `.html`
- **Export to PDF** (📑 PDF button or Ctrl+P → Destination: *Save as PDF*) – A4, selectable text, document name used as file name
- Print (print-optimised CSS) · Save to local drive (Chrome/Edge: native Save dialog) · Autosave to local browser storage
- Installable as an offline app (PWA) when hosted over HTTPS

## Usage
1. Clone the repo, open `app/index.html` in a browser – or see BUILD.md for the Windows installer and Huawei/Android APK.


### Publish with GitHub Pages (optional, enables "Install app")
Repo → **Settings → Pages → Deploy from branch → main / root**.

## Shortcuts
Ctrl+B/I/U, Ctrl+Z/Y, Ctrl+C/X/V, Ctrl+S (save), Ctrl+P (print), Ctrl +/− (zoom)

## DOCX support
Read & written: text, bold/italic/underline/strike, colours, highlight, font & size, sub/superscript, alignment, line spacing, indents, spacing, headings, bullet/numbered lists, tables, pictures, text-box text.
Not supported yet: shapes/text-box layout, headers/footers, comments/tracked changes, legacy `.doc`.
In Firefox/Safari, Save downloads the file to your Downloads folder instead of showing a Save dialog.

## Notes
- Text boxes and shapes: drag the top handle (text box) or the shape body to move; drag the bottom-right corner to resize; `Delete` removes a selected shape.
- Undo/redo covers text edits; moving/inserting floating objects is not yet undoable.
- Browsers may block the Paste button without permission; Ctrl+V always works.

## Roadmap
Headers/footers, page breaks, find & replace, export to DOCX/PDF, object-level undo.

## License
MIT

## Extended features (ribbon row 2)
Find/Replace, Select all, **Text ▾** (case, effects, spacing, drop cap, format painter…), **Paragraph ▾** (list styles, indents, borders, sort, ¶ marks…), **Layout ▾** (margins, orientation, paper size, columns, header/footer, page numbers, watermark, page colour/border, line numbers…), **Insert ▾** (hyperlink, symbols, equation, chart, WordArt, bookmarks, comments, picture tools…), **Table ▾** (rows/columns, merge/split, styles, sum, text↔table…), **References ▾** (TOC, footnotes, captions, index), **Review ▾** (word count, read aloud, protect, versions, share), **View ▾** (read/focus/draft/web, navigation pane), **Mailings ▾** (mail merge).
Not available offline/not implemented: online pictures, screenshots, 3D models, SmartArt, track changes, compare/combine, translate, ink, macros/VBA, envelopes/labels, split window.
