# ReisenX's LaTeX Template

My personal LaTeX `article` class template for personal usage on documentation and university assignments.

> [!NOTE]
>
> This document uses **XeLaTeX** as a typesetting engine and a compiler.

---

# Features

- [x] Cover page
- [x] Content table page
- [x] Fully support English and Thai language in THSarabunPSK font.
- [x] Support image display
- [x] Automatic syntax highlighted dark-theme code snippet using `minted` package

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

> [!IMPORTANT]
>
> Make sure to set **XeLaTeX** as a compiler and download all THSarabun fonts before compile a LaTeX document.
