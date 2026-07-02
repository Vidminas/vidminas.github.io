# vidminas.github.io

Personal homepage. Built with the [Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv) template on [HugoBlox/kit](https://github.com/HugoBlox/kit) (Tailwind-based).

The site is built with [Hugo Extended](https://github.com/gohugoio/hugo/releases), pinned in `hugoblox.yaml` (`build.hugo_version`) — `.github/workflows/build.yml` and `.github/workflows/deploy.yml` read this value directly, so it only needs updating in one place. `netlify.toml` still pins its own copy separately for Netlify preview builds; keep it in sync by hand when bumping the version.

Hugo Modules are pinned in `go.mod`:

- `github.com/HugoBlox/kit/modules/blox` — core theme (blocks, layouts, SEO)
- `github.com/HugoBlox/kit/modules/integrations/netlify` — Netlify forms/identity
- `github.com/HugoBlox/kit/modules/slides` — Markdown/reveal.js slide decks

Update modules with `pnpm dlx hugoblox upgrade` (also runs automatically most Mondays via `.github/workflows/upgrade.yml`, opening a PR).

Requires Node.js and [pnpm](https://pnpm.io/). For local development: `pnpm install`, then `pnpm dev` (runs `hugo server`).

To import publications, export a collection from Zotero in BibTeX format (or BibLaTeX, both seem to work) and save it to `publications.bib` in this project directory. Then install the `academic` Python package and run `academic import publications.bib content/publications/ --compact`. Add `--dry-run` to see changes without applying them. Note that citation keys get converted from PascalCase to kebab-case directory names. See <https://github.com/GetRD/academic-file-converter> for more details. Pushing a `publications.bib` change to `main` also triggers `.github/workflows/import-publications.yml`, which does the same import automatically and opens a PR — either workflow works.
