# DevQA — Design System

## Overview

**DevQA** (also stylized as "DQ") is the personal portfolio and brand of **Cristian Esplana**, a 2nd-year BSIT (Bachelor of Science in Information Technology) student at PUP Paranaque, Philippines. Cristian works as a freelance QA Analyst and aspires to become a Senior QA Automation Engineer.

The brand serves a dual purpose:
1. **Personal Portfolio Website** (`devqa.github.io`) — a mobile-first, single-page-style personal site showcasing academic projects, personal details, and a contact form.
2. **DevQA Brand Identity** — the "DQ" monogram logo conveys quality assurance (checkmark) and development, serving as a personal brand for freelance and professional work.

### Sources
- **GitHub Repo:** `puppq-bsit-cristianlesplana/devqa.github.io` (public, `main` branch)
  - `index.html`, `projects.html`, `about.html`, `contact.html`
  - `style.css`, `script.js`
  - `LOGO.png`, `DEVQA FAV.png`, `portfolio-background-header-53082_1080x675.jpg`
  - `473167842_1277725740165776_4760458389630140038_n.png` (PolyCal app mockup)
  - `501349887_1279814190234263_7639640468511384140_n.png` (PolyCal secondary mockup)
- No Figma link was provided.
- No slide deck was provided.

### Products / Surfaces
| Surface | Description |
|---|---|
| Portfolio Website | Multi-page static site with Home, Projects, About, Contact |
| DevQA Brand | Logo, favicon, personal brand mark |
| PolyCal | Student calendar app (separate repos: Tkinter desktop, Kivy mobile) |

---

## CONTENT FUNDAMENTALS

### Voice & Tone
- **First-person, direct:** Cristian writes in the first person ("I'm Cristian Esplana," "I capture stories through my lens").
- **Professional but approachable:** The site balances student warmth with professional ambition. Not stiff; not overly casual.
- **Achievement-oriented:** Copy leans into accomplishments and goals ("Senior QA Automation Engineer," "Dual-Platform Release").
- **Concise:** Descriptions are short. No long paragraphs. Cards use 1–3 sentence descriptions.

### Casing
- **Nav items:** ALL CAPS (`HOME`, `PROJECTS`, `ABOUT ME`, `CONTACT US`).
- **Section headings:** Title Case or ALL CAPS (`Past Semester Projects`, `CONTACT US`).
- **Card headings:** Title Case (`POLYCAL v1`, `Book Inventory CRUD`).
- **Body text:** Sentence case.

### Terminology
- Projects are referred to by name + version (e.g. "POLYCAL v1", "POLYCAL v2").
- Academic context is stated (e.g. "Comprog 1", "2nd Year BSIT Student").
- Tech stacks are listed as compact badges.

### Emoji Usage
- **No emoji** in the main site UI. Font Awesome icons are used exclusively in place of emoji for all UI decoration.
- One small exception: the menu button uses ☰ (hamburger unicode char, not emoji).

### Examples of Copy
- Hero: *"Hello, I'm Cristian Esplana. College Student, Freelance QA Analyst & Aspiring Web Developer."*
- Project: *"A student calendar desktop app for Polytechnic students to manage schedules, deadlines, and subjects — built with Python (Tkinter)."*
- Achievement: *"Successfully delivered the same project across two platforms (Desktop & Mobile) across consecutive semesters using different Python frameworks."*

---

## VISUAL FOUNDATIONS

### Color System
The palette is a **navy + electric blue + green** triad, conveying tech, trust, and quality assurance.

| Token | Value | Usage |
|---|---|---|
| `--primary` | `#2c3e50` | Dark navy — headers, logo bg, primary UI elements |
| `--accent` | `#3498db` | Electric blue — links, tags, highlights, gradient partner |
| `--green` | `#2ecc71` / `#41c96d` | Logo checkmark, success, QA-pass metaphor |
| `--bg-overlay-light` | `rgba(244,247,246,0.85)` | Frosted light background overlay |
| `--bg-overlay-dark` | `rgba(18,18,18,0.85)` | Frosted dark background overlay |
| `--card-bg-light` | `rgba(255,255,255,0.9)` | Card surfaces, light mode |
| `--card-bg-dark` | `rgba(30,30,30,0.9)` | Card surfaces, dark mode |
| `--text-light` | `#333` | Body text, light mode |
| `--text-dark` | `#e0e0e0` | Body text, dark mode |
| `--border-light` | `#ddd` | Borders, dividers, light mode |
| `--border-dark` | `#444` | Borders, dividers, dark mode |
| `--shadow-light` | `rgba(0,0,0,0.1)` | Card shadows, light mode |
| `--shadow-dark` | `rgba(0,0,0,0.4)` | Card shadows, dark mode |

