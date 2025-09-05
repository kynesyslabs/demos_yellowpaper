## Demos Yellow Paper

License: CC BY-NC-ND 4.0

The Demos Yellow Paper is a formal technical specification of the Demos Network (Omniweb data and interoperability layer), covering architecture, consensus (PoR-BFT), GCR, CVSA, native bridges, Liquidity Tanks, Web2 on-chain access, XM execution, ZK module, FHE, and more. The current LaTeX source is `ypv6.tex`.


## Repository Status

This document reflects the Demos Network specifications as of 5 September 2025 and will evolve as research and implementation progress. Please check tags/releases and commit history for historical snapshots.

## Usage

If you just want to read the paper, simply open https://github.com/kynesyslabs/demos_yellowpaper/ypv6.pdf or build the PDF with the steps below and open `build/ypv6.pdf` . You can also open the produced PDF in your preferred viewer (Preview, Adobe Acrobat, Evince).

If you want to edit the paper, work directly on the LaTeX source (`ypv6.tex`) with an editor/IDE and recompile.

## Build

### Prerequisites
- A modern TeX distribution (TeX Live 2021+ or MacTeX on macOS)
- `latexmk` (recommended) or `pdflatex`/`xelatex`

On macOS (Homebrew):
```bash
brew install --cask mactex-no-gui
# Optionally ensure latexmk is available:
tlmgr install latexmk
```

On Debian/Ubuntu:
```bash
sudo apt update
sudo apt install -y texlive-full latexmk
```

### Quick start (latexmk)
```bash
# from the repository root
mkdir -p build
latexmk -pdf -interaction=nonstopmode -output-directory=build ypv6.tex
# Output: build/ypv6.pdf
```

### Alternative (pdflatex)
```bash
mkdir -p build
pdflatex -interaction=nonstopmode -output-directory=build ypv6.tex
bibtex build/ypv6 || true
pdflatex -interaction=nonstopmode -output-directory=build ypv6.tex
pdflatex -interaction=nonstopmode -output-directory=build ypv6.tex
```

## Editing

- Recommended: Visual Studio Code with the LaTeX Workshop extension for live preview, linting, and bibliography support.
- Main source: `ypv6.tex`
- Images: place figures under `Pictures/` (e.g., `Pictures/image1.jpg`, `Pictures/image2.png`, etc.), matching their references in the `.tex`.
- Keep hyperlinks consistent: prefer `\href{...}{...}` or `\url{...}` for external URLs.
- Try to avoid empty formatting commands (e.g., `\textbf{}`) unless intentional for layout control.

## Repository Layout

- `ypv6.tex`: Main LaTeX source of the Yellow Paper
- `Pictures/`: Figures and diagrams referenced by the paper
- `LICENSE`: CC BY-NC-ND 4.0
- `README.md`: This file
- Optional (if present): `Biblio.bib`, `build.sh`, `Makefile`

## Contributing

We welcome typo fixes, broken link fixes, and minor clarifications via issues and pull requests. Substantive changes or new sections should be proposed and discussed via an issue before a PR.

Note: The license is CC BY-NC-ND 4.0, which restricts derivative works. By contributing, you confirm you have rights to your contributions and license them consistently.

## Versions

Historical versions should be tracked via tags or a `BRANCHES.md` index. When publishing a stable snapshot, create a tag and update this section with a brief changelog.

## About

The Demos Yellow Paper is a formal specification maintained by the authors and contributors. It aims to provide a rigorous, implementation-agnostic reference for the Demos Network.

## License

CC BY-NC-ND 4.0. See `LICENSE`.
