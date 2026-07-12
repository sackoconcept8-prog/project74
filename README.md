# Project74 — Civic Archive Static Website

A complete responsive static website for **Project74**, designed as a premium civic archive, digital museum and public education platform.

> **Important content notice:** All timeline events, archive cards, featured stories, image captions and downloadable resources included in this starter are clearly labeled samples. They must not be represented as authentic or verified historical materials. Replace them only with official content approved by the Project74 client.

## Technology

- HTML5
- CSS3
- Vanilla JavaScript
- No backend, database, Node server or paid service required
- Ready for GitHub Pages

## Project structure

```text
project74/
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

## Preview locally

Open `index.html` directly in a browser, or run a simple local server from the project folder:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy to GitHub Pages

1. Create a new GitHub repository, for example `project74`.
2. Upload every file and folder in this project to the repository root.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose the `main` branch and the `/ (root)` folder.
6. Select **Save**.
7. GitHub will publish the site at a URL similar to:
   `https://YOUR-USERNAME.github.io/project74/`

All site paths are relative, so the website works from a GitHub Pages project subdirectory.

## Replace website content

### Brand and navigation

Edit `index.html` to replace:

- Project74 summary and mission copy
- Navigation labels if needed
- Email address
- Social media placeholder links
- Accessibility and privacy language

### Historical narrative

Find the section with `id="history"` in `index.html`. Replace the placeholder narrative only with approved, sourced content. Add source notes and image credits where appropriate.

### Timeline

Each `.timeline-event` button in `index.html` contains these data attributes:

- `data-date`
- `data-title`
- `data-description`
- `data-source`

Replace every sample value with verified information. Keep the button structure unchanged so the JavaScript interaction continues to work.

### Archive items

Each `.archive-card` contains:

- `data-category` for filtering
- `data-search` for search keywords
- image and alt text
- year or date
- category
- title
- short description
- preview button metadata

To add an item, duplicate a complete `.archive-card`, update its content and make sure `data-category` exactly matches one of the filter button values.

This starter uses a static HTML collection. For a larger archive, a future version could load a local JSON file while remaining compatible with GitHub Pages.

### Images

Replace the SVG placeholders in `assets/images/` with approved, optimized images.

Recommended formats:

- AVIF or WebP for photographs
- SVG for logos and simple illustrations
- JPG fallback when needed

Keep image files reasonably small, preserve width and height attributes, use `loading="lazy"` below the fold, and write accurate alt text for meaningful images.

### Educational downloads

Replace `assets/documents/project74-resource-placeholder.txt` with approved accessible PDFs. Then update each download link in `index.html`.

Accessible PDFs should include:

- selectable text
- logical reading order
- headings and document tags
- descriptive link text
- image alternative text
- sufficient color contrast

## Contact form options

### Current mailto fallback

The contact form currently opens the visitor’s email application.

In `script.js`, replace:

```js
const CONTACT_EMAIL = 'hello@project74.example';
```

Also replace the same placeholder email in `index.html` and the JSON-LD metadata.

### Optional Formspree connection

Formspree can be connected later without a custom backend:

1. Create a Formspree form and copy its endpoint.
2. In `index.html`, add the endpoint to the form:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

3. Remove or adapt the mailto submit handler in the contact-form section of `script.js`.
4. Add a reviewed privacy statement explaining the third-party form processor.

Project74 should review Formspree’s current pricing, privacy terms and data handling before enabling it.

## SEO setup

Before launch, update in `index.html`:

- page title
- meta description
- Open Graph image and metadata
- Twitter card metadata
- schema `url`
- organization email

The included schema URL is a placeholder:

```text
https://example.github.io/project74/
```

Replace it with the final public URL.

### robots.txt

Update the sitemap URL in `robots.txt` after deployment.

### sitemap.xml

Update the `<loc>` URL in `sitemap.xml` after deployment. Update `<lastmod>` when major public content changes.

## Accessibility checklist before launch

- Verify all official images have accurate alt text or empty alt attributes when decorative.
- Add captions and source credits to archival media.
- Test every page section using keyboard navigation only.
- Test at 200% browser zoom.
- Run a screen-reader review.
- Confirm PDFs are accessible.
- Confirm contrast after any brand color changes.
- Keep motion optional and test `prefers-reduced-motion`.
- Avoid opening new windows without warning.

## Performance checklist

- Compress production images.
- Avoid embedding full-resolution archival scans directly in card thumbnails.
- Use smaller preview images and link to optimized document viewers or downloads.
- Keep third-party scripts to a minimum.
- Add analytics only after privacy review.

## Custom domain

A custom domain can be connected from **Settings → Pages → Custom domain**. GitHub may create a `CNAME` file automatically. Update all SEO URLs and the sitemap after the domain is active.

## License and rights

No rights are claimed over future Project74 historical materials. Before publishing any document, image, transcript or oral history, confirm ownership, permission, privacy considerations, source attribution and usage rights.
