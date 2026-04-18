# Copilot Instructions — Oslo Family Itinerary Site

## What this is
A single-page static travel itinerary website for a London family visiting Oslo in May 2026.
Hosted on GitHub Pages at https://pjsamuel3.github.io/norway-itinary-planner/.

**Audience:** Two adults showing it to their kids (aged 9 and 6) to get excited about the trip.
Design must work beautifully on a phone screen first.

---

## Stack — keep it simple
- **Single file:** everything lives in `index.html` — CSS in `<style>`, JS in `<script>`
- **No build tools, no frameworks, no npm**
- **Google Fonts only** as external dependency (Playfair Display, Source Serif 4, DM Sans, DM Mono)
- **Unsplash** for open-source photography (free, no attribution required for editorial use)
- **GitHub Pages** compatible — no server-side code, relative paths only

---

## Design system

### Colours
```css
--bg:          #FAFAF8   /* warm off-white page background */
--ink:         #0D1B2A   /* primary text — deep navy */
--ink-soft:    #3D4A58   /* secondary text */
--teal:        #2A7C6F   /* primary accent — fjord teal */
--teal-bg:     #E8F5F3   /* teal tint for context notes */
--orange:      #E8763A   /* secondary accent — day tags, highlights */
--orange-bg:   #FDF0E8   /* orange tint */
--card-bg:     #FFFFFF   /* card surface */
--card-border: #E6E0D8   /* card border */
--muted:       #7A7269   /* metadata, labels */
```

### Typography
| Role | Font | Usage |
|------|------|-------|
| Display / hero | Playfair Display 700–900 | H1, chapter h2, footer wordmark |
| Body copy | Source Serif 4 300–400 | Card descriptions, context notes |
| UI / labels | DM Sans 400–600 | Card titles, buttons, nav |
| Metadata | DM Mono 300–400 | Day tags, opening times, badges |

### Card colour rails
Left-edge 4px accent bar signals activity type:
- `rail-teal`   → accommodation, waterfront
- `rail-green`  → free outdoor / nature
- `rail-orange` → highlight / must-do
- `rail-blue`   → culture / museums
- `rail-purple` → arts / architecture
- `rail-red`    → paid experiences / bookings

### Badges
```html
<span class="badge badge-host">Host pick</span>   <!-- orange tint -->
<span class="badge badge-budget">Budget</span>     <!-- green tint  -->
<span class="badge badge-kids">⭐ Kids love it</span>  <!-- yellow tint -->
<span class="badge badge-free">Free</span>         <!-- green tint  -->
<span class="badge badge-book">Book ahead</span>   <!-- blue tint   -->
```

### Kid excitement rating
Show on activities kids will love:
```html
<div class="kid-bar">
  <span class="kid-stars">⭐⭐⭐</span>
  <span>One-line reason kids love it</span>
</div>
```
Max three stars. Use two stars for "good," three for "unmissable for kids."

---

## Content structure

### Section IDs (used by nav anchors)
| ID | Day |
|----|-----|
| `#arrival`   | Saturday 23 May — airport hotels |
| `#nesodden`  | Sunday–Monday — staying with hosts |
| `#tuesday`   | Oslo Day 1 — city bike loop |
| `#wednesday` | Oslo Day 2 — Holmenkollen + forest |
| `#thursday`  | Oslo Day 3 — waterfront + museums |

### Adding a new activity card
Copy this pattern into the relevant `.cards` div:
```html
<article class="card fade-up">
  <div class="rail rail-teal"></div>   <!-- pick appropriate colour -->
  <div class="card-inner">
    <span class="card-emoji" aria-hidden="true">🗺️</span>
    <div class="card-body">
      <div class="card-row1">
        <h3 class="card-title">Activity Name</h3>
        <div class="badges">
          <span class="badge badge-free">Free</span>
        </div>
      </div>
      <p class="card-desc">Description here.</p>
      <div class="card-meta">
        <span>🕐 Opening hours</span>
      </div>
      <div class="card-actions">
        <a href="GOOGLE_MAPS_URL" target="_blank" rel="noopener" class="btn btn-map">📍 Map</a>
        <a href="WEBSITE_URL"     target="_blank" rel="noopener" class="btn btn-web">🔗 Website</a>
      </div>
      <div class="kid-bar">
        <span class="kid-stars">⭐⭐</span>
        <span>Why kids love it</span>
      </div>
    </div>
  </div>
</article>
```

### Section chapter header photos
Each day section has a full-width Unsplash photo as its header.
Classes `ch-arrival`, `ch-nesodden`, `ch-tuesday`, `ch-wednesday`, `ch-thursday`
are defined in CSS with `background-image` + `background-color` fallback.
To update a photo: change the `background-image` URL in the matching CSS rule.
Always keep the `background-color` fallback — it shows if the image fails to load.

---

## Conventions

- **Mobile-first:** design for 375px, then use `@media (min-width: 640px)` for larger screens
- **Scroll animations:** use the `.fade-up` class; `IntersectionObserver` adds `.in` to trigger
- **All external links:** `target="_blank" rel="noopener"`
- **Accessible section headers:** each section has `aria-labelledby` pointing to its `h2`
- **Images:** always include `alt` text; section backgrounds use `role="img" aria-label="..."`
- **No comments that describe what the code does** — names and structure should be self-documenting
- **No external JS libraries** — vanilla JS only

---

## PR workflow
- Branch naming: `feature/`, `fix/`, `content/`
- One logical change per PR
- PRs should reference what section/activity changed
- Merge to `main` → auto-deploys to GitHub Pages (allow ~1 min)

---

## Photos (Unsplash)
Format for embedding:
```
https://images.unsplash.com/photo-{ID}?auto=format&fit=crop&w={WIDTH}&q=80
```
- Section headers: `w=1400`
- Hero: `w=1800`
- All photos are free to use without attribution (Unsplash licence)
