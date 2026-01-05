# patrickfinnerty.com

Personal portfolio site built with [Quarto](https://quarto.org/).

## Local development

- Preview locally: `quarto preview`
- Build once: `quarto render`

Output is written to `_site/` (ignored by git).

## Deployment (GitHub Pages)

This repo is set up to publish `_site/` to the `gh-pages` branch via GitHub Actions.

1. Create a GitHub repo and push this project to the `main` branch.
2. In GitHub: **Settings → Pages**
   - Source: **Deploy from a branch**
   - Branch: `gh-pages` / root
3. Push to `main` and the workflow will publish the site.

## Custom domain (Route 53)

This repo includes a `CNAME` file for `patrickfinnerty.com`. Quarto copies it into the published site automatically.

Typical DNS setup:
- Apex `patrickfinnerty.com`: Route 53 **A/ALIAS** to GitHub Pages for your user/org site
- `www.patrickfinnerty.com`: **CNAME** to your GitHub Pages host

After DNS propagates, enable **Enforce HTTPS** in GitHub Pages.
