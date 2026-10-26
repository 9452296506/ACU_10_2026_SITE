# Delivery Note — LUMERA Multi-Page Website

**Client:** ACURELLA LIMITED (Reg. no. CY10378872I)
**Project:** Multi-page website for the Lumera facial serum (Guatemalan market, Spanish), under the existing agreement
**Delivery date:** 26 October 2026

## Scope (as agreed)

Multi-page website in Spanish, 5 main pages with navigation **Inicio | Producto | Cuidado diario | Ingredientes | FAQ**:

- **Home** — presentation, key product information, benefits, target audience, key ingredients, usage, reviews, order section
- **Product** — description, product images and packaging details, benefits, ingredients, usage instructions, price, reviews, delivery/payment information, order section
- **Usage / Daily care** — dose, morning & evening routines, application technique, use with other cosmetics, storage, 4-week programme
- **Ingredients** — the five actives with cosmetic purpose and benefits
- **FAQ** — use, frequency, results, compatibility, ordering, payment, delivery, returns; order section

Also: Order button in the header and conversion sections; Privacy Policy / Cookie Policy / Terms pages linked in the footer; order form with Name and Phone number; price Q229 throughout.

## Timeline

| Milestone | Date |
|---|---|
| Order agreed | 6 October 2026 (18:00) |
| Development (14 working days × 8 h) | 7 – 26 October 2026 |
| Delivery & invoice | 26 October 2026 |

Daily log: `CHANGELOG.md`.

## Technical requirements — status

| Requirement | Status |
|---|---|
| UX/UI design for the complete website | ✅ Design system + per-page layouts (`README.md`) |
| Front-end: HTML5, CSS, JavaScript and jQuery | ✅ jQuery 3.7 (`js/ui.js`, `js/cart.js`, `js/main.js`) |
| PHP / back-end functionality where necessary | ✅ Not required for the agreed scope: the site is static; order forms POST JSON directly to the client's lead-submission endpoint (`LEAD_ENDPOINT` in `js/main.js`) |
| Fully responsive (desktop, tablet, mobile) | ✅ Breakpoints 1200 / 900 / 620 / 400 px |
| Working navigation, buttons, FAQ sections and cookie notice | ✅ |
| Product images and packaging details | ✅ Client photography: 6-image gallery, packaging section, contextual photos |
| Order/request forms with "Name" and "Phone number" | ✅ Home, Product, FAQ, checkout modal |
| Form validation and connection to the lead submission method | ✅ Client-side validation; integration point ready (`LEAD_ENDPOINT` in `js/main.js`); set the client's URL to activate |
| Basic SEO structure (titles, meta descriptions, headings, clean URLs) | ✅ JSON-LD `Product` and `FAQPage`, sitemap, robots, `.htaccess` for extensionless URLs |
| Privacy Policy, Cookie Policy and Terms links in the footer | ✅ Dedicated Spanish pages |
| Deployment to the server/domain provided by the client | ✅ Instructions in `README.md`; performed on access to the client's server/domain |

## Delivered components

- `index.html`, `producto.html`, `cuidado-diario.html`, `ingredientes.html`, `faq.html`
- `privacidad.html`, `cookies.html`, `terminos.html`
- `css/` — `base.css`, `components.css`, `sections.css`
- `js/` — `ui.js`, `cart.js`, `main.js`
- `images/` — product photography (web-optimised) and illustrations
- `robots.txt`, `sitemap.xml`, `.htaccess`
- `README.md`, `CHANGELOG.md`, `DELIVERY.md`

## Handover package

| Deliverable | Notes |
|---|---|
| Full source code | `github.com/9452296506/ACU_10_2026_SITE_CODE` |
| Delivery documentation (`README.md`, `CHANGELOG.md`, `DELIVERY.md`) | `github.com/9452296506/ACU_10_2026_SITE` |
| GitHub repository access | Granted to the client for both repositories |
| Downloadable archive of all website files | Provided with this delivery |
| Desktop & mobile screenshots | Provided with this delivery |
| Upload instructions | `README.md`, "Deployment" |

## Connecting the lead form

All order forms post `{ name, phone, product, qty, price, source, page }` as JSON to the URL configured in `LEAD_ENDPOINT` (`js/main.js`). Provide the endpoint of your lead-submission method and set this value; until then the forms validate and confirm without sending.

## Before go-live

- Confirm the placeholders listed in `README.md` ("Placeholders to confirm"): company name, NIT, address, e-mail, phone, domain, delivery/payment wording, social-proof claim.
- If the production domain differs from `lumera.com.gt`, replace it in canonicals, Open Graph tags, `sitemap.xml`, `robots.txt`.
- Product claims, labelling and sanitary registration remain the client's responsibility.

## Service summary (for records)

| | |
|---|---|
| **Service (as invoiced)** | Website development / Tworzenie stron internetowych — design and front-end development of a multi-page marketing website (UX/UI design, HTML5/CSS/JavaScript + jQuery programming, SEO structure, content and image integration, testing, documentation, handover package) |
| **Repository (invoice reference)** | `github.com/9452296506/ACU_10_2026_SITE` — delivery documentation; `github.com/9452296506/ACU_10_2026_SITE_CODE` — source code |
| **Ordered by** | ACURELLA LIMITED, 27, 25 Martiou Str., D. MICHAEL TOWER, Office 105A, Engomi, 2408 Nicosia, Cyprus · NIP/VAT: CY10378872I (business customer, EU) |
| **Basis** | Order of 6 October 2026 under the existing framework agreement |
| **Period of performance** | 7 – 26 October 2026 (14 working days × 8 h = 112 h; daily log in `CHANGELOG.md`) |
| **Place of performance** | Performed remotely from Poland; results delivered electronically |
| **Classification** | Software-related services — programming of the website front end (PKWiU 62.01.11.0); registered lump-sum taxation (ryczałt), 12% rate |
| **Deliverables** | Full source code, documentation, downloadable archive, screenshots, repository access |
| **Settlement** | Invoiced on delivery (26 October 2026); bank transfer per the invoice terms; intra-EU B2B service — VAT reverse charge (np./na.), place of supply per Art. 28b |

## Acceptance

The project is **delivered and ready for review** as of **26 October 2026**. The client was provided with the handover package listed above. Deployment to the client's server/domain is performed once access is provided. Further changes are handled as a separate engagement.

---

Prepared for ACURELLA LIMITED · Developer: Oleh Vozniak · 26 October 2026
