# manvijha.com — static site

Plain HTML. No build step, no dependencies.

```
index.html         main page
certificates.html  courses, workshops, certificates
projects.html      full project archive
lectures.html      video lectures, writing, press
assets/            portrait, CV pdf
figures/           paper figures
```

## Deploy on Netlify

New site from Git → pick this repo → leave **build command** empty → **publish directory** `/` (or the folder these files sit in). Netlify serves `index.html` at the root.

Drag-and-drop also works: drop this folder onto the Netlify dashboard.

## Editing

Every page is self-contained, inline-styled HTML. To change text, edit the HTML directly.

- Fonts load from Google Fonts (Newsreader, IBM Plex Sans, IBM Plex Mono).
- The "See 4 earlier talks" button uses a small inline script at the bottom of `index.html`.
- To replace the CV, overwrite `assets/ManviJha_CV.pdf` keeping the same name.
- To add a paper figure, drop the image in `figures/` and point the row's `<img src>` at it.

## Custom domain

Netlify → Domain management → add your domain, then point the DNS records Netlify shows you.
