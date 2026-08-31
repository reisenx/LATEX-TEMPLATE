# ReisenX's LaTeX Template

My personal LaTeX `article` class template for personal usage on documentation and university assignments.

> [!NOTE]
>
> This document uses **XeLaTeX** as a typesetting engine and a compiler.

---

# Features

- [x] Two independent templates: `assignment/` for graded reports, `lecture_note/` for lecture summaries
- [x] Running header (course/lecture label, current section, author) and footer page numbers
- [x] Content table page
- [x] Airy, readable typography (spacing, heading rhythm, list spacing tuned for readability)
- [x] Four muted callout boxes: Note, Definition, Example, Key Takeaway
- [x] Clean figures and tables (`booktabs` rules, captions, `cleveref` cross references)
- [x] Fully support English and Thai language in THSarabunPSK font.
- [x] Support image display
- [x] Automatic syntax highlighted dark-theme code snippet using `minted` package
- [x] Lightweight, optional bibliography (`biblatex`)

---

# File Structure

There are two templates, each a fully self-contained folder with no shared switch between them:

- [`assignment/`](assignment/) — for graded assignments and lab reports. Cover shows assignment number, course, student ID, instructor, and due date.
- [`lecture_note/`](lecture_note/) — for lecture summaries and study notes. Cover shows lecture number, week, topic, and last-updated date.

Each folder is split into three files so day-to-day edits stay small:

- `preamble.tex` — packages, fonts, spacing, header/footer, and callout box styling. Rarely edited.
- `metadata.tex` — the fields you edit per document: title, course, and the fields specific to that folder's mode (student ID/due date for assignments; lecture number/week for lecture notes).
- `template.tex` — the actual document content. `\input`s the two files above.
- `references.bib` — sample bibliography entries used by the optional References section.
- `fonts/` — the THSarabun font files, referenced by a relative path, so each folder carries its own copy.

To start a new document, copy whichever folder matches what you're writing (`assignment/` or `lecture_note/`), edit `metadata.tex` for your details, then write your content in `template.tex`.

---

# Guide

## LaTeX Tutorial

Anyone who want to write your own LaTeX document, I highly recommend [this tutorial](https://youtu.be/ydOTMQC7np0?si=QMT5xd30Azp63Qtd) from `freeCodeCamp.org` to learn about setup and basic LaTeX syntax.

After finishing the tutorial, you will need...

- The LaTeX template files from this repository (or write it you own).
- Choose a way to compile LaTeX into a PDF.
  - Overleaf
  - Install LaTeX locally

---

## Overleaf

[**Overleaf**](https://www.overleaf.com/) is an online platform to write your LaTeX document without any installation.

If you’ve never used LaTeX before **Overleaf** is usually the easiest.

---

## Install LaTeX Locally

1. Install [**MiKTeX**](https://miktex.org/download)
2. Install [**TeXMaker**](https://www.xm1math.net/texmaker/) if you want all-in-one editor.
3. Alternatively, you can install [**VSCode**](https://code.visualstudio.com/) and uses **LaTeX Workshop** extension by James Yu.

To be able to use `minted` package to generate code snippet, please install [**Python**](https://www.python.org/downloads/) and install the library in the terminal.

```bash
pip install Pygments
```

The optional bibliography uses `biblatex` with the `biber` backend. Most LaTeX distributions (and Overleaf) already include `biber`; if compiling locally and it is missing, install it through your TeX distribution's package manager (e.g. MiKTeX Console or `tlmgr install biber`).

> [!IMPORTANT]
>
> Make sure to set **XeLaTeX** as a compiler, enable `-shell-escape`, and download all THSarabun fonts before compiling a LaTeX document. If your editor does not run `biber` automatically, run it once after the first `xelatex` pass (Overleaf and most local setups handle this for you).
