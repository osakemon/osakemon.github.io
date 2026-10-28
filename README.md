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
| `_pages/` | The pages of the site. `about.md` is the home page (`/`); `cv.md` is the CV (`/cv/`). |
| `_news/` | News entries, one file per item, named `YYYY-MM-DD-slug.md`. Rendered inline on the home page and at `/news/`. |
| `_bibliography/papers.bib` | Complete publication list, rendered by jekyll-scholar. |
| `_includes/research_highlights.html` | Home-page research summaries, media, and paper/code/model links. |
| `_includes/skills.html` | Home-page toolbox, mirroring the CV's technical expertise section. |
| `_projects/` | Project pages (`layout: project`) shown on `/projects/`: Loki and Thor, with figures and demo videos. |
| `_includes/video.html` | Self-hosted video player used by the project pages and the home page. |
| `assets/video/` | Re-encoded 720p H.264 demo videos (about 5 MB each). |
| `assets/img/projects/` | Project figures and video poster frames. |
| `_video_src/` | Full-resolution video masters. Git-ignored and excluded from the build; never publish these directly. |
| `_layouts/`, `_includes/`, `_sass/`, `assets/` | Theme internals. |

The CV is published on purpose: `/cv/` ([`_pages/cv.md`](_pages/cv.md)) is the
HTML version and `assets/pdf/CV-WeiqingChen.pdf` the download. The PDF is the
source of truth; when it changes, replace the file (keep the name so links stay
valid) and mirror the edits in `_pages/cv.md`, plus `_pages/about.md` and
`_includes/skills.html` if the headline facts or skills moved. Keep CV drafts and
other working documents out of the repository: anything Jekyll does not recognise
at the top level is copied verbatim into `_site` and served at a guessable public
URL. `cv_work/` is ignored for that purpose.

Navigation is driven by front matter: a page appears in the navbar only when it
sets `nav: true`, ordered by `nav_order`. Today that is `about`, `projects`,
`publications` and `cv`.

## Adding content

- **A news item** — add `_news/YYYY-MM-DD-slug.md` with `layout: news`, `date:`
  and `inline: true`. Ordering is by `date`, not by filename.
- **A publication** — add a BibTeX entry to `_bibliography/papers.bib`. If its
  year is new, add that year to the `years:` list in
  [`_pages/publications.md`](_pages/publications.md). Optional fields include
  `abbr`, `selected`, `html`, `pdf` (relative to `assets/pdf/`), `code`,
  `poster` and `slides`.
- **A research highlight** — edit `_includes/research_highlights.html`. Verify
  project summaries and results against the linked paper or current research records.
  The home page uses these summaries in place of full citations;
  setting `selected_papers: true` in `about.md` also renders `selected={true}` entries.
- **A project** — add a file to `_projects/` with `layout: project`, a `title`,
  `description`, `img` (card thumbnail), `importance`, and optionally `venue`,
  `role` and `links` (a list of `{label, url}`). The body is Markdown and may
  use the `figure.html` and `video.html` includes.
- **A demo video** — put the master file in `_video_src/`, re-encode it to 720p
  H.264 (the step below keeps a three-minute screen recording around 5 MB), save
  the result in `assets/video/`, and grab a poster frame into
  `assets/img/projects/`. Then embed it with
  `{% include video.html path="name.mp4" poster="projects/name_poster.jpg" label="..." caption="..." %}`.

  ```bash
  ffmpeg -i _video_src/master.mov -vf "scale=1280:-2" -c:v libx264 -preset slow -crf 28 \
    -pix_fmt yuv420p -c:a aac -ac 1 -b:a 64k -movflags +faststart assets/video/name.mp4
  ffmpeg -ss 30 -i _video_src/master.mov -frames:v 1 -vf scale=1280:-2 assets/img/projects/name_poster.jpg
  ```
  Use `-an` instead of the audio flags when the recording is silent.

## License

MIT — see [LICENSE](LICENSE). The theme is © Maruan Al-Shedivat and the al-folio
contributors.
