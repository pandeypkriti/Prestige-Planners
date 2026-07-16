# Framer AI Prompts — Prestige Planners
_Paste ONE frame at a time into Framer AI. Review the result, tweak, then ask Claude for the next frame. Built from the locked swipe file: LIGHT + GOLD editorial, no pricing, no counters, real photos only._

**Order of frames:** 0 Setup → 1 Hero → 2 Positioning line → 3 Services → 4 Portfolio covers → 5 Gallery + marquee → 6 Founder → 7 Testimonials → 8 Journal → 9 Instagram → 10 Check Availability → 11 Footer.

---

## FRAME 0 — Project setup (do this manually before any AI prompt)
Not a prompt — do this in Framer first so every generation stays on-brand:
1. Create **Color Styles:** Cream `#F3ECDC` (page background), Navy `#002F5F` (headings/text), Gold `#C4A24C` (accents/buttons), Soft White `#FBF8F1` (alt section bg), Rust `#903E1F` (rare accent), Sage `#A4C0AA` (rare accent).
2. Add fonts: **Fraunces** (or Playfair Display) for display serif, **Poppins** for body.
3. Create **Text Styles:** Display XL (Fraunces 300, ~90px desktop, navy, tight leading), H2 (Fraunces 400 ~48px navy), Eyebrow (Poppins 500, 12px, letterspacing 0.3em, uppercase, gold), Body (Poppins 300, 16px, dark slate), Button (Poppins 500, 14px).
4. Upload her real event photos (the `assets/` folder) to the project.

---

## FRAME 1 — HERO

Copy-paste into Framer AI:

```
Create a full-screen luxury hero section for "Prestige Planners", a high-end wedding and event planning studio in Dubai. Light, editorial, Vogue-magazine mood — NOT dark.

LAYOUT
- Full viewport height. Background: a full-bleed photograph of an elegant event tablescape (placeholder image for now), very slowly zooming in over 20 seconds (subtle Ken Burns loop, scale 1.0 to 1.08, ease in-out, alternating).
- Over the photo, a soft cream overlay (#F3ECDC at 55% opacity) lus a gentle white gradient from the bottom, so the image feels airy and light, and navy text is always readable.
- Content centered horizontally, vertically slightly above center.

NAVIGATION (part of this frame)
- Transparent navbar over the hero: left = wordmark "Prestige" in Fraunces serif italic, navy #002F5F, with "PLANNERS · DUBAI" beneath it in tiny letterspaced Poppins uppercase, gold #C4A24C.
- Right = one pill button: "Enquire on WhatsApp", gold #C4A24C background, navy text, fully rounded, subtle lift + soft gold shadow on hover. Link: https://wa.me/971509118505?text=Hi%20Prestige%20Planners%2C%20I%27d%20love%20to%20enquire%20about%20planning%20my%20event.
- On scroll, navbar background fades to solid cream #F3ECDC with a 1px gold bottom hairline.

HERO CONTENT (staggered fade-up on load, 0.15s delay between items, slow elegant easing)
1. Eyebrow: "LUXURY WEDDINGS & EVENTS · DUBAI" — Poppins 500, 12px, 0.3em letterspacing, uppercase, gold #C4A64C.
2. A 60px horizontal gold hairline that scales in from 0 width.
3. Headline, Fraunces light, very large (~90px desktop / 42px mobile), navy #002F5F, two lines:
   "We curate bespoke moments,"
   then in italic: "crafting timeless memories" — with the word "timeless" in gold.
4. One line of body text, Poppins 300, max 560px wide, dark slate: "From intimate celebrations to grand affairs — designed end to end, so you can simply be present."
5. One button only (same gold WhatsApp pill as the nav, larger padding).
6. Bottom center: a tiny "SCROLL" label in letterspaced Poppins with a 1px vertical gold line beneath it that gently pulses (opacity + scaleY loop).

RULES
- Fonts: Fraunces for all serif headlines, Poppins for everything else. No other fonts.
- Colors only from: cream #F3ECDC, navy #002F5F, gold #C4A24C, white.
- Motion must be slow and subtle — luxury whispers. No bounces, no fast movement.
- Mobile: headline 42px, nav shows logo + WhatsApp pill only, image swaps to a portrait crop, everything still fades up. Must look flawless at 390px width.
- Generous white space. No extra elements, badges, or decorations beyond what is specified.
```

**After it generates, check:** headline is Fraunces and *large*, overlay keeps it light (not washed out, not dark), one CTA only, mobile at 390px, and the Ken-Burns is *slow*. Swap the placeholder photo for one of her real bright/airy images (e.g. the "Something Blue" tablescape). If you have a video clip later, replace the image fill with an autoplay-muted-loop video and keep the cream overlay.

---

