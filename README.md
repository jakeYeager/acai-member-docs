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

## Linking to Downloadable Files

Place downloadable files (e.g. Word templates) in a `files/` folder and link to them normally:

```md
[Download](files/template.docx)
```

Quarto copies the `files/` folder into `docs/` on render. Browsers will automatically prompt a download for `.docx` files. For file types a browser might open inline (e.g. PDFs), force a download with the `download` attribute:

```md
[Download](files/template.pdf){download="template.pdf"}
```

For public Google Docs, use the export URL to trigger a download directly rather than opening the Google Docs viewer:

```md
[Download](https://docs.google.com/document/d/DOCUMENT_ID/export?format=docx)
```

Replace `DOCUMENT_ID` with the ID from the doc's share URL and `format=docx` with `format=pdf` if you'd prefer PDF. The doc must be shared as "Anyone with the link can view."
