# Framer Rebuild Recipe — Recreating the Prestige Landing Page
_How to rebuild every effect from your live HTML draft inside Framer. Keep the HTML page open beside you as your live reference._

---

## The smart workflow (do it in this order)
1. **Set your brand Styles first** — create Color Styles (Navy `#002F5F`, Gold `#C4A24C`, Cream `#F3ECDC`, Rust `#903E1F`, Sage `#A4C0AA`) and Text Styles (Fraunces for headings, Poppins for body). Everything you build after is automatically on-brand.
2. **Build the sections** top to bottom: Hero → Ribbon → Stats → Featured → Services → Gallery → Founder → Testimonials → How We Work → CTA → Footer.
3. **Then layer the Effects on** — this is where the "everything belongs" feeling comes from.
4. **Shortcut:** use **Framer AI (Wireframer)** to scaffold the layout ("luxury Dubai event planner landing page, hero + gallery + founder + testimonials"), then restyle with your brand kit and add effects.

---

## The effects you loved → how to do each in Framer

### ⭐ Native (built in — no code, no plugins)

**Fade + rise on scroll (the reveals)**
Select a section → **Effects** panel → add **Appear** → choose *Fade* + *Move Up*. Apply it to a stack of items and Framer staggers them automatically. This is the single most-used effect on the page.

**Ken Burns hero zoom (slow continuous zoom)**
Select the hero image → **Effects** → add a **Loop** effect → animate **Scale 1 → 1.1**, ease in-out, loop/alternate. Gives that cinematic drift.

**Scrolling gold ribbon (the services marquee)**
**Insert menu → Ticker.** Drop your text items in (Weddings · Bridal Showers · Corporate Galas…) — it scrolls infinitely on its own. Built for exactly this.

**Cards that zoom + reveal their caption on hover**
Make the card a **Component** → add a **Hover variant** → in that variant, scale the image up and slide the caption in. Framer animates smoothly between the two states.

**Hover-zoom gallery images**
Same Hover-variant trick — the image scales up on hover.

**Sticky header that darkens on scroll**
Select the nav → Position → **Sticky** (top offset 0). For the darkening, add a **Scroll** effect that changes its background as the page scrolls down.

**Button shine + hover lift**
Build the button once as a **Component**; add a **Hover** effect (slight lift + shadow). For the shimmer, a Hover variant with a moving highlight.

### ⭐⭐ Marketplace helpers (free drag-in components — Insert → search)
Not one-click, but ready-made so you never touch code:

- **Count-up stats** (50+, 100%, 8+) → search **"Counter"** or "Number animation."
- **Scroll-progress bar** (the gold line along the top) → search **"Scroll progress."**
- **Click-to-enlarge lightbox** (gallery) → search **"Lightbox"** or "Gallery lightbox."

Drag it in, point it at your content, done.

---

## Section-by-section build map

| Section | Framer build | Effects to add |
|---|---|---|
| **Hero** | Full-screen Frame, image fill, dark overlay Frame on top, headline + subline + WhatsApp button | Ken Burns **Loop** on image · **Appear** (staggered) on text |
| **Ribbon** | **Ticker** component with service words | Built-in scroll |
| **Stats** | 4-column Stack | Marketplace **Counter** · **Appear** |
| **Featured** | 3 card **Components** (image + tag + title + caption) | **Hover variant** (zoom + caption reveal) · **Appear** |
| **Services** | 4-column Stack of icon cards | **Hover** lift · **Appear** |
| **Gallery** | Grid or Masonry of her real photos | **Hover** zoom · Marketplace **Lightbox** |
| **Founder** | 2-column: image + text; add Benafsha's real headshot | **Appear** slide-in |
| **Testimonials** | Horizontal Scroll of quote cards | **Appear** |
| **How We Work** | 3-column numbered steps | **Appear** |
| **CTA** | Full-width Frame, image + dark overlay, headline + button | **Appear** |
| **Footer** | Navy Frame, 3 columns of links | — |
| **WhatsApp float** | Fixed-position circle Frame, linked to `wa.me/971509118505` | **Loop** pulse (optional) |

---

## Making it work (live)
- **Publish** → free `.framer.website` URL to show the client.
- **Basic plan (~$10/mo)** → connect her custom domain (e.g. prestigeplanners.ae or a subdomain).
- **WhatsApp button** = a link set to `https://wa.me/971509118505?text=...` (pre-filled message). Nothing to install.
- **Mobile:** switch to the Mobile breakpoint and get it flawless — most Dubai traffic is on phones.

---

## Remember
Brand Styles first · elegant and uncluttered · WhatsApp impossible to miss · obsess over mobile. Build the sections, *then* add the Appear / Loop / Ticker / Hover effects — that layering is what makes it all feel like it belongs.
