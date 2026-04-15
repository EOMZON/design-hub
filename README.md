# Design Index

Static registry site for `design.zondev.top`.

## Purpose

`design-hub` now ships the public site under the brand **Design Index**.

The site should do one job well:

- present the design network as a growing registry instead of a fixed portal
- organize entry by **dimension**, not by historical repo or product naming
- let visitors scan current live layers first, then understand what is in build and what is only planned
- leave room for new dimensions without redoing the homepage each time

## UX Rule

The homepage should answer three questions quickly:

1. What is this?
2. How is it organized?
3. Which dimension should I enter?

That means:

- clear site identity first: `Design Index`
- a short tagline: `Design resources, by dimension.`
- one unified registry schema for every dimension
- lifecycle states separated in the UI: `live`, `in_build`, `planned`
- each live card must explain what that dimension collects, what the user gets, and what comes next
- cards can open a focus view, but the homepage must still work as a registry even before any click

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

Use one registry with explicit lifecycle states:

- `live`: preview + focus view + external link
- `in_build`: real candidate dimension with current asset / prototype / next step
- `planned`: reserved slot with rationale but no fake live entry yet

This avoids turning the homepage into another fixed 4-slot gateway.

## Current Build Candidate

### Research Boards

- state: `in_build`
- why next: strongest candidate for the 5th true dimension
- current asset: `nishengdao-site` local prototype + existing visual/reference board patterns
- eventual role: evidence boards, reference atlases, relation maps, editorial decision surfaces

## Technical Notes

- static site only; no build step
- main implementation lives in `index.html`
- Vercel serves the folder as-is
- iframe preview is viable for:
  - `webdesign.zondev.top`
  - `ux.zondev.top`
  - `icon.zondev.top`
- GitHub does not allow iframe embedding for `design-skills`, so `Methods` uses a local README render + external links
- registry data currently lives inside `index.html` as one unified array; adding a new dimension should mean adding one new object, not patching multiple sections by hand
- focus mode is a frontend shell only; deep content stays in the specialized sites

## Local Preview

- open `index.html` directly, or
- run `python3 -m http.server 4173` inside this repo

## Deploy

Deploy directly with Vercel from this folder.
