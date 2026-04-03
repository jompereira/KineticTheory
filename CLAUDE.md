# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A static marketing/landing site for **Kinetic Theory**, an independent mobile game studio based in Porto, Portugal (solo founder: José Pereira). No build step, no framework, no dependencies — just plain HTML and CSS files served via GitHub Pages and Netlify.

## Deployment

The site is deployed in two places:
- **GitHub Pages**: `jompereira.github.io/KineticTheory/`
- **Netlify**: site ID `96bde2ed-c79d-4464-859a-576866d15320`

Because GitHub Pages serves from a subdirectory, all internal links must use **relative paths** (`index.html`, `support.html`, etc.) — never root-relative paths like `/` or `/index.html`, which would resolve to the bare domain and break navigation.

## Site structure

Three pages, all self-contained (styles are inline `<style>` blocks, no external CSS file):

| File | Purpose |
|---|---|
| `index.html` | Home — hero, games grid, about section, footer |
| `support.html` | Support contact page |
| `privacy-policy.html` | Privacy policy |

Shared nav is copy-pasted across all three files (no templating). When updating the nav, update all three files.

## Design system

CSS custom properties defined in `:root` on each page:

```
--navy / --navy-mid / --navy-light   dark blue backgrounds
--orange (#f7620a) / --amber         primary accent colours
--blue-pop (#1e90ff)                 secondary accent
--text / --muted / --border          typography and dividers
```

Fonts loaded from Google Fonts: **Barlow Condensed** (headings) and **Barlow** (body).

## Images

| File | Used for |
|---|---|
| `KineticTheory_logo.png` | Nav logomark on all three pages |
| `KineticTheory_logo.jpg` | Alternative format (not currently used in HTML) |
| `AppStoreIcon.png` | Game icon for Maze Racer |
| `logo_grey.png` | Game icon for Connect the Colors |

Nav logomark container is 36×36px with `border-radius: 10px`; image uses `object-fit: cover` to fill it. Game icon container is the same style (defined under `.game-icon img`).

## Games

Currently two titles listed in `index.html`:
- **Maze Racer** — procedurally generated mazes, iOS & Android, Free to play (Active)
- **Connect the Colors** — minimalist puzzle game, iOS & Android, Free to play
