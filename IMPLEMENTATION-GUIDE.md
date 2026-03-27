# Downtown Coffee — Implementation Guide

How to apply the mock to the live Squarespace site. Three buckets: copy/paste injection, Squarespace editor work, and SEO settings.

---

## 1. COPY/PASTE: Header Code Injection
**Where:** Settings > Advanced > Code Injection > **Header**

Paste this entire block:

```html
<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />

<!-- Open Graph (link previews in iMessage, Slack, social, etc.) -->
<meta property="og:type" content="website" />
<meta property="og:url" content="https://www.dtcoffee.com/" />
<meta property="og:title" content="Downtown Coffee Honolulu | Hawaii Coffee Roaster" />
<meta property="og:description" content="100% Hawaii-grown coffee, roasted fresh every Saturday in downtown Honolulu. Shop single-origin Kona, Kaʻu, Maui Mokka, and more." />
<meta property="og:image" content="https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1588702335800-WK83V8K80SAJXR7GU6UW/EC677D9A-0821-4631-AA4A-C34965C506E4.jpeg" />
<meta property="og:locale" content="en_US" />
<meta property="og:site_name" content="Downtown Coffee Honolulu" />

<!-- Twitter card -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="Downtown Coffee Honolulu | Hawaii Coffee Roaster" />
<meta name="twitter:description" content="100% Hawaii-grown coffee, roasted fresh every Saturday in downtown Honolulu." />
<meta name="twitter:image" content="https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1588702335800-WK83V8K80SAJXR7GU6UW/EC677D9A-0821-4631-AA4A-C34965C506E4.jpeg" />

<!-- JSON-LD: Local Business structured data (Google reads this) -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CoffeeShop",
  "name": "Downtown Coffee Honolulu",
  "url": "https://www.dtcoffee.com",
  "logo": "https://www.dtcoffee.com/favicon.ico",
  "image": "https://images.squarespace-cdn.com/content/v1/540e2c3be4b0e71908ad1732/1588702335800-WK83V8K80SAJXR7GU6UW/EC677D9A-0821-4631-AA4A-C34965C506E4.jpeg",
  "description": "Independent coffee roaster and coffeehouse in downtown Honolulu specializing in 100% Hawaii-grown coffee since 2011.",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "900 Fort Street Mall, Suite 100",
    "addressLocality": "Honolulu",
    "addressRegion": "HI",
    "postalCode": "96813",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 21.3089,
    "longitude": -157.8589
  },
  "sameAs": [
    "https://www.instagram.com/dtcoffeehonolulu"
  ],
  "servesCuisine": ["Coffee", "Espresso", "Matcha"],
  "priceRange": "$",
  "foundingDate": "2011",
  "hasMap": "https://maps.google.com/?q=900+Fort+Street+Mall+Honolulu+HI"
}
</script>
```

---

## 2. COPY/PASTE: Custom CSS
**Where:** Design > Custom CSS

```css
/* ── DT COFFEE REFRESH ── */

:root {
  --cream:    #f7f3ec;
  --warm:     #ede6d6;
  --espresso: #2b1d0e;
  --roast:    #6b3f1e;
  --gold:     #b5813a;
  --muted:    #8a7460;
  --white:    #fdfaf5;
}

/* Base typography */
body {
  font-family: 'DM Sans', sans-serif !important;
  background: var(--cream);
  color: var(--espresso);
}

h1, h2, h3 {
  font-family: 'Cormorant Garamond', serif !important;
  font-weight: 300;
}

/* NOTE: The CSS below will need to be adapted to Squarespace's       */
/* actual class names once we're in the editor. Squarespace templates  */
/* use their own generated class names (e.g. .header-nav-item,        */
/* .sqs-block-content, etc.) which vary by template version.          */
/* The mock CSS gives us the exact values — we just need to map them  */
/* to the right Squarespace selectors.                                 */
```

> **Important:** The full CSS from the mock won't paste 1:1 into Squarespace because Squarespace has its own class names. Once we're in the editor, we'll inspect the live site's DOM, find the right selectors, and adapt. The mock gives us the exact design values (colors, sizes, spacing) — we just retarget them.

---

## 3. SQUARESPACE EDITOR (manual, point-and-click)

### Navigation
- [ ] Rename "Welcome" → "Home"
- [ ] Merge "Shop Coffee" + "Shop mugs, shirts, books" into single "Shop"
- [ ] Add "Order Now" as a button-style nav link
- [ ] Move Instagram link out of nav (it stays in footer)

### Page Settings
- [ ] Change `/new-page-1` slug → `/contact`

### SEO Settings
- [ ] Settings > SEO > Site Title: `Downtown Coffee Honolulu | Hawaii Coffee Roaster & Coffeehouse`
- [ ] Settings > SEO > Site Description: `Independent coffee roaster and coffeehouse in downtown Honolulu, Hawaiʻi. 100% Hawaii-grown coffee, roasted fresh every Saturday. Visit us at 900 Fort Street Mall.`

### Content (via block editor)
- [ ] Hero section: update heading, subtext, and CTA buttons to match mock
- [ ] About section: update copy and add stats grid
- [ ] Product cards: add tasting note descriptions (owner to provide)
- [ ] Visit section: update layout and copy
- [ ] Footer: update layout, add social links

---

## 4. STILL NEEDS MANAGER INPUT
- [ ] Actual business hours (for JSON-LD `openingHours` and Visit section)
- [ ] Product descriptions / tasting notes
- [ ] Confirm `/new-page-1` → `/contact` slug change is OK
- [ ] Whether they have a Google Business Profile (huge for local SEO, separate from site)
