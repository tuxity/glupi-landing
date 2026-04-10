# GLuPI Landing Page

## Brand
- The brand name is **GLuPI** — not Glupi, GLUPI, or glupi. Never normalize the casing. This caused a critical revert across all pages.
- Canonical URL: https://glupi.com.mx/

## Stack
- Static HTML + vanilla CSS (no JavaScript framework)
- Cloudflare Pages via Wrangler
- Spanish language (es-MX) — all content is in Spanish for Mexico market

## Structure
- `index.html` — main landing page (hero, how-it-works, phases, pricing, CTA)
- `blog/` — SEO blog posts about GLP-1 topics
- `aviso-de-privacidad.html` — privacy policy (Mexican LFPDPPP compliance)
- `terminos-y-condiciones.html` — terms and conditions
- `styles.css` — single stylesheet
- `wrangler.jsonc` — Cloudflare Pages config

## Critical Rules

### Brand name is GLuPI, always
Multiple tickets were caused by agents "fixing" the brand to standard casing. The mixed case is intentional. Search for "Glupi" (wrong) before any PR.

### Legal pages must reflect actual data practices
The privacy notice must match what the backend chatbot actually collects. GLuPI collects sensitive health data (weight, symptoms, medication). Jurisdiction is Guadalajara, Jalisco.

### Pricing must match backend
Landing page shows 3 plans (Arranque, Mantenimiento, Premium). Prices must match what MercadoPago actually charges. Never show test prices on the landing page.

### SEO metadata
All pages have Open Graph, Twitter cards, and JSON-LD structured data. Keep these up to date when content changes.

### No JavaScript framework
This is intentionally a static site. Do not introduce React, Vue, or build tools. Keep it simple HTML+CSS.
