# Design Hub

Static router for `design.zondev.top`.

## Purpose

`design-hub` is no longer a second content site.

It should do one job well:

- route people to the right design dimension
- keep the choice inside one stable entry point
- let specialized sites carry the deep content

The current UI therefore uses a sidebar + embedded viewer shell instead of long explanatory sections.

## UI Rule

The homepage should answer one question first:

> 我现在该去哪？

That means:

- default to task-first routing, not taxonomy explanation
- keep the user inside the hub when switching between design dimensions
- keep meta explanation minimal in the UI
- move boundary and discipline notes into this README instead of the front page

## Current Routes

### Webdesign

- use for: website visual direction, style families, real references, prompt / skill pickup
- not for: full UX diagnosis, icon systems, shared asset governance
- live target: `https://webdesign.zondev.top`

### UX

- use for: information architecture, clarity, user path, service gaps, usability issues
- not for: style atlas browsing, icon recognition details
- live target: `https://ux.zondev.top`

### Icon

- use for: app icon, favicon, recognition, black/white legibility, small-size consistency
- not for: full-page layout, reading rhythm, large content systems
- live target: `https://icon.zondev.top`

### Design Skills

- use for: reusable skills, prompts, shared constraints, cross-site AI assets
- not for: acting as a primary browse surface for end users
- live target: `https://github.com/EOMZON/design-skills`

## Content Boundary

`design-hub` can contain:

- routing UI
- lightweight route descriptions
- live links
- embedded subsite viewing
- link-outs to GitHub or shared repos

`design-hub` should not become:

- a second style atlas
- a design history encyclopedia
- a duplicate prompt download center
- a long manifesto about why the system is split

## Technical Notes

- static site only; no build step
- main implementation lives in `index.html`
- Vercel serves the folder as-is
- iframe embedding is currently viable for:
  - `webdesign.zondev.top`
  - `ux.zondev.top`
  - `icon.zondev.top`
- boundary docs stay here so the UI can stay focused on routing

## Local Preview

- open `index.html` directly, or
- run `python3 -m http.server 4173` inside this repo

## Deploy

Deploy directly with Vercel from this folder.
