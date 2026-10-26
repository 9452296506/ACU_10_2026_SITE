# Changelog — LUMERA Multi-Page Website

Prepared for **ACURELLA LIMITED** (CY10378872I). Versioning: [Semantic Versioning](https://semver.org/).

Development: daily stages of **8 working hours**, 7 – 26 October 2026 (14 working days · 112 h).

---

## [0.1.0] — 2026-10-07 · Project setup & UX planning (8 h)

### Added
- Brief analysis: 5-page structure, Guatemalan market, price Q229
- Content extracted from the client's existing Lumera landing page (claims, ingredients, usage, 4-week programme, testimonials) and reworked into page copy in Spanish
- Site map and navigation: Inicio | Producto | Cuidado diario | Ingredientes | FAQ + legal pages
- Wireframes for the five main pages (desktop, mobile) and conversion sections
- Project scaffolding: `css/`, `js/`, `images/`

## [0.2.0] — 2026-10-08 · Design system & shared frame (8 h)

### Added
- Design tokens from the packaging (cream / sage / terracotta / rose-gold), Cormorant Garamond + Jost, spacing and component styles (`css/base.css`)
- Announcement bar, sticky header with centred wordmark, main navigation, footer (tagline, legal links, contact)
- Mobile slide-in navigation with overlay, ESC and close-button handling (`js/ui.js`)
- Button, form, badge and notice primitives with validation states

## [0.3.0] — 2026-10-09 · Home page, part 1 (8 h)

### Added
- Hero with product photo, dual CTA, rating strip
- USP strip
- Product presentation with price and add-to-bag
- Benefits grid (6 cards)

## [0.4.0] — 2026-10-12 · Home page, part 2 (8 h)

### Added
- Target-audience section with social-proof badge
- Ingredients teaser
- 3-step usage section, results-by-zone section, reviews with rating summary
- Order section (Name + Phone form, privacy consent)

## [0.5.0] — 2026-10-13 · Product page, part 1 (8 h)

### Added
- Gallery (6 photos) with thumbnails, product info, checklist, price, meta strip, specification list
- Description and usage blocks
- Packaging & presentation section
- Breadcrumbs for subpages

## [0.6.0] — 2026-10-14 · Product page, part 2 & cart (8 h)

### Added
- Cart (`js/cart.js`): add to bag, quantity, drawer, `localStorage` persistence, header badge, quetzal formatting
- Checkout modal wired to the lead form with order summary
- Ingredients summary grid, results cards (3) with disclaimers, expectations timeline
- Precautions block, reviews (6), delivery & payment table, order section

## [0.7.0] — 2026-10-15 · Daily care page (8 h)

### Added
- Page hero, dose block (3–5 drops · 1–2×/day · 4 weeks)
- Morning and evening routines (step grids)
- Application technique by facial zone
- Compatibility with other cosmetics, storage & travel tips
- 4-week programme cards, CTA banner

## [0.8.0] — 2026-10-16 · Ingredients page & site search (8 h)

### Added
- Split page hero
- Featured ingredient (hydrolysed collagen) with INCI
- 4 ingredient cards (grape leaf extract, panthenol, prickly pear extract, allantoin) with INCI
- "Free from" strip, INCI notice, synergy section, banner strip
- Site search overlay with static index (`js/main.js`)

## [0.9.0] — 2026-10-19 · FAQ & legal pages (8 h)

### Added
- FAQ page: "Producto y uso" (8), "Pedidos, pago y envío" (6), order section
- Privacy Policy, Cookie Policy, Terms & Conditions (Guatemala)
- Cookie notice with accept/decline and persisted consent
- Back-to-top button, smooth anchor scrolling

## [0.10.0] — 2026-10-20 · Imagery, forms & lead integration (8 h)

### Added
- Client product photography processed: 3024×4032 → 1600 px, JPEG q85 (≈2 MB → ≈300 KB each); other assets WebP; descriptive file names
- Image-to-section mapping on all pages, `alt` texts
- Order forms: validation (name, phone, consent), disabled submit during send, success/error messages
- Lead-submission integration point `LEAD_ENDPOINT` in `js/main.js` (JSON POST, inline server message support)

## [0.11.0] — 2026-10-21 · SEO & structured data (8 h)

### Added
- Titles, meta descriptions, canonical URLs, Open Graph (`es_GT`)
- JSON-LD `Product` (GTQ) and `FAQPage`
- `sitemap.xml`, `robots.txt`; `.htaccess` (clean URLs, caching, WebP MIME)
- Favicon, `lang="es"`

## [0.12.0] — 2026-10-22 · Responsive & accessibility QA (8 h)

### Fixed
- Responsive pass at 1200 / 900 / 620 / 400 px on all 8 pages; hero crops for portrait photos; no horizontal scroll
- Skip link, focus order, `aria-expanded` on accordions, `aria-hidden` on overlays, labelled icon buttons, form error states

## [0.13.0] — 2026-10-23 · Cross-browser & copy QA (8 h)

### Fixed
- Cross-browser check (Chromium, Firefox, WebKit); `file://` smoke test
- Form flows: validation edge cases, checkout from cart, success/error states
- Spanish proofreading (Guatemalan usage)

## [1.0.0] — 2026-10-26 · Final QA & delivery (8 h)

### Added
- Final link and image-weight check
- `README.md`, `DELIVERY.md`, changelog; delivery package (archive + screenshots)

### Notes
- Company data, NIT, contact details and domain are placeholders (see `README.md`, "Placeholders to confirm").
- `LEAD_ENDPOINT` (`js/main.js`) must be set to the client's lead-submission URL to activate live order submissions.

---

**Engagement timeline**

| Milestone | Date |
|---|---|
| Order agreed | 2026-10-06 (18:00) |
| Development (14 working days × 8 h) | 2026-10-07 → 2026-10-26 |
| Delivery & invoice | 2026-10-26 |
