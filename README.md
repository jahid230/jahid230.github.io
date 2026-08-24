# jahid230.github.io

Personal site of **Md Jahidul Haque** — backend & data engineer (JVM, Spark/Scala, AWS, Kubernetes),
co-founder and technical lead of Bakbakum.

Live: <https://jahid230.github.io>

## What this is

A single static page. No build step, no dependencies, no framework — one `index.html`
containing its own CSS and a small amount of vanilla JS (theme toggle, scroll reveal,
nav highlighting). Fonts are loaded from Google Fonts with a system fallback stack.

## Deploying to GitHub Pages

The repository name must be exactly `jahid230.github.io` for the site to be served at
the root domain.

```bash
# from this folder
git init -b main
git add .
git commit -m "Add personal site"
git remote add origin https://github.com/jahid230/jahid230.github.io.git
git push -u origin main
```

Then in the repository: **Settings → Pages → Build and deployment → Source: Deploy from a
branch**, branch `main`, folder `/ (root)`. The site is live at
`https://jahid230.github.io` within a minute or two.

`.nojekyll` is present so GitHub serves the files as-is instead of running them through
Jekyll.

## Editing

Everything lives in `index.html`:

| Section | Anchor |
|---|---|
| About + fact sheet | `#about` |
| Experience timeline | `#work` |
| Bakbakum | `#bakbakum` |
| Stack | `#stack` |
| Research & publications | `#research` |
| Education | `#education` |
| Contact | `#contact` |

Colours are CSS custom properties defined at the top of the `<style>` block — the dark
palette on `:root`, the light palette repeated in the `prefers-color-scheme` media query
and in `[data-theme="light"]`. Change a value in all three places to keep both themes in
step.

## Custom domain (optional)

Add a `CNAME` file containing the bare domain (e.g. `jahidulhaque.de`), point a DNS
`ALIAS`/`ANAME` or four `A` records at GitHub's Pages IPs, and set the domain under
Settings → Pages.