_Frame 2 (Positioning line + editorial social proof) — superseded by the Master Baseline Prompt below._

---

# MASTER BASELINE PROMPT (2026-07-05)
_The one-shot brief for the Framer AI agent. Attach images first (see manifest), paste the whole block, then iterate section-by-section. Encodes: light+gold mood, Homy animations, Royal flipper (few photos), stock placeholder hero video like MOD, no counters, no pricing, single CTA._

**Attach these files to the agent before sending:**
- `Prestige final logo jpeg .jpg.jpeg` (logo)
- From `assets/`: `38-1.png` (blue bridal-shower tablescape — brightest, hero-adjacent), `33.png` (black & gold birthday), `30.png` (butterfly baby shower), `26.png` (fairy-light banquet), `34.png` (40th balloon installation), `36.png` (gold orb styling)

## HERO v2 — chic two-screen (2026-07-06, REPLACES earlier hero)
_Feedback: first output was "a blank canvas with a huge logo, too basic." Fix: NO logo graphic — elegant centered serif NAME + location over a dimmed video (chic like MOD Events). WhatsApp present from screen 1. The "We curate bespoke moments…" phrase moves to screen 2 as a scroll reveal._

```
Replace the current hero with TWO stacked full-screen sections.

SCREEN 1 — the intro (chic, cinematic, like a luxury film title card / MOD Events):
- Full viewport height. Background: a muted, autoplaying, looping video filling the entire screen (elegant event ambience — candlelight, florals, drifting fabric; placeholder video for now, I will replace it).
- Over the video, a deep navy overlay (#002F5F at ~65% opacity) so it is dim, moody and opaque — the video is felt, not loud.
- Do NOT use a large logo graphic. Perfectly centered, with lots of empty space:
   • "Prestige Planners" in Fraunces serif, medium-large, cream #F3ECDC, understated, slightly open letter-spacing.
   • A thin gold hairline beneath it, then "DUBAI · UNITED ARAB EMIRATES" in small Poppins uppercase, 0.3em letter-spacing, gold #C4A24C.
- Minimal transparent top nav: small "Prestige Planners" wordmark left; ONE gold pill "Enquire on WhatsApp" right (https://wa.me/971509118505?text=Hi%20Prestige%20Planners%2C%20I%27d%20love%20to%20enquire%20about%20planning%20my%20event.). Nothing else.
- Bottom center: a small letterspaced "SCROLL" label, cream, with a thin gold vertical line that gently pulses.
- Everything fades in slowly on load. Generous negative space. Minimal, chic, expensive. Flawless on mobile at 390px.

SCREEN 2 — the reveal (directly below; the writing appears here on scroll):
- Full viewport height, background cream #F3ECDC.
- Centered, revealing as a scroll feature — each line fades + rises + softly un-blurs into place as it scrolls in:
   "We curate bespoke moments,"
   italic "crafting timeless memories" — "timeless" in gold #C4A24C.
   Fraunces serif, very large, navy #002F5F.
- Below: one line Poppins body, dark slate: "From intimate celebrations to grand affairs — designed end to end, so you can simply be present."
- Below that, the gold "Enquire on WhatsApp" pill again.
- Slow, staggered, elegant motion. No bounce.

RULES: Fraunces for serif, Poppins for body. Only cream #F3ECDC, navy #002F5F, gold #C4A24C, white. Motion slow and subtle. No stats, badges, or extra sections.
```

---

## The one-shot master prompt (full page) — use after the hero is right:

