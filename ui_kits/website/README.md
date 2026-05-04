# DevQA Website UI Kit

## Overview
High-fidelity recreation of Cristian Esplana's personal portfolio website (`devqa.github.io`).

## Pages Covered
- **Home** — Hero welcome + scrollable section preview cards (Projects, About, Contact)
- **Projects** — Year-grouped project cards with tech tags + achievement items
- **About** — Profile details + photography hobby gallery
- **Contact** — Contact info card + message form

## Usage
Open `index.html` for the interactive click-through prototype. All navigation works between pages.

## Design Notes
- Mobile-first layout, max-width ~600px content column
- Full-bleed background photo with frosted glass overlay
- Dark/light mode toggle persisted in localStorage
- Font Awesome 6 for all iconography
- Talina DEMO for display/logo text
- Segoe UI for body text

## Components
- `Header` — sticky nav with logo, theme toggle, search, menu button
- `NavModal` — fullscreen slide-down navigation
- `PreviewCard` — tinted home section preview cards
- `ProjectCard` — semester project cards with meta, tags, thumbnail
- `AchievementItem` — left-bordered achievement rows
- `DetailModal` — frosted glass project detail overlay
- `GalleryGrid` — 2-col photo gallery with captions
- `ContactForm` — email + message form
- `Footer` — social links + copyright
