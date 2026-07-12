# Project74 — Civic Archive Website

A complete responsive static website for **Project74**, designed as a premium civic archive, digital museum and public education platform.

> **Historical-content notice:** Every timeline event, archive card, document preview, image caption and download included here is clearly labeled sample content. Nothing in this starter should be presented as an authentic historical record. Replace samples only with official, verified and client-approved materials.

## Live deployment

After GitHub Pages is enabled, the public address will be:

`https://sackoconcept8-prog.github.io/project74/`

## Technology

- HTML5
- CSS3
- Vanilla JavaScript
- No backend, database, Node server or paid service
- Relative paths compatible with a GitHub Pages project subdirectory
- Responsive desktop, tablet and mobile layouts
- Reduced-motion support and keyboard-visible focus states

## Project structure

```text
project74/
├── .nojekyll
├── index.html
├── styles.css
├── script.js
├── README.md
├── robots.txt
├── sitemap.xml
└── assets/
    ├── documents/
    │   └── project74-resource-placeholder.txt
    ├── icons/
    │   └── favicon.svg
    └── images/
        ├── archive-sample.svg
        ├── featured-story-placeholder.svg
        ├── historical-image-placeholder.svg
        └── og-cover.svg
```

## Enable GitHub Pages

1. Open this repository on GitHub.
2. Select **Settings**.
3. Open **Pages** in the left menu.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/ (root)**.
6. Select **Save**.
7. Wait for GitHub to display the published address.

The repository already contains `index.html`, `.nojekyll`, the final sitemap URL and relative asset paths.

## Preview locally

Open `index.html` directly, or run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Replace official content

### Main text and contact details

Edit `index.html` to replace:

- mission and historical narrative
- approved quotation and source
- Project74 email address
- social media placeholder links
- accessibility and privacy wording

The placeholder email also appears in the JSON-LD metadata and in `script.js` as `CONTACT_EMAIL`.

### Timeline

Timeline samples are stored in the `timelineData` array near the top of `script.js`. Each item contains:

- `date`
- `title`
- `text`
- `source`

Replace every item with verified dates, descriptions and citations. Keep sample labels visible until the official review is complete.

### Archive explorer

Archive cards are stored in the `archiveData` array in `script.js`. Each entry contains:

- year or date label
- category
- title
- description

The available filters are stored in the `categories` array. Category wording must match exactly for filtering to work.

The current archive uses eight sample items. Search, filtering, result counts, the empty state and document-preview dialog are implemented in vanilla JavaScript.

### Images

Replace files in `assets/images/` with approved optimized media. Recommended formats:

- AVIF or WebP for photographs
- SVG for logos and simple illustrations
- JPG when a fallback is required

Keep accurate alt text, image credits and verified captions. Use `loading="lazy"` for images below the first screen.

### Educational resources

Replace `assets/documents/project74-resource-placeholder.txt` with accessible, approved PDF documents and update the links in `index.html`.

Accessible PDFs should have selectable text, logical reading order, document headings, descriptive links, alternative text and sufficient contrast.

## Contact form

The current form uses a mailto fallback and stores no submissions.

Replace this line in `script.js`:

```js
CONTACT_EMAIL='hello@project74.example'
```

Also replace the same placeholder email in `index.html`.

Formspree can be connected later by adding its endpoint to the form and adapting or removing the mailto submit handler. Review the service’s current privacy terms and data handling before launch.

## SEO

The following are already included:

- professional page title and description
- Open Graph metadata
- Twitter card metadata
- favicon
- WebSite JSON-LD
- `robots.txt`
- `sitemap.xml`

Before a custom-domain launch, update the canonical public URLs in `index.html`, `robots.txt` and `sitemap.xml`.

## Accessibility review before launch

- Test the full site using only a keyboard.
- Test at 200% browser zoom.
- Review official media alt text and captions.
- Confirm all downloadable PDFs are accessible.
- Run a screen-reader review.
- Recheck contrast after brand changes.
- Preserve `prefers-reduced-motion` support.

## Rights and verification

No rights are claimed over future Project74 historical materials. Before publishing any document, photograph, transcript, oral history or family record, confirm authenticity, ownership, permission, privacy considerations, source attribution and usage rights.
