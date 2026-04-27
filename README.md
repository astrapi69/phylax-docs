# phylax-docs

User documentation for [Phylax](https://github.com/astrapi69/phylax) - the local-first, zero-knowledge living health profile PWA.

Live site: https://astrapi69.github.io/phylax-docs/

## Why a separate repo

The Phylax PWA at `astrapi69.github.io/phylax/` owns the `/phylax/` path on GitHub Pages, including its service worker scope. Hosting documentation under a sibling subpath would conflict with the SW scope, so the docs live in their own GitHub Pages site at `astrapi69.github.io/phylax-docs/`.

See `docs/MAINTENANCE.md` in the [main Phylax repo](https://github.com/astrapi69/phylax) for the full rationale and cross-repo coordination notes.

## Status

**Iteration 1 (in progress):** scaffolding only. Tooling, navigation, and placeholder pages are live. Real content is filled in over subsequent iterations as Phylax features stabilize.

## Stack

- [MkDocs](https://www.mkdocs.org/) static site generator
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme
- [mkdocs-static-i18n](https://github.com/ultrabug/mkdocs-static-i18n) for DE/EN parallel content (`docs_structure: folder`)
- [mkdocs-git-revision-date-localized](https://github.com/timvink/mkdocs-git-revision-date-localized-plugin) for last-modified dates
- Poetry for Python dependency management
- GitHub Actions deploy to GitHub Pages

No analytics, no trackers, no third-party CDNs at runtime - same constraints as the Phylax app itself.

## Layout

```
phylax-docs/
├── mkdocs.yml                  # MkDocs config (nav block is generated)
├── docs/
│   ├── pyproject.toml          # Poetry config for the docs build
│   └── help/                   # docs_dir
│       ├── _meta.yaml          # single source of truth for navigation
│       ├── de/                 # German content
│       └── en/                 # English content
├── scripts/
│   └── generate_mkdocs_nav.py  # generates nav block from _meta.yaml
└── .github/workflows/docs.yml  # CI build + deploy
```

## Local build

Requires Python 3.11+ and Poetry.

```bash
cd docs
poetry install --no-interaction
cd ..
poetry --directory=docs run python scripts/generate_mkdocs_nav.py
poetry --directory=docs run mkdocs serve -f mkdocs.yml
```

Open http://127.0.0.1:8000 to preview.

## Contributing content

1. Edit the DE and EN page in parallel (DE in `docs/help/de/...`, EN in `docs/help/en/...`).
2. To add a new page, register it in `docs/help/_meta.yaml` and create both DE and EN files.
3. Run `python scripts/generate_mkdocs_nav.py` so the regenerated nav block reflects the change.
4. The deploy workflow runs the same nav-generation step in CI; the committed `mkdocs.yml` is the canonical version.

The German content follows the umlaut and language conventions documented in the Phylax main repo (`CLAUDE.md`).

## License

MIT - see [LICENSE](LICENSE).
