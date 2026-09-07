# Energy and AI

Site source for the **UESL** (Urban Energy Systems Lab) Energy and AI page, published via GitHub Pages.

## Structure

```
.
├── _config.yml           # Jekyll site config
├── _layouts/              # Page templates (default, docs)
├── _includes/             # Shared header/footer partials
├── assets/css/            # Stylesheet
├── docs/                  # Documentation pages (Markdown)
├── index.md                # Landing page
└── .github/workflows/pages.yml   # Build & deploy to GitHub Pages
```

## Adding content

- **Landing page**: edit [index.md](index.md).
- **Docs pages**: add a new `.md` file under [docs/](docs/) with front matter:
  ```yaml
  ---
  title: My Page
  nav_order: 2
  ---
  ```
  It's picked up automatically in the docs sidebar (ordered by `nav_order`).

## Local development

Requires Ruby + Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000/energy-and-AI/.

## Deployment

Pushing to `main` triggers [.github/workflows/pages.yml](.github/workflows/pages.yml), which builds the Jekyll
site and publishes it to GitHub Pages. In the repo's **Settings → Pages**, set
**Build and deployment → Source** to **GitHub Actions** (one-time setup).

## Roadmap

Currently a minimal landing page + docs section. Planned: People, Projects, Publications, News —
and potentially migrating to a JS-based framework (e.g. Astro) once the site's needs outgrow
plain Jekyll/Markdown.
