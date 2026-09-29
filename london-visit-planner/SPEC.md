# London Visit Guide — Website Spec

## Overview

A single-page, mobile-first static website: a host's guide to London for a visiting guest (Una) and their family group, including two children aged 10 and 15. It mirrors the structure of the [Oslo itinerary site](https://github.com/pjsamuel3/norway-itinary-planner). The page is organised by section rather than by day, because the days haven't been planned yet (see Open Questions).

---

## Content structure

- **h1:** site title ("London")
- **h2:** one per section: The Basics · Sights · Full-day trips · Food & Drink · Adults only · Open Questions
- **h3:** one per place or activity, with an emoji before it (🏛️ 🦕 🚀 🎭 🎨 🎡 🌀 💎 🌿 ⛵ 🍳 🍷 🌆 🥑 🥐 ☕ 🔥 🥂 🍸)

Each place card contains:
- A one-line description
- 📍 A Google Maps link in the form `https://maps.google.com/?q=LAT,LONG`
- 🕐 Opening hours and ☎️ phone number, where relevant
- Tag badges:
  - **Host recommendation ⭐**: the host's personal favourites (British Museum, Bill's Soho, Gordon's Wine Bar, Duck & Waffle)
  - **Family**: suitable for the 10- and 15-year-old
  - **Best for the teen**: better suited to the 15-year-old (Crystal Maze)
  - **Adults only / Best for adults**: not for the kids (Trisha's, Gordon's)
  - **Free**, **Book ahead**

Practical advice appears in `<blockquote class="tip">` callouts that begin with **Tip:**. These are the HTML version of Markdown's `> Tip:`.

The page ends with an **Open Questions** checklist. The boxes start unchecked. Ticks are saved in the viewer's own browser (`localStorage`) and are never shared.

---

## Design

- **Dark by default**, with a light palette under `prefers-color-scheme: light`. All colours are CSS custom properties on `:root`.
- The accent is London-bus red (`#E5484D` in dark mode, `#C8102E` in light), with teal for map buttons and gold for host picks and tips.
- **Fonts** (Google Fonts, the same set as the Oslo site): Playfair Display for headings, Source Serif 4 for descriptions, DM Sans for the UI, and DM Mono for labels.
- **Section headers** use gradients with a large emoji watermark instead of photos. That means no external image hosts and nothing to break.
- **Navigation:** a sticky top nav on desktop (≥720px) and a fixed bottom tab bar on mobile, which highlights the section in view.
- Cards fade in on scroll using `IntersectionObserver`. The animation is switched off when the viewer has `prefers-reduced-motion` set.

---

## Technical requirements

- A single `index.html` with CSS in `<style>` and JS in `<script>`
- No build tools, frameworks, npm or JS libraries. Google Fonts is the only external request.
- Mobile-first: works at 375px width with no horizontal scroll
- Semantic HTML5: `header`, `main`, `section`, `article`, `nav`, and a `table` for the basics
- External links use `target="_blank" rel="noopener"`
- Meta tags: `title`, `description`, `og:title`, `og:description`, `theme-color`, `color-scheme`

---

## GitHub Pages setup

- Repo: `london-visit-planner`
- **Settings → Pages → Deploy from a branch → `main` / `(root)`**
- Live at: `https://pjsamuel3.github.io/london-visit-planner/`
- To update: edit `index.html` (and `README.md` to keep them in sync) and push to `main`

---

## File structure

```
london-visit-planner/
├── index.html   ← the whole site (HTML + CSS + JS)
├── README.md    ← the guide as plain Markdown (renders on GitHub)
└── SPEC.md      ← this file
```
