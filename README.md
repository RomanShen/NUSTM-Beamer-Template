# NUSTM Beamer Template

This repository provides a NUSTM-styled Beamer slide template for paper reading reports and academic presentations.

## Features

- Custom NUSTM theme (`NUSTM.sty`) with:
  - color palette and themed title/frame blocks
  - custom header/footer (author, date, title, slide numbers)
  - rounded block styles and code block support
- Ready-to-use demo slides in `NUSTM.tex`
- English and Chinese configuration options
- Citation support with `natbib`
- Bundled assets (figures, logos, fonts, bibliography)

## Repository Structure

- `/NUSTM.tex`: main Beamer source file (example presentation)
- `/NUSTM.sty`: custom theme/style definitions
- `/my_bib.bib`: bibliography database
- `/acl_natbib.bst`: bibliography style file
- `/figures`: images used by slides
- `/source`: theme assets used in the header/title area
- `/fonts`: optional font files
- `/NUSTM.pdf`: compiled example output

## Requirements

Install a LaTeX distribution with Beamer and BibTeX support (for example, TeX Live or MiKTeX), including commonly used packages such as:

- `beamer`, `tikz`, `booktabs`, `tcolorbox`, `natbib`
- math packages (`amsmath`, `amssymb`, etc.)

## Quick Start

1. Edit content in `NUSTM.tex`:
   - title/author/institute/date
   - sections and frames
   - figures and tables
2. Compile the slides:

```bash
pdflatex NUSTM.tex
bibtex NUSTM
pdflatex NUSTM.tex
pdflatex NUSTM.tex
```

This generates `NUSTM.pdf`.

## Chinese / English Support

The template supports both English and Chinese workflows.

- For English slides, keep the default settings.
- For Chinese slides, uncomment the Chinese-related lines in `NUSTM.sty` (around the `EN/CN settings` section), including:
  - localized names (`\figurename`, `\tablename`, `\refname`)
  - `ctex` / `xeCJK` font settings as needed

If you enable Chinese font packages, use a compatible engine (typically XeLaTeX).

## Bibliography and Citation

- Citations are managed with `natbib`.
- The sample document uses:
  - `\bibliographystyle{ieeetr}`
  - `\bibliography{my_bib.bib}`
- For footnote-style references in slides, combine `\cite{...}` with `\blfootnote{...}` (see examples in `NUSTM.tex`).

## Customization Tips

- **Theme colors/layout**: edit color and Beamer template definitions in `NUSTM.sty`.
- **Header logo/title image**: replace files in `/source` and update references in `NUSTM.sty` if needed.
- **Slide aspect ratio**: change `aspectratio` in `\documentclass[...]` in `NUSTM.tex`.
- **Title page metadata**: update `\title`, `\author`, `\institute`, and `\date`.

## Notes

- Keep image paths relative to `NUSTM.tex` (for example, `figures/...`).
- If bibliography entries do not appear, ensure you run BibTeX between LaTeX compilation passes.
