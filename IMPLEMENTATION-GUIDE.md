# Downtown Coffee — Implementation Guide

## Current Status (2026-03-29)
- Manager gave buy-in to proceed
- Ben set up a Squarespace trial account using the **Eldridge** template
- Header code injection (SEO/meta/JSON-LD) is **pasted and live** on the test site
- Logo uploaded, nav pages created (Home, Our Story, Shop Coffee, Visit, Contact)
- Editing the content/layout is in progress — early stages, needs work
- Design reference: Kai Coffee Hawaii (kaicoffeehawaii.com) — clean, warm, minimal Shopify site. Closest to the vibe we want.
- Approach: **lean on Eldridge's default styling**, minimize custom CSS. Manager wants as little custom code as possible.

**Test site:** celery-burgundy-a26x.squarespace.com

---

## Workflow

1. Build out content and layout on Ben's test Squarespace account
2. Keep custom CSS minimal — use Squarespace's built-in style controls where possible
3. Claude Code produces paste-ready files for code injection and any CSS overrides needed
4. Manager reviews the test site
5. Replicate to the live dtcoffee.com account with manager approval

---

## What's Done

- [x] Squarespace trial account created (Eldridge template)
- [x] Header code injection pasted (Open Graph, Twitter cards, JSON-LD, Google Fonts)
- [x] DT Coffee logo uploaded to nav
- [x] Nav pages created: Home, Our Story, Shop Coffee, Visit, Contact
- [x] Instagram icon in nav

---

## Action Items — Content & Layout

### Hero Section
- [ ] Replace Eldridge placeholder image with DT Coffee storefront/counter photo
- [ ] Add text overlay: "Roasted with Aloha" headline
- [ ] Add subtext: "100% Hawaii-grown coffee, roasted fresh every Saturday morning at 900 Fort Street Mall."
- [ ] Add CTA buttons: "Shop Coffee" + "Our Story"
- [ ] Talk to manager about getting a video (like Local Joe's site) — future enhancement

### Our Story Section
- [ ] Fix layout — text is overlapping the team photo right now
- [ ] Use a two-column layout: photo on left, text on right (or stacked)
- [ ] Replace placeholder copy with real DT Coffee about text
- [ ] Add team photo as a standalone image, not a background

### Coffee Menu / Shop Section
- [ ] Replace Eldridge's placeholder menu with DT Coffee's actual offerings
- [ ] Decide: use Eldridge's menu-style list (like the screenshot) OR product cards (like our mock)
- [ ] Replace stock coffee photo with DT Coffee product shots
- [ ] Get real prices from the live site or manager
- [ ] Product descriptions — placeholder for now, manager to provide

### Quote/Testimonial Section
- [ ] Replace "The Star-Review" placeholder quote with a real review or remove it
- [ ] Check if DT Coffee has any press quotes or notable Google reviews to feature

### Newsletter / Mailing List Section
- [ ] Decide if manager wants this — good feature but needs an email service (Mailchimp, etc.)
- [ ] If keeping, update copy for DT Coffee branding
- [ ] If not keeping, remove the section

### Visit / Contact Section
- [ ] Add address: 900 Fort Street Mall, Suite 100, Honolulu, HI 96813
- [ ] Add "Get Directions" button linking to Google Maps
- [ ] Add business hours (need from manager)
- [ ] Add contact form or link to contact page

### Footer
- [ ] Instagram link
- [ ] Shop link
- [ ] Shipping info link
- [ ] Copyright: © 2025 Downtown Coffee Honolulu

### Nav Cleanup
- [ ] Change the "Contact" button (top right) to "Order Now" → links to Shop page
- [ ] Remove duplicate Contact in nav if it's showing twice

---

## Action Items — Images to Upload

All images are from DT Coffee's existing Squarespace CDN. Open each URL in browser, right-click > Save Image As, then upload to your test site.

**Storefront/counter (hero):**
```
https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1588702335800-WK83V8K80SAJXR7GU6UW/EC677D9A-0821-4631-AA4A-C34965C506E4.jpeg
```

**Team photo (about section):**
```
https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1588702332363-6L2OKRMLTSVGP5T5V6M1/FEF48159-A3BB-43A3-9770-4BA3BD8D4FDE.jpeg
```

**Product photos:**
- Downtown Blend: `https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1471291200651-NCRDORHD1TJK5SRHIF34/IMG_2090.jpg`
- Mokka: `https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1412195453847-N1QANNYJ8GVYV37TD78V/IMG_6323.JPG`
- Kona: `https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1497726503262-AX8JY7OTU3VS8P52AWM4/IMG_7762.jpg`
- Ka'u: `https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1497726227810-W6XQ2170WUEG86BIJWHS/IMG_7758.jpg`

---

## Action Items — SEO (done or ready)

- [x] Header injection pasted (OG, Twitter, JSON-LD, fonts)
- [ ] Set site title in Squarespace SEO settings: `Downtown Coffee Honolulu | Hawaii Coffee Roaster & Coffeehouse`
- [ ] Set site description: `Independent coffee roaster and coffeehouse in downtown Honolulu, Hawaiʻi. 100% Hawaii-grown coffee, roasted fresh every Saturday. Visit us at 900 Fort Street Mall.`
- [ ] Add alt text to every image uploaded
- [ ] Change `/new-page-1` slug to `/contact` (on the live site, when migrating)

---

## Still Needs Manager Input

- [ ] **Business hours** — for JSON-LD and Visit section
- [ ] **Product descriptions / tasting notes** — placeholder copy for now
- [ ] **Video of the shop** — would elevate the hero section significantly (like Local Joe's site)
- [ ] **Confirm `/new-page-1` → `/contact` slug change** on live site
- [ ] **Google Business Profile** — does one exist? If not, set one up (free, ~15 min, huge for SEO + AI)
- [ ] **Press quotes or reviews** — anything to put in the testimonial section?
- [ ] **Mailing list** — does he want a newsletter signup? Needs an email service.
- [ ] **Budget** — Squarespace Business plan ($23/mo) needed for code injection on the live site

---

## Design References

- **Our mock:** `dtcoffee-refresh-mock.html` (GitHub Pages: benjaminboughton.github.io/dt-coffee/dtcoffee-refresh-mock.html)
- **Kai Coffee Hawaii:** kaicoffeehawaii.com — the target vibe. Clean, warm, minimal, good product showcase.
- **Local Joe:** localjoehi.com — video hero inspiration, practical local-business features
- **The Curb Kaimuki:** thecurbkaimuki.com — dark/moody upscale alternative, multilingual nav is smart for Hawaii

---

## How to Pick Up Next Session

Feed Claude Code both files:
- `dtcoffee-claude-briefing.md` — full project context
- `dtcoffee-refresh-mock.html` — visual spec and SEO reference

Then say what you want to work on — content editing, CSS tweaks, or next steps.
