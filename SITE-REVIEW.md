# Downtown Coffee — Site Review & Proposed Improvements

A summary of what we'd like to improve on dtcoffee.com, and what we can offer.

---

## Part 1: Style & Functionality

### Navigation is cluttered
The current site has **8 items** in the top navigation: Welcome, About Us, Shop Coffee, Shop mugs/shirts/books, Shipping, Location, Contact Us, and Instagram. That's a lot for a visitor to parse. Best practice for a small business site is 4–5 focused links plus one clear call-to-action button.

**What we'd change:**
- Consolidate the two shop links into one "Shop" link
- Move Shipping and Instagram out of the main nav (Shipping becomes a footer link, Instagram goes in the footer social section)
- Rename "Welcome" to "Home"
- Add a prominent "Order Now" button in the nav so visitors always have a clear next step

### No clear call-to-action on the homepage
When someone lands on the site, there's no obvious "Shop Now" or "Order Coffee" button. The homepage is mostly text — no featured products, no visual product showcase, no quick path to buying. Visitors have to find the shop on their own.

**What we'd change:**
- Add a hero section with a strong headline and two clear buttons: "Shop Coffee" and "Our Story"
- Add an info strip highlighting key selling points (free local pickup, Hawaii-grown beans, roasted every Saturday)
- Feature 4 top products directly on the homepage with photos and descriptions

### Visual design feels dated
The current site uses a dark background with default Squarespace template fonts. There's no distinct brand typography, and the layout doesn't do justice to the quality of the product.

**What we'd change:**
- Introduce a warm, refined color palette: cream, espresso brown, and gold accents
- Use Cormorant Garamond (an elegant serif) for headings and DM Sans (clean, modern) for body text
- Create a more spacious, photo-forward layout that lets the coffee and the shop speak for themselves
- Add a polished Visit/Contact section with address, directions, and a clear layout

### Contact page has a broken URL
The Contact Us page currently lives at `/new-page-1` — this is a default Squarespace slug that was never updated. It looks unprofessional if anyone shares that link.

**What we'd change:**
- Rename the slug to `/contact`

---

## Part 2: Search & Discoverability (SEO)

SEO — search engine optimization — is how your site shows up when people Google things like "coffee shop Honolulu" or "Hawaii coffee roaster." Right now, the site is leaving a lot on the table. Here's what that means in plain terms:

### When someone shares your link, it looks bare
When you text a link or share it on social media, most apps show a preview — a title, a short description, and a photo. Right now, dtcoffee.com is **missing the tags that control this preview** on some platforms. That means shared links may show up with no image, a generic description, or just a raw URL.

**What we'd add:**
- Open Graph tags (controls how links look in iMessage, Facebook, Slack, etc.)
- Twitter/X card tags (same thing, for Twitter/X)
- A curated preview image, title, and description so every shared link looks intentional and professional

### Google doesn't know you're a coffee shop
Google uses hidden structured data on your site to understand what your business is, where it's located, what you serve, and when you're open. The current site has some of this, but it's incomplete.

**What we'd add:**
- A complete "CoffeeShop" data profile that tells Google: this is a coffee shop at 900 Fort Street Mall, Honolulu, they serve coffee/espresso/matcha, they've been open since 2011, and here's a link to the map. This helps with local search results, Google Maps, and the info panel that shows up when someone searches your name directly.

### Images are invisible to search engines
Almost none of the images on the current site have **alt text** — the short description that tells Google (and screen readers) what's in the photo. Without it, Google can't index your images, and they won't show up in image search results. This is also an accessibility issue for visually impaired visitors.

**What we'd add:**
- Descriptive alt text on every image across the site (product photos, interior shots, etc.)

### Each page should have its own search description
Right now, some pages are relying on a single site-wide description instead of their own. That means when your Shop page or About page shows up in Google results, the preview text may not be relevant to what's actually on that page.

**What we'd add:**
- A unique, keyword-rich title and description for each page so Google shows the right blurb in search results

### The site title has an emoji in it
The current site title includes a heart emoji. While that's charming, it can display inconsistently in Google search results — sometimes showing as a box or question mark depending on the device. Cleaner to keep the title text-only.

---

## Summary

| Area | Current State | After Improvements |
|------|--------------|-------------------|
| Navigation | 8 cluttered links, no CTA | 5 clean links + "Order Now" button |
| Homepage | Text-heavy, no products shown | Hero image, featured products, info strip |
| Typography | Default template fonts | Refined serif + sans-serif pairing |
| Link previews | Missing or incomplete | Professional previews on all platforms |
| Google local search | Partial business data | Complete coffee shop profile |
| Image SEO | No alt text on most images | Descriptive text on every image |
| Page descriptions | Generic/missing | Unique per page |
| Contact page URL | `/new-page-1` | `/contact` |

All proposed changes are **gentle, iterative improvements** — not a redesign. The goal is to make the existing site cleaner, more inviting, and easier for both customers and search engines to navigate.

---

## Will these changes make the site harder to manage?

No. The day-to-day stuff — swapping photos, changing prices, editing descriptions, adding or removing products — all happens through Squarespace's normal content editor, which is **completely separate** from our enhancements. Nothing about that workflow changes.

Our improvements live in two places that don't touch content management:

- **Custom CSS** (fonts, colors, spacing) — this is a styling layer on top of the site. Changing a product photo or editing a price doesn't interact with it at all.
- **Code Injection** (SEO tags, structured data, font imports) — this sits in the page header. It has nothing to do with product or content editing.

Think of it like painting the walls and putting up new signage in a store — you can still rearrange the shelves, swap out merchandise, and update the menu board without touching the paint or the signs.

**Two small things to be aware of:**
1. If we use CSS to hide or move a specific navigation link and the nav gets reorganized later, that one CSS rule might need a quick update.
2. On rare occasions, Squarespace updates their templates in ways that change the underlying code. If that happens, some styling tweaks may need minor adjustments. This is uncommon.
