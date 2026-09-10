# Asor Notes — marketing site

A single-page static site showcasing the Asor Notes Bible journal app.

## Deploy to Vercel

1. Push this folder to a GitHub repo (or drag-and-drop it into vercel.com/new).
2. In Vercel: **New Project → Import** the repo. No build command or framework
   is needed — this is a plain static site (`index.html` at the root).
3. Deploy. Vercel serves `index.html` and everything in `/assets` automatically.

### Or deploy via the Vercel CLI
```
npm i -g vercel
cd asor-notes-site
vercel
```

## Structure
```
index.html      — the whole site (HTML + CSS + JS in one file)
assets/         — optimized screenshots used on the page
vercel.json     — minor routing config
```

## Editing
- Colors, type, and layout are controlled by CSS variables at the top of
  `index.html` (`:root { ... }`).
- Swap screenshots by replacing files in `/assets` and updating the
  matching `<img src="assets/...">` path.
- The "Request early access" button in the Install section currently
  points at a mailto: link — replace with a real download/install URL
  once one exists.
