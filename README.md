# portfolioimrana.yoyosdevices.com.ng — portfolio

The source for Imrana Haruna Abdullah's portfolio and freelance business site.

## What this is

Plain static HTML, CSS and JavaScript. No framework, no build step, no dependencies.
Netlify serves the repo root directly (`publish = "."` in `netlify.toml`).

## Files

| File | What it is |
|---|---|
| `index.html` | The whole site — markup, styles and scripts in one file |
| `netlify.toml` | Publish directory and security/cache headers |
| `robots.txt` | Crawler rules, points at the sitemap |
| `sitemap.xml` | Single-page sitemap |
| `portfolio-1.html` | The previous version, kept for reference. Not served — Netlify serves `index.html` at the root. |
| `logo.svg` | Nav logo |
| `favicon.png` | Favicon and social preview image |
| `profile.jpg` | Hero profile photo |

## Two things to fill in

Both live in the `<script>` block at the top of `index.html` and are empty on purpose.

- **`GA4_ID`** — create a Google Analytics 4 property for this site and paste the
  measurement ID (`G-XXXXXXXXXX`). Empty means no tag loads.
- **`META_PIXEL_ID`** — same idea for the Meta Pixel.

They are deliberately not filled in with an existing property's ID. Pointing this
page at a property belonging to another site merges two sites' data and makes both
sets of numbers wrong.

## The contact form

Uses Netlify Forms. The form is registered by its `name="inquiry"` attribute and the
hidden `form-name` field. Submissions appear under **Forms** in the Netlify dashboard.

If JavaScript is disabled the browser posts natively and Netlify's own success page
is shown. With JavaScript on, the page shows a confirmation only after Netlify has
actually accepted the submission.

## Editing

Anything committed to `main` deploys automatically. Nothing else does — there is no
drag-and-drop step any more.

## Local preview

Open `index.html` in a browser. The form will not submit locally, because there is no
Netlify endpoint to receive it.
