# Homy Template — Full Decode & How to Replicate for Prestige
_Kriti loves the **Homy** Framer template ([framer.com/community/marketplace/templates/homy](https://www.framer.com/community/marketplace/templates/homy/), $49). This decodes every section's animation and how to rebuild it for Prestige._

## ⚠️ THE GOLDEN RULE (again)
Homy is a **real-estate template**: bold black grotesk sans, dark cards, property/price content. Prestige is **LIGHT + GOLD serif editorial.** We steal the **MOTION and STRUCTURE**, NOT the look. Re-skin every section to cream/navy/gold + Fraunces/Poppins, and strip all real-estate bits (prices, "listings," "Book a Visit").

## 💡 SMARTEST PATH — buy & re-skin (recommended)
Framer AI can't reliably build these layered scroll effects from a prompt (that's why Claude Design looked bad). But **Homy already has them built.** So:
1. **Buy Homy ($49)** and remix it into your Framer account.
2. **Re-skin globally:** swap its font for Fraunces + Poppins, its colors for cream #F3ECDC / navy #002F5F / gold #C4A24C, its images for Benafsha's real event photos.
3. **Rewrite content** for a wedding planner; **delete** property-specific parts (price badges, "listings," rental language).
4. Keep the animations as-is — they're the whole reason to buy it.
This gets the exact motion she loves in a day, versus weeks fighting AI. The animations below explain what each does so she knows what she's re-skinning.

---

## Section-by-section decode

### 1. HERO — layered scroll (house rises, text sinks behind, clouds drift) ⭐ signature
- **What it is:** Headline + buttons + a house silhouette; fog/clouds at the bottom. On scroll the **house rises up**, the **headline+buttons shrink and slide up *behind* the house**, and **clouds drift** across the front obscuring it. Layer order: clouds (front) → house (middle) → text (back).
- **Animation name:** **scroll-linked layered parallax** on a **pinned hero**, with z-index layering so text passes *behind* the house.
- **How it's built:** Framer Motion `useScroll` + `useTransform` mapping scroll → each layer's `y`/`scale`/`opacity`; a transparent fog PNG on top drifting on `x`. In Framer native: pin the section + add a **Scroll effect** (parallax) to each layer at different speeds, with the house on a higher layer than the text. Complex but the template already does it.
- **Prestige version:** house silhouette → a **wedding arch / floral installation / venue cutout PNG**; clouds → **soft light haze or drifting petals**; bold sans headline → big **Fraunces serif** "We curate bespoke moments." Text sinks behind the arch as it rises.

### 2. OUR IMPACT — clean rounded stat boxes (minimal motion)
- **What it is:** A heading + 3 rounded stat rows ($4.6M+ / 320+ / 98%) flanked by two photos. Lots of white space. Just a gentle reveal-on-scroll.
- **Animation:** **Appear (fade + rise)** on scroll. No counters (static numbers — matches Kriti's "no generic counters" rule).
- **Prestige version:** her social proof in rounded **cream** boxes — but per her decision, use the **editorial line + Google rating**, or "50+ celebrations / ★4.9 / bespoke," flanked by two real event photos. Rounded boxes = her "bubble" motif.

### 3. DISCOVERY — blur-to-focus word reveal ⭐
- **What it is:** "Focused on **discovery**, built for…" — words start **blurred + faded** and **sharpen into focus** as you scroll, forming a full sentence.
- **Animation name:** **scroll-triggered blur-to-focus text reveal** (`filter: blur()` + opacity mapped to scroll).
- **How it's built:** Framer Motion `useTransform` on `filter: blur(Npx)` + opacity per word; or a Framer Scroll effect animating blur. GSAP SplitText for word-by-word if coded.
- **Prestige version:** a poetic line — "Focused on the **details**, built for the **unforgettable**." Navy Fraunces, the accent words in gold, blur-sharpening on scroll.

### 4. TOP PROPERTIES — stacked full-bleed cards slide up ⭐
- **What it is:** Full-screen event images that **slide up and stack on top of each other** as you scroll (Sky High Condo, Downtown Loft…), each with a badge + name + location + button.
- **Animation name:** **sticky scroll-stack** (each full-bleed card pins, the next slides over it).
- **How it's built:** sticky positioning per card + scroll transform; native in Framer via sticky sections.
- **Prestige version:** her real events as stacked full-bleed cards — couple name + venue + "View" (NO price, per her decision). This can BE the portfolio/magazine-cover section (Entry 7).

### 5. OUR SERVICES — expanding accordion cards ⭐ (she loves this)
- **What it is:** Cards .01 .02 .03; click one → it **expands** (black, image, title jumps to top) while the **others shrink into grey boxes** and slide aside. Self-organizes.
- **Animation name:** **interactive expanding accordion** with **layout animation**.
- **How it's built:** a Framer **component with active/inactive variants** + layout transition (Framer Motion `layout`); click swaps the active one. Native-ish in Framer.
- **Prestige version:** her 3 services — **Planning · Styling · Coordination** — as this accordion. Active card = gold/cream with a real photo + description; inactive = collapsed with a big gold number. (Replaces the static Entry 6 grid with something far richer — she likes this more.)

### 6. PROPERTY LISTINGS — word marquee behind a floating image ⭐
- **What it is:** Big words ("Live Better · Explore Homes · …") **scroll horizontally** with a **floating image in the center**; bottom gradient-blurred so text stays clean.
- **Animation name:** **headline marquee/ticker behind floating imagery** — this IS Kriti's gallery "bubble-words behind images" idea (Entry 9).
- **How it's built:** Framer **Ticker** (or two, opposite directions) on a layer behind a centered image + a bottom gradient mask.
- **Prestige version:** outline/gold serif words — "Timeless · Bespoke · Unforgettable · Dubai" — drifting behind her floating gallery images. Merge with Entry 9.

### 7. HIGHLIGHTED HOME — video scales to full-screen on scroll ⭐⭐ (her favourite)
- **What it is:** A **video** plays in a card; key text slides side-to-side **behind** it; as you scroll the **video grows until it fills the screen**; scroll back and it **shrinks**. Giant "HOMY" wordmark behind.
- **Animation name:** **scroll-scrubbed video scale-to-fullscreen** + side-scrolling text + oversized outline wordmark.
- **How it's built:** Framer **Scroll effect** mapping scroll → the video frame's `size`/`scale`; a Ticker of text behind; a huge outline wordmark on a back layer.
- **Prestige version:** her hero highlight event **video** (⚠️ **use a PLACEHOLDER video block for now** — Benafsha has no video yet; swap real footage/IG Reel later, or a Higgsfield cinemagraph from her photos). Behind it: giant outline **"PRESTIGE"** wordmark + drifting words.

### 8. CLIENT REVIEWS — testimonial cards + featured photo card
- **What it is:** Row of quote cards (name + role + photo), one **featured card = full-bleed portrait** (Ethan Walker). Horizontal scroll.
- **Animation:** horizontal scroll / hover lift; featured card is a photo.
- **Prestige version:** her REAL named reviews (needs names + event type); featured card = a real client or Benafsha.

### 9. FAQ — clean accordion
- **What it is:** "Things You Should Know" +/- expandable rows. Basic but tidy.
- **Prestige version:** wedding/event FAQ — lead times, what's included, do you travel, how booking works. (Also a low-key SEO win.)

### 10. FINAL CTA + FOOTER — full-bleed graphic + lead-capture modal + giant wordmark
- **What it is:** Same hero graphic full-screen, "Discover homes… / Get in Touch" → button opens a **lead-capture popup with a map + form**; giant "HOMY" watermark; footer blends in.
- **Animation:** button → modal reveal; oversized wordmark.
- **Prestige version:** "Let's plan something **extraordinary**" + Enquire/WhatsApp (or the simple Check-Availability form, Entry 8); giant outline **"PRESTIGE"** wordmark; footer with WhatsApp/email/IG.

---

## Which Homy animations map to Kriti's existing swipe entries
- Hero layered parallax → NEW signature (replaces plain Ken-Burns hero, Entry 1) — grander.
- Services accordion → upgrades Entry 6 (static grid → interactive accordion). She prefers this.
- Stacked full-bleed cards → Entry 7 (portfolio covers).
- Word-marquee-behind-image → Entry 9 (gallery bubble words) — same effect.
- Blur-to-focus text → new; pairs with her "words pop out blurred/unblur" love.
- Video scale-to-fullscreen → her favourite; needs a **placeholder video** for now.

## Video placeholder note
Everywhere Homy uses video (hero highlight, sec 7), drop in a **placeholder video block** (a muted looped stock/ambient clip, clearly temporary) until Benafsha provides real footage or an IG Reel — then swap. Do NOT ship synthetic AI wedding video as her "real" work.
