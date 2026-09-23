# springwiz11.github.io

Personal academic site for **Kishan Gurumurthy** — ML researcher working on
geometric deep learning, neural ODEs, and federated learning.

Live at <https://springwiz11.github.io>.

Built with [Jekyll](https://jekyllrb.com/) and the
[al-folio](https://github.com/alshedivat/al-folio) theme.

## Layout

```
_bibliography/papers.bib   publications — the single source of truth
_pages/                    about (landing), publications, news, cv, 404
_news/                     short announcements shown on the landing page
_data/socials.yml          email, Scholar id, GitHub, LinkedIn, X
_config.yml                site settings
```

## Adding a publication

Add one BibTeX entry to `_bibliography/papers.bib` and push. Useful fields:

| Field | Effect |
| --- | --- |
| `abbr` | venue badge on the left |
| `selected={true}` | also show it on the landing page |
| `bibtex_show={true}` | adds a copyable BibTeX button |
| `arxiv`, `html`, `pdf`, `code` | link buttons |
| `award` | highlighted note under the entry |
| `abstract` | expandable abstract |

## Deploying

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site
and pushes the result to the `gh-pages` branch. GitHub Pages serves that branch
— **Settings → Pages → Source: Deploy from a branch → `gh-pages` / `root`**.
Do not set the source to "GitHub Actions"; this theme does not use the Pages
artifact flow.

## Local preview (optional)

Needs Ruby 3.x — macOS system Ruby (2.6) is too old.

```bash
brew install ruby
gem install bundler
bundle install
bundle exec jekyll serve
```