```
You are building a landing page for PRESTIGE PLANNERS — a luxury wedding & event planning studio in Dubai, run by founder Benafsha. The mood is LIGHT, editorial, Vogue-wedding luxury. Never dark, never techy, never generic-AI.

=== BRAND KIT (use exactly, set as project styles first) ===
Colors: Cream #F3ECDC (page background), Soft White #FBF8F1 (alternating sections), Navy #002F5F (headlines/text), Gold #C4A24C (accents, buttons, hairlines), Rust #903E1F and Sage #A4C0AA (rare small accents only).
Fonts: Fraunces (or Playfair Display) for ALL display/headlines — light weight, large sizes, occasional italic accents with single words in gold. Poppins (300/500) for body and labels. Labels/eyebrows: Poppins 500, 12px, uppercase, 0.3em letter-spacing, gold.
Buttons: fully rounded gold pills, navy text, subtle lift + soft gold shadow on hover.
I have attached the logo and 6 real event photographs — use ONLY these photos, never stock photography. The blue tablescape image is the brightest and best for large placements.

=== GLOBAL RULES ===
- One primary CTA everywhere: "Enquire on WhatsApp" → https://wa.me/971509118505?text=Hi%20Prestige%20Planners%2C%20I%27d%20love%20to%20enquire%20about%20planning%20my%20event.
- NO pricing anywhere. NO animated count-up counters. NO cursor effects.
- Motion is slow, subtle, elegant — luxury whispers. Fades, soft parallax, gentle blur-to-focus. No bounces.
- Generous white space. Mobile-first: must be flawless at 390px.
- All numbers/social proof appear as editorial serif sentences or a Google ★ rating pill — never stat dashboards.

=== PAGE STRUCTURE (in this order) ===

1. HERO — full-bleed muted looping STOCK VIDEO placeholder (elegant event ambience: candlelight, florals, soft fabric — I will replace with real footage later). Over it: soft cream overlay (~50%) + white gradient from bottom so it stays LIGHT and navy text is readable. Transparent nav (logo left, WhatsApp gold pill right; on scroll nav turns solid cream with 1px gold bottom hairline). Centered: gold eyebrow "LUXURY WEDDINGS & EVENTS · DUBAI", a gold hairline that scales in, huge Fraunces headline "We curate bespoke moments," / italic "crafting timeless memories" with "timeless" in gold, one short subline, ONE gold CTA. Staggered fade-up on load. Small pulsing SCROLL cue at bottom.

2. FLIPPER STRIP — keep the template's flipper animation but use FEW images: maximum 3–4 of my attached photos, large, slow, with breathing room. Do not crowd it.

3. POSITIONING LINE — full-width cream section, one huge serif sentence that BLURS INTO FOCUS word by word as you scroll: "Focused on the details, built for the unforgettable." — "details" and "unforgettable" in gold italic. Below it, small and quiet: "★★★★★ Loved by our clients · Reviewed on Google" as a tiny gold pill.

4. SERVICES — interactive expanding accordion cards (like premium templates): three cards .01 Planning, .02 Styling, .03 Coordination. Clicked card expands with a real photo + 2-line description; the others collapse into slim cream boxes with a large gold number. Smooth layout animation.

5. PORTFOLIO — "Real Celebrations": full-bleed stacked cards that slide up and pin one over another on scroll. Each card = one real event photo, couple/host name placeholder, venue placeholder, small "View" link. 3 cards max. No prices.

6. GALLERY — masonry of the remaining real photos. BEHIND the images: two lines of huge OUTLINED (hollow stroke) gold serif words drifting horizontally as you scroll — one line enters from the left, the other from the right: "Timeless · Bespoke · Unforgettable · Dubai". Images sit on top; words peek through the gaps. Click any image to enlarge.

7. FOUNDER — "Meet Benafsha": two columns, portrait placeholder left (label it "Founder portrait — replace"), right an eyebrow "MEET YOUR PLANNER", serif headline "Hello, I'm Benafsha", two short warm paragraphs (aviation + hospitality background, London to Dubai, works directly with every client), italic gold signature "Benafsha". Soft slide-in on scroll.

8. TESTIMONIALS — horizontal row of cream quote cards, gold top border, serif italic quotes with [PLACEHOLDER — real Google review] text, name + event type lines. One featured card is a full-bleed photo card.

9. FROM THE JOURNAL — two parts: (a) one featured post block: image left, eyebrow "FROM THE JOURNAL", serif title "The Power of Detail", one-line excerpt, "Read" link — fades up on scroll. (b) below it, a hover-reveal index: three rows of article titles in large navy serif with thin gold hairline dividers — "The Art of the Guest List", "Innovative Décor, Quietly Done", "Planning Without the Stress" — hovering a row softly reveals a small image beside it and the row's title turns gold.

10. INSTAGRAM — cream section: eyebrow "FOLLOW OUR JOURNEY", serif headline, a QR code placeholder frame linking to https://www.instagram.com/prestigeplannersuae/, and a gold "Click here" pill to the same URL. 3 small square photo tiles beside it.

11. CHECK AVAILABILITY — split section: left = one real photo; right = serif headline "Check Availability", short line "Tell us your preferred date, month or season — we'll confirm availability and send our Services Guide.", a SIMPLE form (Name, Event type, Preferred date/season, Email or WhatsApp) submitting to email, and below it small rounded gold outline pills: "Unlimited consultations" · "Exclusive vendor perks" · "Venue tours" · "Complimentary design renders". NO pricing pill.

12. FINAL CTA + FOOTER — full-width cream-to-soft-white band: giant outlined "PRESTIGE" wordmark in the background (very low opacity gold stroke), serif headline "Let's plan something extraordinary", one gold WhatsApp CTA. Footer: logo, WhatsApp +971 50 911 8505, contact@prestigeplanners.ae, Instagram link, Meydan Grandstand Dubai, discreet copyright. A floating WhatsApp bubble stays bottom-right on every screen.

Build desktop + mobile breakpoints. Keep every animation subtle and slow. Do not add sections, badges, stats, or stock photos beyond what is specified.
```
