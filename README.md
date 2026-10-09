# koinig.site landing page

Static landing page for the `koinig.site` GitHub Pages repository.

## Files

- `index.html` — complete landing page
- `.nojekyll` — prevents Jekyll processing

No build step and no external CSS/JS dependencies are required.

## Deployment

1. Create the new GitHub repository.
2. Put `index.html` and `.nojekyll` in the repository root.
3. Enable GitHub Pages for the repository.
4. Configure `koinig.site` as the custom domain in GitHub Pages.
5. Configure the DNS records required by GitHub Pages.

## Project links

The project cards are directly in `index.html`.

Current configured live links:

- Gamehub: `https://geri1993.itch.io/gamehub2`
- Annotation Tool: `https://AVAWLeoben.github.io/CV-Waste-Web/`

Annotation Trainer and HSI Labelling Tool are displayed as unavailable until their URLs are ready.

Search for `EDIT LINKS HERE` in `index.html` to find the project-card section quickly.

## Adding another tool

Duplicate one of the `<a class="card">...</a>` blocks and change:

- `href`
- title
- description
- status badge
- destination label

For a project that is not yet published, duplicate a `<div class="card disabled">...</div>` block instead.
