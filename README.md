# Filmorax — filmorax.com (static landing site)

The cinematic & advertising production arm of **influUGC**. Designated as the
network's production brand site by owner decision, Nov 6, 2026. **Files only —
not deployed.**

## Identity (owner rule for ALL network satellites, Nov 5, 2026)

Every network site uses the **main influUGC identity** — no distinct designs:

- Black background `#000`, neon lime accent `#C8FF00`, dark panels, bold heavy
  typography — the www.influugc.com feel (same design system as the
  prinfluencer.net satellite; `styles.css` is adapted from it).
- Brand lockup: `Filmorax.` wordmark with the subline "The cinematic &
  advertising production arm of influUGC" (Arabic: «ذراع الإنتاج السينمائي
  والإعلاني من influUGC»).
- Only real company data: est. 2020, Arab League St Agouza (Giza 12651),
  Egypt + Saudi/Gulf, real client names (Riyadh Season, Saudi Tourism
  Authority, flynas, Saudia, realme, Domino's, TikTok Live, Zanussi) and the
  documented works (realme 2024 promo, Domino's 2024 commercial, flynas 2023
  corporate video). No prices, no invented figures, no testimonials, no stock
  imagery (CSS/text only).

## Pages built (3 HTML pages, 2 languages)

| File | What |
|---|---|
| `index.html` | Arabic-first landing (RTL): hero, client proof strip, **guides section (3 guides, see retrofit note below)**, 6 production services (commercial production, brand films, cinematic social content, product videos, event coverage, post-production), selected works (realme 2024 promo, Domino's 2024 commercial, flynas 2023 corporate video), why influUGC (with the in-body editorial link to influugc.com), 4-step production process (pre-production → shoot → post → delivery), 6-question answer-first FAQ, contact/CTA band, network footer. |
| `en.html` | Full English mirror (LTR), same structure, guides, works and FAQ. |
| `404.html` | Branded not-found page (Arabic). |

Plus: `styles.css`, `favicon.svg` (black screen-frame + lime play mark),
`sitemap.xml` (hreflang-annotated), `robots.txt`, `llms.txt`.

## Content retrofit (Nov 6, 2026 — content-first model)

Retrofitted to the owner's Nov 6 content-first model (sites lead with useful
content for search engines and AI answers, with influUGC's services and real
work woven in), following the aistore guides pattern: a **Guides** section now
opens the page flow (after the proof strip, before Services), with three
substantive, answer-first guides as anchor-linked on-page blocks, in both
languages:

1. `#guide-brief` — how to write a production brief for a commercial.
2. `#guide-shoot` — what a one-day shoot actually involves (schedule, crew, deliverables).
3. `#guide-rights` — video usage rights for ads, explained.

Each guide closes with a woven-in Filmorax/influUGC line + the standard
central CTAs (booking + WhatsApp, `utm_source=filmorax`). No invented
statistics. Section numbering shifted (Guides 01 → Services 02 → Works 03 →
Why 04 → Process 05 → FAQ 06); header nav and footer nav link the guides;
`llms.txt` carries guide summaries with UTM CTAs. Guide blocks are on-page
anchors, so `sitemap.xml` is unchanged.

## SEO / GEO

- Canonical base `https://filmorax.com/` (the real domain — if this site is
  first deployed to an `onrender.com` URL before the domain attaches, switch
  all canonical/OG/sitemap/robots/llms bases in one pass, same as the
  ugccompany rule in `../DEPLOY.md` §2).
- Title/meta target "Production / إنتاج سينمائي وإعلاني" + Egypt / Saudi
  Arabia in both languages; OpenGraph + Twitter cards; hreflang ar/en both
  ways.
- JSON-LD: `Organization` (with `parentOrganization: influUGC`, postal
  address, areaServed, the four real social profiles), `WebSite`, and
  `FAQPage` matching each page's visible FAQ.

## CTAs (all central, all carry the satellite UTM set)

- Booking → `https://www.influugc.com/book?utm_source=filmorax&utm_medium=satellite&utm_campaign=network`
- WhatsApp (client line) → `https://wa.me/201029979797?utm_source=filmorax&utm_medium=satellite&utm_campaign=network`
- Footer legal line: "Part of the influUGC network" linking to the hub.

## What remains (not done here)

1. **Deploy** — static folder; any static host or a Render Static Site (free
   tier per the network rule). No server/admin in this build: a static
   landing, like prinfluencer.
2. **Domain attach** — point `filmorax.com` DNS at the host (same checklist
   pattern as `../DEPLOY.md` §4: apex A + www CNAME from the host's screen;
   no MX changes — mail stays on influugc.com). Note: filmorax.com currently
   sits in the new company Namecheap account (`influugc`) with a $200 sale
   designation — the listing must be pulled when the domain is attached.
3. **prodactionpr.com 301 → filmorax.com** — prodactionpr.com is the second
   production domain (owner: use both — filmorax as the production site,
   prodactionpr as its 301 shield). This supersedes the earlier plan of
   redirecting prodactionpr.com to the production page on influugc.com.
4. After go-live: dedicated Google Search Console property + submit
   `sitemap.xml`; verify both pages return 200 and the FAQ renders.

## Deploy status (Nov 6, 2026)

- **Repo**: https://github.com/mostafaabaas/filmorax (private, branch `main`) — source pushed Nov 6, 2026.
- **Hosting**: PENDING-DASHBOARD — the Render Static Site service has **not** been created yet.
  Creating it requires the Render dashboard (no Render API key is available to the
  automation): Render Dashboard → New → Static Site → connect this repo — the repo's
  `render.yaml` blueprint pre-fills the service name (`filmorax`) and publish path (`.`).
  Expected live URL once created: https://filmorax.onrender.com
- **Domain attach**: separate later batch (see "What remains" item 2 above).
