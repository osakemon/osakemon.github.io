# osakemon.github.io

Personal academic website of Weiqing Chen — <https://osakemon.github.io>

Built with [Jekyll](https://jekyllrb.com/) on a trimmed-down version of the
[al-folio](https://github.com/alshedivat/al-folio) theme, deployed to GitHub
Pages by [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) on every
push to `master`.

## Running locally

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

`jekyll-imagemagick` generates responsive `.webp` variants at build time, so a
local `imagemagick` install (`brew install imagemagick`) is needed for image
processing to run.

## Layout

| Path | What it holds |
| --- | --- |
| `_pages/` | The pages of the site. `about.md` is the home page (`/`). |
| `_news/` | News entries, one file per item, named `YYYY-MM-DD-slug.md`. Rendered inline on the home page and at `/news/`. |
| `_bibliography/papers.bib` | Publications, rendered by jekyll-scholar. `selected={true}` also lists the entry on the home page. |
| `_projects/` | Project entries shown on `/projects/` (currently empty). |
| `_layouts/`, `_includes/`, `_sass/`, `assets/` | Theme internals. |

The site deliberately carries **no CV page and no CV file**. Do not add one, and
keep CV or resume documents out of the repository entirely: anything Jekyll does
not recognise at the top level is copied verbatim into `_site` and served at a
guessable public URL.

Navigation is driven by front matter: a page appears in the navbar only when it
sets `nav: true`, ordered by `nav_order`. Today that is `about` and
`publications`; `/projects/` is reachable by URL but deliberately hidden.

## Adding content

- **A news item** — add `_news/YYYY-MM-DD-slug.md` with `layout: news`, `date:`
  and `inline: true`. Ordering is by `date`, not by filename.
- **A publication** — add a BibTeX entry to `_bibliography/papers.bib`. If its
  year is new, add that year to the `years:` list in
  [`_pages/publications.md`](_pages/publications.md). Optional fields include
  `abbr`, `selected`, `html`, `pdf` (relative to `assets/pdf/`), `code`,
  `poster` and `slides`.
- **A project** — add a file to `_projects/` with a `title`, `description`,
  `category` (`work` or `fun`) and `importance`, then flip `nav: true` in
  [`_pages/projects.md`](_pages/projects.md).

## License

MIT — see [LICENSE](LICENSE). The theme is © Maruan Al-Shedivat and the al-folio
contributors.
