# Downtown Coffee — Claude Code Briefing

## What This Project Is
We're proposing iterative improvements to **dtcoffee.com**, a Squarespace site for Downtown Coffee Honolulu — a small, locally-owned Hawaii coffee roaster and coffeehouse. The owner/manager is low-key and prefers **gentle, iterative tweaks** over an overhaul. Nothing goes live without explicit manager approval.

## The File
`dtcoffee-refresh-mock.html` is a **standalone HTML mock** of the refreshed site. It uses:
- Real copy and CDN images pulled from the live site
- Proposed design improvements (see below)
- Baked-in SEO (meta tags, Open Graph, JSON-LD)

It is **not connected to Squarespace** — it's a visual proposal only. Changes here are zero-risk.

## Design Decisions Already Made
- **Fonts:** Cormorant Garamond (headings, serif, elegant) + DM Sans (body, clean)
- **Palette:** Cream `#f7f3ec` · Espresso `#2b1d0e` · Gold `#b5813a` · Muted `#8a7460`
- **Tone:** Warm, organic, refined — fits a local Hawaii roaster. NOT flashy.
- **Principle:** Less is more. Tweaks, not overhaul.

## Nav Changes (vs. live site)
| Before | After |
|---|---|
| "Welcome" | "Home" |
| "Shop Coffee" + "Shop mugs, shirts, books" (two links) | Single "Shop" + "Order Now" CTA button |
| Instagram in nav | Instagram moved to footer |
| `/new-page-1` slug for Contact | Fixed to `/contact` |

## Sections in the Mock
1. **Fixed nav** — cleaned up links, CTA button
2. **Hero** — full-bleed photo, tagline, two CTAs ("Shop Coffee" / "Our Story")
3. **Info strip** — quick facts bar (free pickup, Hawaii-grown, Saturday roast)
4. **About** — two-col layout, existing copy, stats grid
5. **Shop** — 4 product cards with roast tags + tasting note descriptions (placeholder copy — needs real input from manager)
6. **Visit / Contact** — split layout, address, directions CTA
7. **Footer** — logo, copyright, social links

## SEO Already Baked In
- `<title>` — keyword-rich, includes "Hawaii Coffee Roaster & Coffeehouse"
- `<meta name="description">` — search result blurb
- Open Graph tags — controls link previews in iMessage, Slack, etc.
- Twitter card tags
- **JSON-LD local business schema** (`@type: CoffeeShop`) — tells Google the address, coordinates, founding date, cuisine served. This is the big one for local search.
- Descriptive `alt` text on all product images

## What Still Needs Real Input (from manager)
- [ ] Actual business hours (for JSON-LD and Visit section)
- [ ] Tasting notes / product descriptions (placeholder copy in cards right now)
- [ ] Confirmation that `/new-page-1` → `/contact` slug change is OK
- [ ] Any preferred brand colors or existing style guide
- [ ] Whether they have a Google Business Profile (separate from site, huge for local SEO)

## How to Apply Changes to the Real Site (when approved)
Squarespace does **not** have a CLI or API for content. Workflow is:
1. Draft CSS/copy changes here in Claude Code
2. Paste CSS into Squarespace → Design → Custom CSS
3. Paste meta/JSON-LD into Squarespace → Settings → Advanced → Code Injection (header)
4. Update page slugs in Page Settings individually
5. **No staging environment in Squarespace** — use Preview mode carefully before publishing

## Live Site Reference
- Homepage: https://www.dtcoffee.com/
- Shop: https://www.dtcoffee.com/shop
- About: https://www.dtcoffee.com/about-us
- Location: https://www.dtcoffee.com/locations
- Squarespace CDN base: `https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/`
