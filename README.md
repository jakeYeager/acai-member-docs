# ACAI Member Docs

Useful documentation for ACAI Studio members.

Built with [Quarto](https://quarto.org) and hosted on GitHub Pages.

## Local Development

A Docker Compose file is included so you don't need Quarto installed locally.

```bash
docker compose up
```

Then open [http://localhost:4848](http://localhost:4848) in your browser. The preview hot-reloads on file changes.

## GitHub Pages

The site is served from the `docs/` folder on the `main` branch. To publish changes, render the site and commit the output:

```bash
quarto render
git add docs/
git commit -m "Render site"
git push
```

GitHub Pages is configured in **Settings > Pages** to use the `main` branch, `/docs` folder as the source root.
