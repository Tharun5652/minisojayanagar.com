# MINISO Jayanagar — Premium Flagship Website

Static, production-ready website for **MINISO Jayanagar** (Bengaluru).
Built for tomorrow's project evaluation.

## What's inside

| File | Purpose |
|---|---|
| `index.html` | Complete single-file app (HTML + CSS + JS). No build step, no dependencies. |
| `products.json` | 2,974-product catalogue (SKU, barcode, name, category, sub-category, price, image). |
| `store_entrance.jpg.jpeg` | Hero background — the store entrance photo. |

## Run it

Any static host works — GitHub Pages, Netlify, Vercel, S3, or plain nginx.
For a quick local preview:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Premium features (all implemented)

### ⭐ WhatsApp Product Enquiry (highlight)
Every product card + product page has a **"Check Availability"** / **"Enquire on WhatsApp"** button
that opens WhatsApp with a pre-filled message containing product name, price and SKU:

> Hi MINISO Jayanagar, I'm interested in this product.
> Product Name: {name}
> Price: ₹{price}
> SKU: {sku}
> Is this product currently available in your store? …

### 🛍 Shopping experience
- **Dedicated product detail pages** (`#p/<SKU>` route, deep-linkable, browser-back friendly) with:
  - Multi-image gallery (main + auto-derived alternate angles from `-1/-2/-3` MINISO CDN pattern)
  - Category, sub-category, SKU, barcode
  - Deterministic star rating stable per product (4.2 – 4.99)
  - In-store availability pill tied to live store hours
  - "Enquire on WhatsApp" · Wishlist · Share buttons
  - **You May Also Like** — similar products from the same sub-category
  - **Recently Viewed** carousel at the bottom
- **Live search suggestions** with product image, category, and price · keyboard shortcut `Cmd/Ctrl+K` · quick chips
- **Product badges** — 🆕 New Arrival · 🔥 Best Seller · ❤️ Trending · 🎁 Limited Edition
- **Wishlist** ❤️ with slide-in panel, persisted in `localStorage`, header badge counter
- **Recently Viewed** carousel on home + product page (persisted)
- **Share** — WhatsApp · Instagram (copy caption) · Facebook · Copy Link
- **Barcode Scan** helper button on the shop search bar

### 🎯 Discovery
- **Featured / Best Sellers / New Arrivals** horizontal scrollers
- **Category tiles** — 13 departments each with icon, brand colour, and product count
- **Sub-category chip filters**

### 🏬 Store information
- **Live status bar** — 🟢 Open Now / 🔴 Closed, computed from `10 AM – 10 PM`
- **Store block** — address, timings, phone, WhatsApp, real embedded Google Map + WhatsApp/Call/Directions CTAs
- **6 customer reviews** with avatars, star ratings, verified badges

### 📱 Floating actions (visible on every page)
- 🟢 WhatsApp (main, pulsing halo)
- ⚫ Call Store
- 🔵 Google Maps
- 🌈 Instagram
- ⬆️ Scroll-to-top (bottom-left)

### ✨ Premium UI/UX
- **Loader** with MINISO mark + animated progress bar
- **Glassmorphism sticky navbar** — blurs everything under it, elevates on scroll
- **Typography** — Cormorant Garamond (editorial display) + Outfit (body)
- **Hero** with cinematic slow zoom, staggered fade-up, animated title
- **Fade-in reveal on scroll** for every section (IntersectionObserver)
- **Card hover** — lift + shadow, image zoom, wishlist reveal
- **Image zoom lightbox** on the product page
- **Toasts** for wishlist/share confirmations
- **Fully responsive** (down to 400 px), respects `prefers-reduced-motion`
- **Editorial red / cream / ink palette** — keeps MINISO branding
- **`Esc` / `Cmd+K`** keyboard shortcuts

## Store details (used everywhere)

- 📍 4th Block, Jayanagar, Bengaluru, Karnataka 560011
- 📞 +91 72593 52730
- 📱 WhatsApp: same number
- 🕒 Mon – Sun · 10:00 AM – 10:00 PM
- 📸 Instagram: [@miniso__jayanagar](https://www.instagram.com/miniso__jayanagar)

---
Zero backend needed — everything works from a plain static file host. Fully offline-capable once loaded.
