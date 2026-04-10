# Design Hub

Static gateway for `design.zondev.top`.

## Purpose

- route users to the correct design dimension instead of becoming a second content-heavy atlas
- explain the boundary between `webdesign`, `ux`, `icon`, and shared `design-skills`
- provide one stable entry point for future design dimensions without merging them back into one mixed repo

## Content boundary

`design-hub` should stay shallow.

It can contain:

- task-based routing
- ecosystem overview
- boundary explanation
- live / planned status
- links to shared repositories

It should not become:

- a web-style gallery
- a selector for website visual families
- a history / movement encyclopedia
- a duplicate prompt / skill download surface

Those belong in the specialized sites, especially `webdesign-site`.

## Local preview

- No build step. Open `index.html` directly or run a quick server such as `python -m http.server 4173` or `npx serve .`
- Keep `vercel.json` next to the static files so Vercel can deploy the folder as-is

## Deploy

This repo is a static folder. Deploy directly to Vercel or any static host that serves HTML.
