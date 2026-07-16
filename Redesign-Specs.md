# Prestige — Comprehensive Redesign Specs (from 3 research agents, 2026-07-07)
_Status (2026-07-07, post-restart): ALL SECTIONS **IMPLEMENTED** in prestige-homy.html — Testimonials, FAQ, CTA, Stats "Client Deck", and the Global Polish tiers (label system, gilded-navy buttons, glass nav, hero scrim, grain, watermark, champagne dark panel, mesh backgrounds, video loop crossfade). Refero research done live (Kobu + Cup of Couple full styles; sharp-edge hairline editorial direction confirmed). Remaining: real content from Benafsha, longer seamless hero video (crossfade fallback B is live), mobile pass, her visual review._

Shared motion language (all sections): easing `cubic-bezier(0.22, 1, 0.36, 1)`, durations 600–1200ms, staggers 70–130ms, everything gated behind `prefers-reduced-motion`.

New color tokens (from the polish audit — adopt sitewide):
```css
--gold-ink:   #7A5F29;  /* gold for SMALL TEXT on cream (5.1:1 AA; raw #C4A24C on cream FAILS at 2.1:1) */
--gold-light: #E8CF8A;  /* gold text on navy (8.7:1) + gradient highlight */
--gold-glint: #F6ECC8;  /* metallic hotspot stop */
--gold-shadow:#8C6D2F;  /* metallic dark stop */
--navy-ink:   #08182B;  /* dark champagne-glass section canvas */
--navy-chip:  #0B1626;  /* badge chip fill (never pure #000) */
--hairline: 1px solid rgba(196,162,76,.32);
```

---

## A. STATS SECTION — "The Client Deck" ✅ IMPLEMENTED
Replaces the banner rows + side photos. Stats become *evidence*: every number pinned to a real event.

**Structure**
- 12-col container max-1200. LEFT (cols 1-5, sticky top 120px): Fraunces italic gold intro line, sentence case: "Proof, kept quietly" → heading "Every detail, considered" (Fraunces clamp(40px,4vw,54px)) → one Poppins para (max 46ch): "Eight years of weddings, launches, and long tables under fairy lights. These are the numbers our clients would tell you themselves." → stat rail: 3 rows, padding 28px 0, separated by 1px gold hairlines @35% with a 5px rotated-square gold marker at each rule's left end; each row = Fraunces 600 numeral 44px navy inline + Poppins 15px descriptor; count-up on view (1800ms easeOutQuint `1-(1-t)^5`; 4.9 with toFixed(1)). Quiet gold text link: "See the events behind these numbers".
- RIGHT stage (cols 6-12, relative, h 560px): GHOST NUMERAL "50" Fraunces 600 280px navy @6% top-right, partially overlapped by the deck. DECK of 4 absolutely-positioned client record cards 380×470, radius 24: depth transforms front→back: `translateY(0) scale(1) rotate(-1.5deg)` / `translateY(20px) scale(.955) rotate(1deg)` / `translateY(40px) scale(.91) rotate(-.5deg)` / `translateY(58px) scale(.87)` @45% opacity. (Aceternity Card Stack geometry, tuned.)
- Card anatomy: event photo 16:10 radius 16 inset 14px (mounted-print look) → Fraunces italic 21px title "A harbourside wedding for 180" → keyline row of 2 micro-stats Poppins 14 ("180 guests" + five 14px gold stars) → 1px gold rule @30% → Poppins italic 15px client line "Not one thing went wrong. Not one." + attribution.
- Responsive: <1024 stage under text, cards 340×430; <600 single swipeable card + dots, ghost numeral 160px.

**Visual:** cream canvas; behind stage a vertical `#FBF8F1` band ~55% width, feathered 120px via mask; 2.5% SVG grain overlay; one full-width horizontal gold hairline @30% behind cards at 62% height. Cards: `linear-gradient(165deg,#FBF8F1,#F6EFE1)`, border 1px rgba(0,47,95,.10), shadow `0 2px 6px rgba(0,47,95,.06), 0 28px 56px -28px rgba(0,47,95,.38)`.

**Motion:** left rail fades up 800ms → cards "deal in" from `translateY(60px) rotate(6deg)` 1000ms stagger 150ms. Deck auto-advances every 7000ms: front card eases translateX(46px)+fade 1100ms then re-enters at back; others move up one depth slot. Pause on hover/focus-within; click/dots advance. Optional front-card 3D tilt max 3deg. Reduced motion: static fan.

**Vanilla:** deck = JS array; rotation shifts array and rewrites `data-depth="0..3"`; geometry lives in CSS keyed to `[data-depth]` with `transition: transform 1.1s cubic-bezier(.22,1,.36,1)`. One setInterval, cleared on pointerenter/focusin. `role="group"` + `aria-roledescription="carousel"`; only transform/opacity animate.

