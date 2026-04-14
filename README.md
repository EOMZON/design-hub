# Design Index

Static index site for `design.zondev.top`.

## Purpose

`design-hub` now ships the public site under the brand **Design Index**.

The site should do one job well:

- present the design network as a growing index instead of a fixed portal
- organize entry by **dimension**, not by historical repo or product naming
- let visitors scan current live layers first, then enter a focused route
- leave room for new dimensions without redoing the homepage each time

## UX Rule

The homepage should answer three questions quickly:

1. What is this?
2. How is it organized?
3. Which dimension should I enter?

That means:

- clear site identity first: `Design Index`
- a short tagline: `Design resources, by dimension.`
- current live dimensions separated from planned / future dimensions
- each live card must explain what that dimension collects
- cards can open a focus view, but the homepage must still work as an index even before any click

## Current Live Dimensions

### Web Visual

- use for: website direction, style families, references, visual prompts
- live target: `https://webdesign.zondev.top/browse`

### UX & Flow

- use for: information architecture, user path, service clarity, flow audit
- live target: `https://ux.zondev.top`

### Icon & Assets

- use for: icon systems, favicon, recognition rules, small-scale assets
- live target: `https://icon.zondev.top`

### Methods

- use for: reusable skills, prompts, constraints, workflow assets
- live target: `https://github.com/EOMZON/design-skills`

## Growth Model

The homepage should be able to grow without changing its core pattern.

Use two layers:

- `Current Dimensions`: live cards with preview + focus view + external link
- `Growing Structure`: planned dimensions that are not live yet, but already have a place in the index

This avoids turning the homepage into another fixed 4-slot gateway.

## Technical Notes

- static site only; no build step
- main implementation lives in `index.html`
- Vercel serves the folder as-is
- iframe preview is viable for:
  - `webdesign.zondev.top`
  - `ux.zondev.top`
  - `icon.zondev.top`
- GitHub does not allow iframe embedding for `design-skills`, so `Methods` uses a local README render + external links
- focus mode is a frontend shell only; deep content stays in the specialized sites

## Local Preview

- open `index.html` directly, or
- run `python3 -m http.server 4173` inside this repo

## Deploy

Deploy directly with Vercel from this folder.
