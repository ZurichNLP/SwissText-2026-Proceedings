# SwissText 2026 proceedings

This repository contains the proceedings for the 11th Swiss Text Analytics Conference (SwissText 2026).
Proceedings are compiled using `aclpub2` ([https://github.com/rycolab/aclpub2](https://github.com/rycolab/aclpub2)).

## Repository structure

- `aclpub2-main/` is the upstream `aclpub2` source with templates and tooling.
- `aclpub2-main/examples/swisstext2026/` contains the YAML inputs (metadata, program, sponsors, etc.).
- `aclpub2-main/output/` contains the compiled PDF outputs (including `proceedings.pdf`).

## Setup

1. Clone this repository.
2. Ensure you have Python, Java, and LaTeX (with `pdflatex`) installed. See `aclpub2` docs for details.
3. (Optional) Create a virtual environment and install Python dependencies:

```bash
cd aclpub2-main
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Generate proceedings

From the `aclpub2-main/` directory, run:

```bash
python ./bin/generate examples/swisstext2026 --proceedings --overwrite
```

The output PDF will be placed in `aclpub2-main/output/proceedings.pdf`. The `--overwrite` flag allows re-running without manually deleting previous outputs.

## Contact

- Yingqiang Gao, yingqiang.gao@uzh.ch
- Jannis Vamvas, jannis.vamvas@uzh.ch

## Notes

- If you edit YAML inputs under `aclpub2-main/examples/swisstext2026/`, re-run the generate command.
- Watermarked PDFs are emitted under `aclpub2-main/output/watermarked_pdfs/`.
