# koinig.site landing page

Static landing page for **koinig.site**, used as a central entry point for browser-based annotation tools, HSI/NIR labelling software, training utilities, games, and related project links.

## Files

- `index.html` — complete landing page
- `.nojekyll` — prevents Jekyll processing
- `README.md` — repository documentation

No build step is required. The landing page is self-contained and does not depend on external CSS or JavaScript frameworks.

## Deployment

1. Put `index.html`, `.nojekyll`, and this `README.md` in the repository root.
2. Enable GitHub Pages for the repository.
3. Configure `koinig.site` as the custom domain under **Settings → Pages**.
4. Configure the DNS records required by GitHub Pages.
5. Verify that `https://koinig.site` opens the landing page over HTTPS.

The individual tools are hosted independently, so they can be updated or redeployed without changing the landing-page repository unless their URLs change.

## Live projects

The current project cards in `index.html` point to:

- **Gamehub**  
  `https://geri1993.itch.io/gamehub2`

- **Annotation Tool**  
  Detection + segmentation annotation with local files and LiteRT inference.  
  `https://AVAWLeoben.github.io/CV-Waste-Web/`

- **Annotation Trainer**  
  Browser-based training workflow for annotated YOLO datasets.  
  `https://avawleoben.github.io/ANNOTATION_TRAINER/`

- **HSI / NIR Labelling Tool**  
  Browser-based hyperspectral pixel labelling and spectral export workflow.  
  `https://avawleoben.github.io/HSI-Labeller/`

All four project cards are currently marked **Live**.

## Navigation links

The top navigation also contains:

- **Tools** — jumps to the project-card section
- **Gamehub** — `https://geri1993.itch.io/gamehub2`
- **ResearchGate** — `https://www.researchgate.net/profile/Gerald-Koinig`
- **GitHub** — `https://github.com/AVAWLeoben`

## Editing project links

Search for:

```html
EDIT LINKS HERE
```

inside `index.html` to find the project-card section quickly.

Each live project uses an anchor block similar to:

```html
<a class="card" href="https://example.com/" target="_blank" rel="noopener">
  ...
</a>
```

To change a project, update:

- `href`
- project title
- description
- status badge
- launch text
- destination label

For a project that is not yet available, use a disabled card based on:

```html
<div class="card disabled">
  ...
</div>
```

## Adding another tool

Duplicate an existing live project card and change its icon, title, description, URL, badge, launch text, and destination label.

The card grid is responsive and automatically collapses to a single column on smaller screens.

## GitHub username / organization changes

`koinig.site` is the public custom domain and can remain unchanged if the GitHub account or organization name changes.

If repository ownership or the GitHub Pages namespace changes, update any hard-coded `github.io` project URLs in `index.html` and this README.

If DNS uses a CNAME pointing to a `*.github.io` hostname, update that target as well. If the custom domain remains assigned to the landing-page repository and DNS is still valid, visitors can continue using:

`https://koinig.site`

## Current structure

The landing page intentionally remains separate from the individual applications:

```text
koinig.site
├── Annotation Tool      → CV-Waste-Web
├── Annotation Trainer   → ANNOTATION_TRAINER
├── HSI / NIR Labeller  → HSI-Labeller
└── Gamehub              → itch.io
```

This keeps deployment and maintenance of each project independent.
