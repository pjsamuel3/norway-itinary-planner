# Oslo Visit — GitHub Pages Website Spec

## Project Overview

Build a beautiful, single-page static website for a family trip itinerary: a London family visiting Oslo in May 2025. Hosted on GitHub Pages. No build tools required — pure HTML, CSS, and vanilla JS in a single `index.html` file (plus any assets).

---

## Goals

- Display a structured travel itinerary in a visually polished, readable format
- Work perfectly on mobile (guests will use this on their phones)
- Fast, lightweight, no frameworks, no dependencies except Google Fonts
- Easy to update — content lives in clearly commented HTML sections

---

## Aesthetic Direction

**Scandinavian editorial** — clean, confident, typographically driven. Think Norwegian travel magazine meets architect's notebook. Not cold — warm and inviting, like a well-designed cabin.

- **Palette:** Off-white background (`#F7F4EF`), deep ink navy (`#1A1F2E`), warm fjord teal accent (`#3D7E7A`), soft birch cream for cards (`#EDE9E0`)
- **Typography:**
  - Display/headings: `Playfair Display` (Google Fonts) — editorial, characterful
  - Body: `Source Serif 4` (Google Fonts) — warm and readable
  - Labels/metadata: `DM Mono` (Google Fonts) — subtle technical feel for dates, times, links
- **Motion:** Staggered fade-up on scroll for each day/section card. Subtle hover lifts on cards.
- **Layout:** Single column, generous whitespace. Section headers break left with a teal rule. Cards for each activity with emoji icon, title, description, and optional links.
- **No generic AI aesthetics** — no purple gradients, no Inter, no rounded pill buttons

---

## Site Structure

### Header
- Large display title: **"Oslo, May 2025"**
- Subtitle: *"A guide for our visit"*
- Short intro sentence (1 line)
- Sticky nav with jump links: Arrival · Nesodden · Tuesday · Wednesday · Thursday

### Sections (one per day/phase)

Each section has:
- Day label (e.g. `SAT 23 MAY`) in DM Mono
- Section title (e.g. "Arrival & Airport")
- Optional intro note in italic
- Activity cards (see below)

### Activity Card Component

Each card contains:
- Emoji icon (left)
- Activity title (bold)
- Short description (1–3 sentences)
- Optional tags: `🕐 Opening hours`, `🔗 Website`, `📍 Google Maps`
- Links open in new tab

### Footer
- Simple: *"Made with love for a long-overdue visit. Oslo, May 2025."*

---

## Content

Populate the site with the following itinerary content exactly:

---

### Saturday 23 May — Arrival

**Where to stay — airport area**

> Arriving 21:45. Recommend staying near Gardermoen — no stress with tired kids.

