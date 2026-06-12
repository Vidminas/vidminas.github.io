# vidminas.github.io

Personal homepage. Created with [Hugo Academic CV Theme](https://github.com/HugoBlox/theme-academic-cv).

The site is built with [Hugo Extended 0.148.2](https://github.com/gohugoio/hugo/releases/tag/v0.148.2) (pinned in `.github/workflows/publish.yaml` and `netlify.toml` — keep all in sync when upgrading).

It uses the final releases of the legacy Bootstrap-based Hugo Blox module line, pinned in `go.mod`:

- `blox-bootstrap/v5` @ `v5.9.8-0.20250819232439-62f5b139d3c5` (last commit before the module was retired, includes Hugo 0.146–0.148 compatibility fixes)
- `blox-core` v0.4.1, `blox-seo` v0.3.1, `blox-plugin-reveal` v1.2.4, `blox-plugin-netlify` v1.2.0 (final tags)

⚠️ Do **not** run `hugo mod get -u`: this module line is end-of-life and there are no newer compatible versions. Upstream development moved to the Tailwind-based [HugoBlox/kit](https://github.com/HugoBlox/kit), so updating further means migrating the whole site to the new [Academic CV template](https://github.com/HugoBlox/hugo-theme-academic-cv) (new config format, Node/pnpm toolchain, and rewriting the custom partials in `layouts/_partials/`).

Note: `layouts/_partials/blocks/about-biography.html` is a project copy of the module's `about.biography` block — dotted template names collide in Hugo 0.146+ and render the wrong layout, so avoid enabling dotted blocks (e.g. `about.avatar`) directly.

For local development, run `hugo server` in the project directory.

To import publications, export collection from Zotero in BibTeX format (or BibLaTeX, both seem to work) and save it to `publications.bib` in this project directory. Then install the `academic` Python package and run `academic import --bibtex publications.bib --publication-dir content/publication --compact`. Add `--dry-run` to see changes without applying them. Note that citation keys get converted from PascalCase to kebab-case directory names. See <https://github.com/GetRD/academic-file-converter> for more details.