# matan53153.github.io

Personal site of Keith Matanachai, built on [al-folio](https://github.com/alshedivat/al-folio) and served by GitHub Pages.

Pushing to `master` triggers the deploy workflow, which builds the site and publishes it to the `gh-pages` branch.

## Local development

Requires Ruby 3.3.5 (matches CI). Managed by [mise](https://mise.jdx.dev/):

```bash
brew install mise imagemagick libyaml   # libyaml is required, Ruby's psych ext won't build without it
mise install                            # reads .tool-versions
bundle install
bundle exec jekyll serve --livereload   # http://localhost:4000
```

## Updating

- **Blog post:** add `_posts/YYYY-MM-DD-title.md` (copy the existing post as a template)
- **CV:** replace `assets/pdf/cv.pdf` (the navbar CV link points straight at it; path set by `cv_pdf` in `_config.yml`)
- **"Now" items:** add a file in `_news/`
- **Publications:** edit `_bibliography/papers.bib`
- **About page:** edit `_pages/about.md`