- 🏨 **Radisson Blu Airport Hotel** *(Host recommendation)*
  Short covered walk directly to/from the terminal. Reliable, easy, good breakfast. Best for early morning flights.
  📍 [Google Maps](https://maps.google.com/?q=60.192577,11.095312) · ☎️ +47 63 93 30 00

- 🏨 **Radisson Red Oslo Airport** *(Host recommendation)*
  More modern and design-led, ~5 min walk to the terminal. Stylish rooms, great if you want something a bit hipper.
  📍 [Google Maps](https://maps.google.com/?q=60.189782,11.102034) · ☎️ +47 67 02 41 00

- 🏨 **Comfort Hotel Runway** *(Budget option)*
  Requires a shuttle bus (80 NOK/person). Significantly cheaper, breakfast from 4am. Less convenient late at night with kids.
  📍 [Google Maps](https://maps.google.com/?q=60.193262,11.071843) · ☎️ +47 63 94 88 88

---

### Sunday & Monday (Bank Holiday) — Nesodden

> Staying with us on Nesodden — plans TBC, but expect fjord, forest and good food.

*(Placeholder — content to be added)*

---

### Tuesday — Oslo Day 1

- 🚲 **E-bike through the city**
  Borrowing our electric bike (fits both kids on the back). Route: Vigeland Park → waterfront → Opera House.

- 🌿 **Vigeland Park**
  Free, open 24 hours. Gustav Vigeland's monumental sculpture park — enormous and great for kids to roam. One of Oslo's unmissables.
  📍 [Google Maps](https://maps.google.com/?q=59.927029,10.700865)

- 🎭 **Oslo Opera House**
  Walk up the sloping white marble roof for panoramic fjord views. Free to explore outside.
  📍 [Google Maps](https://maps.google.com/?q=59.907489,10.753128)

---

### Wednesday — Oslo Day 2

- 🏔️ **Holmenkollen Ski Jump**
  Take the Metro (T-bane line 1) up to Holmenkollen. Ride to the top of the ski jump for extraordinary views over Oslo and the fjord. Ski museum on site.
  🕐 Open daily 10:00–16:00
  📍 [Google Maps](https://maps.google.com/?q=59.965009,10.664657)

- 🌲 **Hiking from Holmenkollen**
  Marked trails lead directly into the Nordmarka forest from the jump. Easy, well-signposted, manageable for a 6 and 9 year old.

- 👁️ **Grefsenkollen Viewpoint**
  Alternative or add-on viewpoint — panoramic Oslo view, accessible by a different Metro line. Could combine with Teknisk Museum nearby.

- 🔬 **Norsk Teknisk Museum** *(Norwegian Museum of Science and Technology)*
  100+ hands-on exhibits including a science centre, oil rig simulator, model railway, aviation hall and more. Outstanding for kids and adults.
  🕐 Tue–Fri 09:00–16:00 | Closed Mondays
  🔗 [tekniskmuseum.no](https://www.tekniskmuseum.no/en/)
  📍 [Google Maps](https://maps.google.com/?q=59.966936,10.783378)

- 🚶 **Maridalsvatnet**
  Oslo's main reservoir — lovely easy lakeside walk, very manageable for young kids. Beautiful in late May.
  📍 [Google Maps](https://maps.google.com/?q=59.985000,10.765000)

---

### Thursday — Oslo Day 3

- ⚓ **Aker Brygge**
  Oslo's main waterfront district. Great for a morning wander, lunch, coffee, watching the harbour.
  📍 [Google Maps](https://maps.google.com/?q=59.909958,10.725805)

- 🛁 **KOK Floating Sauna**
  Wood-fired floating sauna at Aker Brygge — heat up, then plunge into the fjord. One of Oslo's most memorable experiences.
  ⚠️ *Check kid policy when booking*
  🕐 Open daily from 07:00
  📍 [Google Maps](https://maps.google.com/?q=59.909271,10.726909)

- 🏰 **Akershus Fortress**
  13th century fortress on the fjord — free to enter, cobbled grounds, excellent harbour views. Easy walk from Aker Brygge.
  🕐 Open daily 06:00–21:00
  📍 [Google Maps](https://maps.google.com/?q=59.907586,10.737084)

- 🎨 **Tjuvholmen**
  Adjacent to Aker Brygge — sculpture beach, Astrup Fearnley modern art museum, great architecture.
  📍 [Google Maps](https://maps.google.com/?q=59.907723,10.721885)

- 🚢 **Fram Museum** *(via ferry)*
  Take ferry Line 91 from Aker Brygge. Board the Fram — the world's strongest wooden ship, used in Arctic and Antarctic polar expeditions. Immersive and excellent for kids.
  🕐 Open daily 10:00–17:00
  📍 [Google Maps](https://maps.google.com/?q=59.903381,10.699729)

- 🖼️ **Munch Museum**
  Home of The Scream and thousands of other Munch works. World-class, beautifully designed building with fjord views. **Free entry on Wednesday evenings.**
  🕐 Tue–Sun 10:00–18:00 (Wed/Thu/Fri/Sat until 21:00)
  📍 [Google Maps](https://maps.google.com/?q=59.905904,10.755261)

---

## Technical Requirements

- Single `index.html` file — everything inline (CSS in `<style>`, JS in `<script>`)
- Google Fonts loaded via `<link>` tag (Playfair Display, Source Serif 4, DM Mono)
- Mobile-first responsive design — works well on iPhone screen width (375px+)
- Smooth scroll for nav jump links
- Scroll-triggered fade-in animations using `IntersectionObserver`
- No external JS libraries
- Valid HTML5, accessible (semantic elements, alt text where needed)
- Meta tags: title, description, `og:title`, `og:description` for sharing
- GitHub Pages compatible — no server-side code, relative paths only

---

## GitHub Pages Setup Notes

- Repo name suggestion: `norway-itinary-planner`
- Enable GitHub Pages from `Settings > Pages > Deploy from branch: main, / (root)`
- The site will be live at: `https://[your-username].github.io/oslo-may-2026/`
- To update content: edit the HTML directly and push to main

---

## File Structure

```
oslo-visit-2026/
├── index.html        ← entire site (HTML + CSS + JS)
├── SPEC.md           ← this file
└── README.md         ← itinerary in plain markdown (for GitHub)
```
