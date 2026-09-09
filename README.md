# Manvi Jha — Academic Portfolio

This branch contains a ready-to-publish static website. The homepage is
`index.html`; it preserves the academic design and content from the design
previews without requiring their React/CDN runtime.

## Pages

| URL | Source |
| --- | --- |
| `/` | `index.html` |
| `/certificates.html` | `certificates.html` |
| `/project-archive.html` | `project-archive.html` |
| `/lectures-and-press.html` | `lectures-and-press.html` |

The portrait is in `src/Assets/`, and the downloadable CV is `uploads/cv.pdf`.
The shared responsive styles and native talks disclosure styles are in
`site.css`. All content and navigation, including the previous-talks disclosure,
work without JavaScript. Google Fonts is an optional network resource; the site
uses fallback fonts if those fonts are unavailable.

## Netlify

Connect **Severus-Matthew/Portfolio**, production branch **blackhole**, after
merging this fix into that branch. `netlify.toml` specifies:

- Base directory: repository root (`.`)
- Build command: empty
- Publish directory: repository root (`.`)

Clear any separate Package directory override in Netlify if one was configured.
Redeploy the latest commit. The deploy's published files must include
`index.html`, the other three pages, `site.css`, `src/Assets/`, and `uploads/`.
No catch-all SPA redirect is needed because each page is a real HTML file.

## Local check

From this repository, run `python3 -m http.server 8000` and open
`http://localhost:8000/`. Check the main navigation, archive links, CV download,
and the “See previous talks” disclosure.

## Editing

Edit the standard HTML files listed above for changes to the published site.
The original `*.dc.html` files and `support.js` are retained as design references;
they are not the website's entrypoints and do not synchronize automatically with
the standard HTML pages. `github.md` records the older React repository used as
reference material; that repository is not a dependency of this static site.