**Gradient usage:** The header uses a horizontal `linear-gradient(90deg, #2c3e50 → #3498db)`. Section preview cards each have a distinct tinted gradient (blue→teal for Projects; purple→pink for About; orange→red for Contact). Page headings use a clip-path gradient text treatment (`--primary` → `--accent`).

### Typography
- **Primary font:** `'Segoe UI', sans-serif` — system font stack, no custom webfont.
- **Logo text:** `CRISTIAN` set in bold, 1.4–1.6rem, white, inline with logo icon.
- **Nav links:** 1.5–2rem, bold, accent-colored.
- **Section headings (h2):** 1.3–2.4rem, gradient text clip.
- **Card headings (h3):** 1.05–1.5rem.
- **Body / card text:** 0.78–0.95rem.
- **Tags/badges:** 0.72rem, bold or semi-bold.

### Backgrounds
- The global background is a **full-bleed fixed photograph** (`portfolio-bg.jpg` — a dark portfolio/bokeh image), overlaid with a semi-transparent frosted layer (`::before` pseudo-element). This creates a depth effect where content cards float above the image.
- No tiling patterns or hand-drawn illustrations.
- No gradient-only backgrounds (the photo is always present underneath).

### Cards
- `border-radius: 12–16px` (cards), `8–10px` (inner elements).
- `backdrop-filter: blur(10–14px)` — frosted glass effect on all card surfaces.
- `box-shadow: 0 4px 10px var(--shadow)` — soft, offset shadow; heavier in dark mode.
- `border: 1px solid var(--border)` — thin, subtle borders.
- Card backgrounds are semi-transparent (`rgba`), not solid fills.
- Preview item cards have colored tinted gradients (blue/teal, purple/pink, orange/red).

### Spacing & Layout
- Max content width: `600px` (mobile), up to `1160px` (desktop).
- Grid: `grid-template-columns: 1fr 1fr` for two-column layouts on tablet+.
- Section padding: `14–40px` depending on breakpoint.
- Gap between cards: `12–20px`.
- Mobile-first responsive with breakpoints at `375px`, `600px`, `768px`, `1260px`.

### Shadows & Elevation
- Cards: `0 4px 10px var(--shadow)`
- Active/modal boxes: `0 8px 32px var(--shadow)` / `0 20px 60px rgba(0,0,0,0.35)`
- No inset/inner shadows used.

### Borders & Corner Radii
- Cards/modals: `12–16px`
- Buttons: `4–8px`
- Tags/badges: `10–20px` (pill shape)
- Tech stack chips: `10px`
- Image thumbnails: `6–10px`

### Animations & Transitions
- Hover: `transform: translateY(-4px)` + heavier shadow on gallery items.
- Modal entrance: `@keyframes detailSlideIn` — `opacity: 0 → 1` + `translateY(20px) → 0` + `scale(0.97 → 1)`, duration `0.25s ease`.
- Nav modal: slides in from `top: -100%` with `transition: top 0.4s`.
- Theme toggle: `transition: background 0.4s ease` on the body overlay.
- Search box: `transition: width 0.3s` on expand.
- No bounce animations. No spring physics. Easing is `ease` or `ease-in-out`.

### Hover & Press States
- Links/social icons: opacity dimming on hover (`opacity: 0.85`).
- Gallery items: `translateY(-4px)` lift + shadow deepens.
- Buttons: no explicit press/active state beyond cursor change; implicit browser behavior.
- Close buttons: `opacity: 0.6 → 1` on hover.
- Thumbnails: `opacity 0.85–0.88` on hover with `cursor: zoom-in`.

### Dark Mode
- Full dark mode via `body.dark` class, toggled by a moon/sun button, persisted in `localStorage`.
- The header gradient deepens to near-black navy in dark mode.
- Cards shift to `rgba(30,30,30,0.9)`.
- Text becomes `#e0e0e0`.

### Imagery
- **PolyCal mockups** — actual app screenshots (PNG).
- **Gallery/placeholder images** — `picsum.photos` used for hobby gallery and project thumbnails (warm/cool natural photography style).
- No grain, no duotone, no B&W treatment. Color photography with natural tones.
- Images displayed with `object-fit: cover`, consistent aspect ratios.

---

## ICONOGRAPHY

