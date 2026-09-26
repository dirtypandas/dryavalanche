# dryavalanche.com

Holding page for Dry Avalanche. Single self-contained HTML file — no build step,
no dependencies, no external network requests at runtime.

## Structure

    index.html    the holding page (fonts + favicon embedded as data URIs)
    CNAME         custom domain for GitHub Pages — must contain only: dryavalanche.com
    .gitignore    keeps secrets and local noise out of the repo

## Deploying

Hosted on GitHub Pages from the `main` branch, root directory.

    git add -A
    git commit -m "describe the change"
    git push

Live within a minute or two.

## Adding pages later

GitHub Pages serves the file tree as-is:

    content/index.html   ->  dryavalanche.com/content/
    blog/index.html      ->  dryavalanche.com/blog/
    404.html             ->  shown for any unknown URL

## DNS (managed at Wix, which is the registrar)

    A     @     185.199.108.153
    A     @     185.199.109.153
    A     @     185.199.110.153
    A     @     185.199.111.153
    CNAME www   dirtypandas.github.io

## Notes

- Never commit API keys. Anything in `.env` stays out via `.gitignore`.
- This repo is public; everything in it, including history, is readable.