**Fallback option (Evening Ledger bento mosaic):** 12-col grid auto-rows 132px gap 20: portrait photo (5col×4row, glass caption chip) + stat card 50+ (4×2) + stat card 4.9 w/ SVG star fill sweep (3×2) + photo w/ frosted glass numeral panel "8+" (3×2, `rgba(251,248,241,.5)` + blur 14px) + navy quote card (4×2, Fraunces italic 22 soft-white quote + gold attribution). Radial `#FBF8F1` bloom + grain + one thin gold SVG arc breaking the top-right. Same count-up utility. (Use if per-event testimonials are weak.)

Key refs: Vivre/San Luis Lodges (vivre.agency/san-luis-lodges), Sport Cover (sportcover.co), Resonant Link (resonant-link.com), Loook.ai, Calder Clark (calderclark.com — editorial proof w/ press names), Aceternity Card Stack (ui.aceternity.com/components/card-stack — CARD_OFFSET 16, SCALE_FACTOR .06), Magic UI Number Ticker + Bento, Aceternity Wobble/Glowing/3D Card.

---

## B. TESTIMONIALS — "The Spotlight Letter" ✅ IMPLEMENTED
One quote at a time, magazine pull-quote + layered photo stack; auto-rotate 7s w/ progress hairline, prev/next, counter, pause on hover; word-by-word blur reveal (600ms, 18ms stagger); photos cycle front/mid/back with tilt (−3°/2.5°, scale .95/.93) + gold hairline inset frame; giant Fraunces quote mark @7% gold bleeding off top-right. Copy: 40-70 words, one key phrase pulled in gold roman inside the italic quote; attribution = names + event line (no job-title format, no stars, no avatars). Sample quotes in place; swap for Benafsha's real reviews. Key ref: Aceternity Animated Testimonials + The Stars Inside "Love Notes" (thestarsinside.com/love-notes) for copy voice.

## C. FAQ — "Questions, answered" ledger ✅ IMPLEMENTED
Two-column: sticky serif intro left ("Questions, answered" + WhatsApp text link) / hairline-ruled single-open accordion right. Fraunces italic gold numerals 01-05, Fraunces 21-22px questions sentence case, thin gold plus that rotates into minus (500ms), grid-template-rows 0fr→1fr height animation (600ms), answer text fades in 150ms after space opens, hover: question slides 4px right. Radial soft-white wash behind the column. No boxes, no chevrons, no caps.

## D. FINAL CTA — "The Invitation" ✅ IMPLEMENTED
Full-bleed dark finale (the only dark moment): real candlelit photo + navy scrim `linear-gradient(rgba(0,47,95,.45), rgba(0,47,95,.78))` + vignette; **1px gold hairline frame inset 28px that draws itself on entry** (scaleX/scaleY from center, 1.2s) — replaces the giant ghost wordmark (now a recognized AI tell, deleted). Content: Fraunces italic gold "Prestige invites you" → 2-line masked-reveal headline (line 2 italic) → one sub line → **magnetic** gold WhatsApp pill (translate ×.18 toward cursor, label ×.06, spring back 600ms) + microcopy "We reply within a few hours, often sooner." + quiet email link. 40s Ken-Burns drift on the photo. Line-mask entrances staggered 130ms.

---

## E. GLOBAL POLISH SPEC (hero / nav / type / backgrounds) ✅ IMPLEMENTED (loop fix = option B crossfade; regenerated 12s loop still optional)
Direction lock: **quiet boutique-hotel editorial**. Gold = a METAL, not a paint: hairlines, borders, gradients, glints; almost never large flat fills.

### Tier 1 quick wins
1. **Kill ALL-CAPS Poppins eyebrows everywhere** (biggest de-AI move). New label system, all Fraunces:
   - A. Italic serif overline (default): `font: italic 500 1.0625rem "Fraunces"; letter-spacing:.015em; color:var(--gold-ink);` + font-variation `"SOFT" 0, "WONK" 1`. Copy mixed-case: "The art of the unforgettable evening".
   - B. Hairline + word: 32px 1px gold rule + middot + italic label (section openers).
   - C. Numbered index: `No. 01 · Planning`, oldstyle-nums italic.
   - Poppins never appears in a label again. If small caps must exist (footer meta only): Fraunces 11px tracking ≤.08em.
2. **Hero contrast:** layered scrim anchored to text zone, not flat overlay: `radial-gradient(70% 55% at 50% 62%, rgba(0,24,43,.42), transparent 72%) + linear-gradient(to top, rgba(8,24,43,.6), transparent 55%)`; H1 soft-white w/ `text-shadow:0 1px 28px rgba(0,21,42,.35)`; verify 4.5:1 at video's brightest frame.
3. **Button system — invert roles: navy carries, gold finishes.**
   - Primary "gilded navy": `linear-gradient(180deg,#003A73,var(--navy) 55%,#00264D)`, text #F8F3E6, border 1px rgba(196,162,76,.55), **border-radius 2px (sharp corner = luxury; retire pills)**, inset top highlight `inset 0 1px 0 rgba(255,255,255,.14)`, hover: warm gold-white **shine sweep** (skewed gradient pseudo-el translateX −130%→320%, .7s).
   - Secondary: transparent + 1px gold border, hover fills rgba(196,162,76,.10).
   - Optional ONE hero metallic-gold CTA: 7-stop ramp `135deg: shadow 0%, gold 22%, light 45%, glint 50%, light 55%, gold 78%, shadow 100%` + navy text. Never both fills on one screen.
