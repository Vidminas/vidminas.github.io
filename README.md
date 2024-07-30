# vidminas.github.io

Personal homepage. Created with [Hugo Academic CV Theme](https://github.com/HugoBlox/theme-academic-cv).

For local development, run `hugo serve` in the project directory.

To import publications, export collection from Zotero in BibTeX format (or BibLaTeX, both seem to work) and save it to `publications.bib` in this project directory. Then install the `academic` Python package and run `academic import --bibtex publications.bib --publication-dir content/publication --compact`. Add `--dry-run` to see changes without applying them. Note that citation keys get converted from PascalCase to kebab-case directory names. See <https://github.com/GetRD/academic-file-converter> for more details.