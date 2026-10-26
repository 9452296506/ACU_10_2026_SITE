# LUMERA — Multi-Page Website

Multi-page website for the **Lumera** facial serum (Spanish, Guatemalan market), produced for **ACURELLA LIMITED** (Reg. no. CY10378872I).

| | |
|---|---|
| **Client** | ACURELLA LIMITED — CY10378872I |
| **Source code** | `github.com/9452296506/ACU_10_2026_SITE_CODE` |
| **Documentation** | `github.com/9452296506/ACU_10_2026_SITE` |
| **Product** | Lumera — intensive rejuvenating facial serum · 30 ml dropper bottle |
| **Market / language** | Guatemala · Spanish (es-GT) |
| **Price shown** | Q229 (IVA incluido) |
| **Type** | Static multi-page website: 5 main pages + 3 legal pages |

## Pages & navigation

Main navigation: **Inicio | Producto | Cuidado diario | Ingredientes | FAQ**. "Pedir ahora" (Order) button in the header and in the conversion sections.

| Page | File | Content |
|---|---|---|
| Home | `index.html` | Hero, USP strip, product + price, benefits (6), target audience, ingredients teaser, 3-step usage, results by facial zone, reviews (3), order form |
| Product | `producto.html` | Gallery (6 photos), key info, price, specifications, description, usage, packaging & presentation, ingredients summary, results + timeline, precautions, reviews (6), delivery & payment table, order form, JSON-LD `Product` |
| Daily care | `cuidado-diario.html` | Dose (3–5 drops · 1–2×/day · 4 weeks), morning and evening routines, application technique by facial zone, combining with other cosmetics, storage, 4-week programme |
| Ingredients | `ingredientes.html` | Hydrolysed collagen (featured), grape leaf extract, panthenol, prickly pear extract, allantoin — purpose, benefit, INCI; "free from" strip; synergy |
| FAQ | `faq.html` | 14 questions in 2 groups, JSON-LD `FAQPage`, order form |
| Legal | `privacidad.html`, `cookies.html`, `terminos.html` | Privacy Policy, Cookie Policy, Terms & Conditions (Guatemala), linked in every footer |

## Design

Palette and typography derived from the packaging: cream (`#f8f4ec`), sage (`#6f7f63`), terracotta (`#9c3b26`, action colour), rose-gold (`#c99a6b`). Fonts: Cormorant Garamond (display) + Jost (body). Tokens in `css/base.css`.

## Order forms & lead integration

Forms (Name + Phone + privacy checkbox) on Home, Product, FAQ and in the checkout modal; each tagged with a `source` value. Client-side validation: name ≥ 2 characters, phone ≥ 8 digits, consent required.

Integration point in `js/main.js`:

```js
var LEAD_ENDPOINT = ''; // client's lead-submission URL
// POST JSON: { name, phone, product, qty, price, source, page }
```

While `LEAD_ENDPOINT` is empty, the forms validate and show the success state without sending. Once set, each valid submission is POSTed as JSON; a response `{ ok: false, message }` is shown inline.

## Features

- Cart: add to bag, quantity controls, drawer with `localStorage` persistence (`lm_cart_v1`), checkout modal wired to the lead form; prices formatted as `Q229.00`
- Sticky header, announcement bar, site search overlay (pages, sections, ingredients, FAQs), mobile slide-in menu
- Product gallery, FAQ accordions, breadcrumbs, back-to-top, smooth anchor scrolling
- Cookie notice with accept/decline, persisted in `localStorage` (`lm_cookie_consent`)

## Responsive

Breakpoints: 1200 / 900 / 620 / 400 px. Verified at 1440, 820 and 390 px: no horizontal scroll.

## SEO

- Unique `<title>` and meta description per page; one `h1` per page
- Canonical URLs, Open Graph (`es_GT`), JSON-LD `Product` (GTQ) and `FAQPage`
- `sitemap.xml`, `robots.txt` (legal pages excluded)
- Optional `.htaccess`: clean extensionless URLs, asset caching, WebP MIME type
- Domain used in canonicals/sitemap/robots: `https://lumera.com.gt/`

## Tech stack

HTML5, CSS3, JavaScript + jQuery 3.7. Static site, no build step. CSS: `base`, `components`, `sections`. JS: `ui`, `cart`, `main`. Google Fonts and Font Awesome via CDN. Images: client photography downscaled to ≤1600 px (JPEG q85), remaining assets WebP/PNG.

## Project structure

```
/
├── index.html              Home
├── producto.html           Product
├── cuidado-diario.html     Daily care
├── ingredientes.html       Ingredients
├── faq.html                FAQ
├── privacidad.html         Privacy Policy
├── cookies.html            Cookie Policy
├── terminos.html           Terms & Conditions
├── css/                    base.css, components.css, sections.css
├── js/                     ui.js, cart.js, main.js
├── images/                 product photography + illustrations
├── robots.txt, sitemap.xml, .htaccess
├── README.md, CHANGELOG.md, DELIVERY.md
```

## Deployment

1. Upload all files (optionally without `README.md`, `CHANGELOG.md`, `DELIVERY.md`) to the document root of the server/domain provided by the client.
2. `index.html` must be served as the default document.
3. In `js/main.js`, set `LEAD_ENDPOINT` to the lead-submission URL to activate order submissions.
4. If the production domain differs from `lumera.com.gt`, replace it in canonical URLs, Open Graph tags, `sitemap.xml` and `robots.txt`.
5. Apache: keep `.htaccess` for clean URLs. Nginx or static hosts: ignore it or add `try_files $uri $uri.html =404;`.

The site also runs locally by opening `index.html`.

## Placeholders to confirm before publication

| Item | Current value | Where |
|---|---|---|
| Operating company | Lumera Guatemala, S.A. | footer, legal pages |
| NIT | 1234567-8 | `privacidad.html`, `terminos.html` |
| Address | 12 Calle 1-25, Zona 10, Ciudad de Guatemala | footer, legal pages |
| E-mail | info@lumera.com.gt | footer, legal pages, FAQ |
| Phone | +502 2385 4420 | footer, legal pages, FAQ |
| Domain | lumera.com.gt | canonicals, OG, `sitemap.xml`, `robots.txt` |
| Delivery terms | 1–3 business days capital, 2–5 departments; cash on delivery; returns 7 days unopened | `producto.html`, `faq.html`, `terminos.html` |
| Social-proof claim | "Más de 2.500 personas ya lo usan" (from the client's landing page) | `index.html` |
| Sanitary registration no. | not shown (stated as "figura en el envase") | `terminos.html` |

---

Prepared for ACURELLA LIMITED · Developer: Oleh Vozniak
