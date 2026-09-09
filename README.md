# prrealestatehyd.com

Website for **PR Real Estate** — land and open plot brokers in Moinabad mandal,
Ranga Reddy district, Telangana. Working since 2015.

Live at **https://prrealestatehyd.com**

---

## What this is

A single static HTML page. No framework, no build step, no dependencies.
Open `index.html` in any browser and it works.

| File | Purpose |
|---|---|
| `index.html` | The whole site — markup, CSS, JS and both portraits |
| `img/og-cover.jpg` | Link preview card for WhatsApp, Facebook, X |
| `CNAME` | Custom domain for GitHub Pages |
| `robots.txt` | Search engine directives |
| `sitemap.xml` | Submitted to Google Search Console |
| `.nojekyll` | Stops GitHub Pages running Jekyll on the files |

Both partner portraits and the favicon are embedded as data URIs inside
`index.html`, so the file is self-contained.

---

## Deploying

**GitHub Pages**

1. Settings → Pages → Source: *Deploy from a branch* → `main` / `root`
2. Custom domain: `prrealestatehyd.com` (the `CNAME` file sets this)
3. Tick **Enforce HTTPS**
4. At the domain registrar, point DNS at GitHub Pages:
   - `A` records for the apex domain → `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `<owner>.github.io`

Confirm the current IPs against GitHub's own Pages documentation before
setting them — they change occasionally.

Changes pushed to `main` go live in about a minute.

---

## Still to add

Five photo slots are wired up but empty. Drop the files into `img/` with
these exact names and they appear automatically — no code change needed.
Until then those sections hide themselves rather than showing broken images.

| File | Size | Subject |
|---|---|---|
| `img/land-wide.webp` | 2000 × 1100 | Wide open land, boundary markers or approach road |
| `img/site-visit.webp` | 2000 × 1100 | Layout board with LP number readable, or a site visit |
| `img/land-1.webp` | 900 × 1200 | Boundary stones |
| `img/land-2.webp` | 900 × 1200 | Approach road into a layout |
| `img/land-3.webp` | 900 × 1200 | Farm or agricultural parcel |

Shoot landscape for the two wide files, portrait for the three verticals.
Convert to WebP before committing — raw phone photos are 20× the size for no
visible gain.

Also outstanding: the Google Maps link in the contact section, currently a
placeholder. It comes from the Google Business Profile.

---

## Maintenance

**Review quarterly.** The page states regulatory positions that change:

- **GO 111** — catchment restrictions, actively litigated. The page carries a
  visible "current as of" date. Update the text and the date together.
- **Bhu Bharati** — replaced Dharani in April 2025.
- **Rates** — the price table is dated. Refresh it or remove it; a stale
  price table is worse than none.

**Prices are indicative ranges only.** They carry a variability note on the
page. Keep it there.

**Nothing on the site is legal advice.** The footer says so. Don't remove it.

---

## Accessibility and performance

Built to WCAG 2.1 AA criteria — semantic landmarks, one `h1`, logical heading
order, visible focus styles, `prefers-reduced-motion` respected, alt text on
every image. Verify contrast and run a keyboard-only pass before any redesign.

Performance targets: LCP under 2.5s, CLS under 0.1, INP under 200ms. These
assume a CDN in front of the origin and compressed images. Check with
Lighthouse on mobile after deploying, not before.

---

© PR Real Estate, Aziz Nagar, Moinabad, Ranga Reddy District, Telangana.
All rights reserved. Not licensed for reuse.
