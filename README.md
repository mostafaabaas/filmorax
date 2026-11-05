# Filmorax — filmorax.com (static landing site)

A cinematic & advertising production studio site, part of the **influUGC**
network. Designated as the network's production brand site by owner decision,
Nov 6, 2026.

## Identity (owner rule for ALL network satellites)

Every network site uses the **main influUGC identity**:

- Black background `#000`, neon lime accent `#C8FF00`, dark panels `#0A0A0A`,
  IBM Plex Sans Arabic (AR pages) / Sora + Inter (EN pages). Lime buttons
  always carry **black** text.
- Brand lockup: `Filmorax.` wordmark with the subline "Cinematic &
  commercial production" (Arabic: «إنتاج سينمائي وإعلاني»).
- Real company data only: team working since 2020, Arab League St, Agouza
  (Giza 12651), shooting in Egypt + Saudi Arabia + the Gulf. **No portfolio
  or works sections anywhere on the site** (owner order, Nov 6, 2026), no
  prices, no invented figures, no testimonials, no stock imagery
  (CSS/text only).

## Layout system (restructure, Nov 6, 2026)

The v1 design was rejected by the owner (loose big text, no defined frames,
no organized sections) and the site was fully restructured:

- Fixed 1200px container; **every content block sits inside a framed panel**
  (1px solid `#1E1E1E`, `#0A0A0A` background, 16px radius). No unframed text.
- Uniform section anatomy: lime eyebrow label + H2 (≤40px) + one short lead
  line (≤68ch); sections separated by hairlines; 8pt spacing scale; body
  16–17px; hero headline ≤56px.
- Hero = two framed columns: text panel (badge chip, H1, lead, dual CTA,
  fact chips) + a pure-CSS **call-sheet visual panel** (shoot-day rows,
  deliverables checklist, stat tiles). No images.
- Services = bordered card grid. Process = numbered steps 01–04 in framed
  cells. Guides = article cards (category chip + title + excerpt + key
  points). FAQ = framed rows. CTA = framed lime-glow panel.

## Pages built (3 HTML pages, 2 languages)

| File | What |
|---|---|
| `index.html` | Arabic-first landing (RTL): hero with call-sheet panel → 01 Production formats (6 cards: commercials, corporate & brand films, product videos, event coverage, cinematic social content, post-production) → 02 Process (brief & treatment → pre-production → shoot day → post & delivery) → 03 Production guides (3 cards: the production brief, one full shoot day, usage rights) → 04 FAQ (6 questions) → CTA panel → network footer. |
| `en.html` | Full English mirror (LTR), same composition. |
| `404.html` | Framed not-found panel (Arabic) with booking + WhatsApp CTAs. |

Plus: `styles.css`, `favicon.svg` (black screen-frame + lime play mark),
`sitemap.xml` (hreflang-annotated), `robots.txt`, `llms.txt`.

## SEO / GEO

- Canonical base `https://filmorax.com/`; OpenGraph + Twitter cards;
  hreflang ar/en both ways.
- JSON-LD: `Organization` (with `parentOrganization: influUGC`, postal
  address, areaServed, the four real social profiles), `WebSite`, and
  `FAQPage` matching each page's visible FAQ exactly.
- `llms.txt` carries the formats, the 4-stage process and guide summaries.

## CTAs (all central, all carry the satellite UTM set)

- Booking → `https://www.influugc.com/book?utm_source=filmorax&utm_medium=satellite&utm_campaign=network`
- WhatsApp (client line) → `https://wa.me/201029979797?utm_source=filmorax&utm_medium=satellite&utm_campaign=network`
- The only influUGC references on the site: the footer network line
  («جزء من شبكة influUGC» / "Part of the influUGC network") + these CTAs.

## What remains (not done here)

1. **Domain attach** — filmorax.com DNS records are recorded in
   `../DNS-BATCH.md`; they are set in the new-account (`influugc`) registrar
   session, after which Render verifies + issues the certificate.
2. **prodactionpr.com 301 → filmorax.com** — registrar redirect batch
   (production shield).
3. After go-live on the real domain: dedicated Google Search Console
   property + submit `sitemap.xml`.

## Deploy status (Nov 6, 2026)

- **Repo**: https://github.com/mostafaabaas/filmorax (public, branch `main`).
- **Hosting**: LIVE — Render Static Site (free tier), auto-deploys from
  `main`: https://filmorax.onrender.com (verified live).
- **Domain attach**: pending the DNS batch above.
