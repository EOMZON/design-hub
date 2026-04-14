# Design Index

Static index site for `design.zondev.top`.

## Purpose

This repo is the entry layer for a growing design network.

It should do one job well:

- show the current design dimensions at a glance
- keep room for future dimensions before those sites exist
- route people into the right specialized surface without turning the homepage into another encyclopedia

The live homepage therefore acts as an index, not a fixed four-link hub.

## IA Rule

The homepage should answer these questions in order:

1. what is this system
2. how is it organized
3. which dimension should I enter next

That means:

- title and tagline must frame the site as a growing index
- live dimensions and future dimensions should be separated
- dimension cards should use stable naming that can survive expansion
- implementation details should stay in this README, not dominate the front page

## Current Naming

- site name: `Design Index`
- tagline: `Design resources, by dimension.`

### Live dimensions

- `Web Visual`
  - live target: `https://webdesign.zondev.top`
- `Interaction`
  - live target: `https://ux.zondev.top`
- `Icon & Assets`
  - live target: `https://icon.zondev.top`
- `Methods`
  - live target: `https://github.com/EOMZON/design-skills`

### Planned dimensions

- `Motion`
- `Brand Systems`
- `Type Systems`
- `Image Direction`

## Content Boundary

`design-hub` can contain:

- index framing
- live preview cards
- fullscreen focus viewing
- planned-dimension placeholders
- link-outs to GitHub or specialized sites

`design-hub` should not become:

- a duplicate style atlas
- a second UX knowledge base
- a full prompt download center
- a manifesto explaining the whole system every time a user lands

## Technical Notes

- static site only; no build step
- main implementation lives in `index.html`
- Vercel serves the folder as-is
- iframe embedding is currently viable for:
  - `webdesign.zondev.top`
  - `ux.zondev.top`
  - `icon.zondev.top`
- GitHub does not allow iframe embedding for `design-skills`, so `Methods` uses a local README preview plus an external link
- the homepage is data-driven through a dimension array so future expansion can happen by adding new entries rather than redesigning the shell

## Local Preview

- open `index.html` directly, or
- run `python3 -m http.server 4173` inside this repo

## Deploy

Deploy directly with Vercel from this folder.