### Icon System: Font Awesome 6
The site uses **Font Awesome 6.0.0** loaded from CDN:
```
https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css
```
All icons are `<i class="fa fa-*">` or `<i class="fab fa-*">` inline elements. No SVG icons, no PNG icon sprites, no custom icon font.

### Icon Usage Patterns
| Context | Icon(s) |
|---|---|
| Navigation sections | `fa-code` (Projects), `fa-user` (About), `fa-envelope` (Contact) |
| Project types | `fa-calendar-check` (PolyCal), `fa-gamepad` (Tic-Tac-Toe), `fa-project-diagram` (Linking), `fa-book` (Book Inventory) |
| Platform tags | `fa-desktop`, `fa-mobile-alt`, `fa-users`, `fa-user` |
| Achievements | `fa-certificate`, `fa-trophy`, `fa-code-branch` |
| Contact info | `fa-phone`, `fa-envelope`, `fa-map-marker-alt` |
| Social links | `fab fa-facebook`, `fab fa-instagram`, `fab fa-linkedin` |
| UI chrome | `fa-moon` / `fa-sun` (theme toggle), `fa-paper-plane` (send), `fa-arrow-right` |
| Year label | `fa-calendar-alt` |

### Logo Mark
The **DQ logo** (LOGO.png / DEVQA FAV.png) is a custom mark:
- Square with rounded corners (`~20px` radius), filled `#2c3e50` (primary navy).
- White semi-transparent "D" letterform on the left.
- Green (`#41c96d`) circular "Q" with a checkmark bisecting it — the "QA pass" metaphor.
- Available as PNG (500×500). No SVG source in the repo.
- Used as `60×60px` logo icon in the header alongside the "CRISTIAN" wordmark.

---

## FILE INDEX

```
/
├── README.md                         ← This file
├── SKILL.md                          ← Agent skill definition
├── colors_and_type.css               ← CSS design tokens (colors, type, spacing)
├── fonts/
│   └── Talina_DEMO.otf               ← Brand display font (DEMO — license needed for production)
├── assets/
│   ├── LOGO.png                      ← DQ logo mark (500×500 PNG)
│   ├── DEVQA FAV.png                 ← Favicon / alternate logo (1024×1024 PNG)
│   ├── polycal-mockup.png            ← PolyCal app screenshot #1
│   ├── polycal-mockup-2.png          ← PolyCal app screenshot #2
│   └── portfolio-bg.jpg              ← Full-bleed background photo
├── preview/                          ← Design System tab cards
│   ├── colors-brand.html             ← Brand color swatches (navy, blue, green + extended)
│   ├── colors-semantic.html          ← Semantic / dark-mode tokens + header gradients
│   ├── colors-card-gradients.html    ← Tinted card gradient variants
│   ├── type-talina-specimen.html     ← Talina DEMO full specimen
│   ├── type-scale.html               ← Full size scale — Talina display + Segoe UI body
│   ├── type-headings.html            ← Gradient text + header lockup treatments
│   ├── type-tags.html                ← Subject tags, platform tags, tech chips, year labels
│   ├── spacing-tokens.html           ← Spacing scale + border radius system
│   ├── spacing-shadows.html          ← 4-level shadow elevation system
│   ├── components-header.html        ← Sticky header — light + dark
│   ├── components-cards.html         ← Card variants (generic + 3 tinted)
│   ├── components-project-card.html  ← Full project card with meta, tags, thumbnail
│   ├── components-achievement.html   ← Left-bordered achievement row
│   ├── components-buttons.html       ← Buttons, inputs, textarea
│   ├── components-modal.html         ← Detail modal — frosted glass, slide-in
│   ├── brand-logo.html               ← Logo on dark/light/photo + favicon + lockup
│   ├── brand-background.html         ← Full-bleed photo + light/dark overlay
│   └── brand-iconography.html        ← Font Awesome 6 icon set by category
└── ui_kits/
    └── website/
        ├── README.md                 ← UI kit guide
        └── index.html                ← Interactive portfolio prototype (Home/Projects/About/Contact)
```

## Font Note
**Talina DEMO** (`fonts/Talina_DEMO.otf`) is used as the brand display font for hero headings and the logo wordmark. The DEMO version may have limited glyph coverage — obtain a full license for production use. The `--font-display` CSS variable in `colors_and_type.css` references it; swap the file path when upgrading.

## Icon Note
All icons are **Font Awesome 6.0.0** from CDN (`cdnjs.cloudflare.com`). No custom SVG or PNG icons are used. Load with:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```
