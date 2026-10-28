# rananameer.github.io

Personal site for Rana Nameer Hussain Khan, built on the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme.

## Local development

```bash
bundle install
npm ci
bundle exec jekyll serve
```

The dev server runs at `http://localhost:4000/`.

## Structure

- `_pages/about.md` — home page bio
- `_pages/cv.md` + `_data/cv.yml` — CV page (education, experience, publications, skills)
- `_bibliography/papers.bib` — publications list
- `_projects/` — project pages
- `_data/socials.yml` — contact/social links
- `assets/pdf/` — downloadable CV and transcript

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site with Jekyll and publishes it to the `gh-pages` branch. GitHub Pages (Settings → Pages) should be set to deploy from the `gh-pages` branch.

`Gemfile.lock` is intentionally not committed: CI pins Ruby 3.3.5, but an older local Ruby resolves older, incompatible versions of `jekyll-sass-converter`/`sass-embedded` (missing `color.channel`, breaking the CSS build). Each environment resolves its own lockfile instead.
