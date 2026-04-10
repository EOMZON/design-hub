# Design Hub

Static landing for `design.zondev.top`

## Purpose

- act as the root entry for the independent Webdesign, UX, and Icon hubs
- mirror live links for `webdesign.zondev.top`, `ux.zondev.top`, and `icon.zondev.top`
- provide a lightweight, future-proof layer so new design dimensions can spin up without being forced into this repo

## Getting started

1. `cd design-hub && git init`
2. `git add .`
3. `git commit -m "Initial commit"`
4. Create the GitHub repo (for example, `EOMZON/design-hub`), add the remote via `git remote add origin <repo-url>`, and push (`git push -u origin main` or `master`)

## Local preview

- No build step. Open `index.html` in a browser or run a quick server: `python -m http.server 4173`, `npx serve .`, etc.
- Keep `vercel.json` next to the static files so Vercel automatically picks up the configuration when deploying.

## Deploy

This repo is a static folder. Deploy directly to Vercel or any static hosting that can serve the HTML.
