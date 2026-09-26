# Asor Notes — marketing site

A static site showcasing the Asor Notes Bible journal app, a Privacy Policy
page, and a waitlist signup page.

## Deploy to Vercel

1. Push this folder to a GitHub repo (or drag-and-drop it into vercel.com/new).
2. In Vercel: **New Project → Import** the repo. No build command or framework
   is needed — this is a plain static site.
3. Deploy. Vercel serves every page automatically.

### Or deploy via the Vercel CLI
```
npm i -g vercel
cd asor-notes-site
vercel
```

## Structure
```
index.html      — the main site
privacy.html    — Privacy Policy page
waitlist.html   — email signup page, linked from the footer + install section
styles.css      — shared styles for all three pages
assets/         — logo + optimized screenshots
vercel.json     — minor routing config
```

## Before this goes live — two things to wire up

1. **Waitlist emails.** `waitlist.html`'s form currently posts to a placeholder
   Formspree URL. To make it collect real emails:
   - Go to formspree.io, make a free account, and create a form.
   - Copy your form's endpoint (looks like `https://formspree.io/f/xxxxxxx`).
   - In `waitlist.html`, replace `YOUR_FORM_ID` in the `<form action="...">`
     line with your real ID. There's a `<!-- TODO -->` comment right above it.
   - Until you do this, the page shows a friendly "not connected yet" message
     instead of silently failing.
   - (Any other form backend works too — just swap the `action` URL.)

2. **Google Play link.** The "Get the app" button in `index.html` points at
   `#` — there's a `<!-- TODO -->` comment right above it marking where to
   drop the real Play Store URL once the app is live.

## Editing
- Colors, type, and layout are controlled by CSS variables at the top of
  `styles.css` (`:root { ... }`) — shared by all three pages.
- Swap screenshots by replacing files in `/assets` and updating the
  matching `<img src="assets/...">` path.
- To update the Privacy Policy text, edit the numbered `<section class="clause">`
  blocks in `privacy.html` directly.
