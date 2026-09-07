# Energy and AI

Site source for the **UESL** (Urban Energy Systems Lab) Energy and AI page, published via GitHub Pages.

## Structure

```
.
├── _config.yml           # Jekyll site config
├── _layouts/              # Page templates (default, docs)
├── _includes/             # Shared header/footer partials
├── assets/css/            # Stylesheet
├── docs/                  # Content pages: papers, projects, tools
├── index.md                # Landing page
└── .github/workflows/pages.yml   # Build & deploy to GitHub Pages
```

## Adding content

Each content page holds a list of entries. Open the file, copy the template block
from the HTML comment at the top, paste it below the last entry, and fill it in.
The template comment stays in the file and does not appear on the website.

- **Research papers**: [docs/papers.md](docs/papers.md) — title, year, authors (first three then
  *et al.*), the AI method, and a short summary of method / usage / relation to AI. Entries go
  under one of the five sub-field sections; the index at the top of the page builds itself.
- **Projects and tools**: [docs/projects-and-tools.md](docs/projects-and-tools.md) — start the
  metadata line with **Project** or **Tool**.
- **Urban energy systems**: [docs/domain.md](docs/domain.md) — domain context and partners.
- **Landing page**: [index.md](index.md) — intro and contacts. The counts on it are computed
  from the pages above, so they update themselves.

Entries are written newest-first. Delete the `_No entries yet._` line once a page has
real content.

To add a whole new section, create another `.md` file under [docs/](docs/) with front
matter — it appears in the sidebar automatically, ordered by `nav_order`:

```yaml
---
title: My Page
nav_order: 4
---
```

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

If the entry lists grow large enough that hand-editing Markdown becomes awkward, the next
step is moving them to structured data files (`_data/papers.yml` etc.) with generated listing
pages — and potentially a JS-based framework (e.g. Astro) after that.
