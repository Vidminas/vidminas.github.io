# vidminas.github.io

Personal homepage. Built with the [Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv) template on [HugoBlox/kit](https://github.com/HugoBlox/kit) (Tailwind-based).

The site is built with [Hugo Extended](https://github.com/gohugoio/hugo/releases), pinned in `hugoblox.yaml` (`build.hugo_version`) — `.github/workflows/build.yml` and `.github/workflows/deploy.yml` read this value directly, so it only needs updating in one place. `netlify.toml` still pins its own copy separately for Netlify preview builds; keep it in sync by hand when bumping the version.

Hugo Modules are pinned in `go.mod`:

- `github.com/HugoBlox/kit/modules/blox` — core theme (blocks, layouts, SEO)
- `github.com/HugoBlox/kit/modules/integrations/netlify` — Netlify forms/identity
- `github.com/HugoBlox/kit/modules/slides` — Markdown/reveal.js slide decks

Update modules with `pnpm dlx hugoblox upgrade` (also runs automatically most Mondays via `.github/workflows/upgrade.yml`, opening a PR).

Requires Node.js and [pnpm](https://pnpm.io/). For local development: `pnpm install`, then `pnpm dev` (runs `hugo server`).


## Importing publications

To import publications, export a collection from Zotero in BibTeX format (or BibLaTeX, both seem to work) and save it to `publications.bib` in this project directory.

Pushing `publications.bib` to `main` triggers `.github/workflows/import-publications.yml`, which runs the import and opens a PR.

Alternatively, to run the import locally, install and run the `academic` Python package:
```bash
uv tool install academic
academic import publications.bib content/publications/ --compact --verbose
```

Add `--dry-run` to see changes without applying them. Note that citation keys get converted from PascalCase to kebab-case directory names.

After importing, each new `index.md` needs a few site-specific edits that `academic` doesn't make — copy the shape from an existing entry such as `content/publications/vizgirda-2025-teacher-online/index.md`:

- Replace your own name in `authors:` with `admin` (the owner slug in `data/authors/admin.yaml`).
- Convert the flat `publication: '*Venue*'` string to the structured `publication: {name, short_name}` shape, and move a top-level `doi:` under `hugoblox.ids.doi`. `academic` still writes the legacy shapes, and the theme logs a deprecation warning for each.
- Rewrite `links: [{name: URL, ...}]` as `links: [{type: source, url: ..., label: ACM DL}]`.
- Add `projects:` associations pointing at slugs in `content/projects/`.
- Delete any `url_pdf` holding a local `~/Zotero/storage/…` path. To attach a PDF, drop the file into the bundle named `<slug>.pdf` — the theme auto-detects it (along with `cite.bib`) and renders the buttons; no front matter needed.

See <https://github.com/GetRD/academic-file-converter> for more details.