4. **Backgrounds:** alternate cream/cream-soft between sections + `radial-gradient(120% 80% at 50% 0%, rgba(196,162,76,.10), transparent 60%)` glow.

### Tier 2 headline fixes
1. **Eyebrow chip:** best = NO chip (system above). Over video if needed = **glass chip**: `rgba(251,248,241,.13)` + blur(10px) saturate(1.3) + border rgba(232,207,138,.45) + `inset 0 1px 0 rgba(255,255,255,.25)` top bevel (the lit edge that stops "painted-on"), Fraunces italic 13px. Dark sections = **metallic engraved chip**: gradient-border via padding-box/border-box stacking + shimmer gold text (`background-clip:text`, 200% gradient, ONE 5s shimmer pass on scroll-into-view, not infinite).
2. **Navbar:** State 1 transparent (cream links/logo over hero). State 2 scrolled: `rgba(251,248,241,.72)` + blur(16px) saturate(1.4) + **gold hairline bottom border** (no shadow), height 88→64px. Link hover: 1px gold underline scaleX(0→1) from left (.3s). Nav CTA = secondary outline btn, never the filled primary. (Floating pill nav = too SaaS, rejected.)
3. **Hero video loop (choppy fix), ranked:** A) regenerate/re-cut asset to **10-15s** with crossfaded seam (best); B) code-only: fade video to poster (frame-1 export) 1s before end: `setTimeout(fade, (v.duration/v.playbackRate - 1)*1000)` on 'playing'/'seeked'; C) two stacked videos crossfading; D) ping-pong REJECTED (no negative playbackRate; reversed human motion looks wrong). Delivery: MP4+WebM, poster=frame1, <5MB, static poster on mobile, pause control + reduced-motion pause (WCAG 2.2.2).
4. **Portfolio badges (done in interim, refine):** navy-chip `#0B1626` glass + gradient gold border (padding-box/border-box), Fraunces italic mixed case ("Private estate"), text `--gold-light`; hover flips gradient angle 135°→315° (ring catches light).

### Tier 3 bigger lifts
1. **Background system for every dead strip:** (a) sitewide SVG grain `feTurbulence fractalNoise baseFrequency .8 numOctaves 4 stitchTiles stitch`, opacity .035, multiply; (b) light mesh: two radial washes (cream-soft + gold @8%) on cream; (c) ONE signature tone-on-tone pattern section: gold hairline lattice `repeating-linear-gradient(90deg, rgba(196,162,76,.05) 0 1px, transparent 1px 72px)` ≤6%; (d) **watermark Fraunces italic glyph** 24rem @7% gold (services/process); (e) ONE dark champagne panel section: `--navy-ink` + gold radial glow @16% + grain screen + glass panels w/ brighter TOP border rgba(232,207,138,.45) = lit glass.
2. **Magnetic CTA** (hero + final only, done in final).
3. **Type pass:** headlines Fraunces `"opsz" 144`, tracking −0.01em, text-wrap balance; Poppins demoted to body 400/500 15-16px lh 1.7, never tracked/uppercase; `font-variant-numeric: oldstyle-nums`; pull quotes = hanging gold quote mark, not cards.

### De-AI acceptance checklist
1. Zero letterspaced ALL-CAPS Poppins labels. 2. Zero em dashes (middots/colons/commas/full stops; ranges use "to"; meta separators `Est. 2019 · Dubai`). 3. No flat gold fills (except optional one metallic hero CTA). 4. No pure #FFF/#000 (darkest #0B1626, lightest #FBF8F1). 5. One radius language: 2px buttons/panels, 999px chips only. 6. Every beige strip carries grain + one of mesh/glow/watermark/pattern. 7. Hero loop 10s+ seamless, reduced-motion poster, pause control. 8. Gold text on cream = #7A5F29 always. 9. Signature moves: champagne glass panel + watermark serif glyphs.

---

## NEXT-SESSION EXECUTION ORDER
1. Restart activates **Refero MCP** → verify with a styles/screens search before building.
2. Tier 1 global pass (labels system, buttons, scrim, background alternation) — touches every section.
3. Build Stats "Client Deck" (section A).
4. Hero video: regenerate 12s seamless loop (Higgsfield, extend current scene) or apply code crossfade B.
5. Tier 2: nav glass, chip system, badge refinement.
6. Tier 3: grain + watermark + champagne panel + marquee-section background fill.
7. Re-audit against the De-AI checklist.
Also outstanding from Kriti's feedback: arch pop-up must tie cohesively into the portfolio story; marquee section background needs filling; blur-panel text centering check; "moments" gold shine.
