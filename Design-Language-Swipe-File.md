# Prestige — Design Language & Swipe File
_Kriti's collected UI references. Each entry = what she loves → what it's called → how we build it in Framer → prompt notes. This is a LIVING doc — we keep adding. When Kriti says "code this," these references are what she means._

**Workflow:** Kriti collects references → Claude turns each into a **Framer AI prompt** → she feeds it to Framer AI → agents build & iterate.

**Locked brand:** Navy `#002F5F` · Gold `#C4A24C` · Cream `#F3ECDC` · Rust `#903E1F` · Sage `#A4C0AA` · Fonts: Fraunces/Playfair (display serif) + Poppins (body). Contact via WhatsApp +971 50 911 8505.

---

## 🔒 ENTRY 1 — Full-page autoplay VIDEO HERO  ·  *NEED (non-negotiable for frame 1)*
**Source:** MOD Events — [modevents.ae](https://www.modevents.ae/) ("Dream with MOD")
**What she loves:** The whole first screen is a continuously-playing background video dedicated to the brand. Every luxury site she's seen has video playing. This is the required first framing of the landing page.
**What it's called:** **Full-bleed autoplay background video hero** (muted, looped, poster fallback).
**Build in Framer:** Full-screen Frame → insert a background **Video** (autoplay, loop, muted, hidden controls) → dark overlay Frame (~35%) → brand logo + oversized serif headline + one CTA on top. Mobile: swap to a static poster image under 768px.
**Prompt notes:** must say "autoplay, muted, looped background video, dark overlay, centered serif logo + headline + single gold CTA, mobile poster fallback."

## 🔒 ENTRY 2 — "Follow us on Instagram" section  ·  *WANT*
**Source:** MOD Events (section lower on the page)
**What she loves:** A dedicated section inviting visitors to follow on Instagram — she wants this on hers, **with a QR code** and a **"Click here" button**.
**What it's called:** Instagram CTA / social-follow section (with QR + button).
**Build in Framer:** Section with heading "Follow our journey" → a QR code image linking to [@prestigeplannersuae](https://www.instagram.com/prestigeplannersuae/) → a gold "Click here" button linking to the same → optional live Instagram feed embed.
**Prompt notes:** "Instagram follow section: heading, QR code, and a 'Click here' button both linking to the IG profile."

## 🔒 ENTRY 3 — All videos AUTOPLAY  ·  *global rule*
**What she loves:** Videos throughout the site should autoplay (not click-to-play) for an immersive feel.
**Build note:** every video = autoplay + muted + loop + `preload` optimized + poster fallback (mobile serves image). Applies site-wide.

## 🔒 ENTRY 4 — Enriching SCROLL EXPERIENCE  ·  *WANT (reference: GEM)*
**Source:** Restaurant GEM (Awwwards winner) — dark cinematic, Michelin fine-dining
**What she loves:** The overall enriching, cinematic scroll — content revealing elegantly as you move down. She wants her scroll to *feel* like GEM.
**What it's called:** **Scroll-driven / scroll-triggered storytelling** (reveals, pinned sections, cinematic pacing) — powered by GSAP ScrollTrigger + smooth scroll (Lenis) in code, or Framer's **Scroll** + **Appear** effects.
**Build in Framer:** smooth scroll on; each section uses Appear (fade + rise), some images use a Scroll (parallax) effect; keep motion slow and purposeful.

## 🔒 ENTRY 5 — GEM hero LAYOUT + the left/right moving text  ·  *WANT + "what is this animation?"*
**Source:** Restaurant GEM hero + the big outlined words that move as you scroll
**What she loves:** (a) the GEM hero *layout* — huge serif "Restaurant / GEM." split over the image with a short intro line + Michelin marks; (b) the big words **below the frame that move left and right** as you scroll.
**What it's called:**
- The moving words = a **kinetic typography marquee** (a.k.a. **ticker / infinite scrolling text**). Because two lines slide in **opposite directions** and their speed reacts to how fast you scroll, it's specifically a **scroll-velocity / opposing-direction marquee**.
- The see-through hollow letters = **outline (stroke) text** (transparent fill + a thin gold stroke).
**What we use it for:** filling "blank" areas with elegant motion (your exact fix for "too empty"), section dividers, and repeating brand keywords — e.g. `Weddings · Bespoke · Timeless · Dubai · Prestige ·` drifting across in outlined gold serif.
**Build in Framer:** the **Ticker** component (constant drift) for the simple version; for the scroll-reactive opposing-direction version, a Scroll effect on two Ticker rows moving opposite ways, or a small Code Component using Framer Motion `useScroll`+`useVelocity`. Style the text as outline (stroke) serif in gold.
**Build in code (if ever):** GSAP ScrollTrigger horizontal loop tied to scroll velocity, or Framer Motion `useVelocity` → `x` transform; CSS `-webkit-text-stroke` for the outline.

## 🔒 ENTRY 6 — Services three-column editorial block  ·  *WANT (with a caveat)*
**Source:** an editorial wedding-planner site (Planning / Styling / Coordination columns + "As Seen On" press logos + testimonials)
**What she loves:** the clean magazine feel — three tall image columns, big serif labels, a "Learn More" pill on each, then a press-logo bar and quotes. Feels "like a newsletter, fun."
**Her own caveat (correct):** worries it's *informational, not enriching.* See the RHYTHM note in Open Decisions.
**Build in Framer:** three full-height columns (image + serif label + Learn More). Lift it from "newsletter" to "enriching" with **video-on-hover** (column plays a short clip), staggered Appear reveal, and a slow zoom. Keep the press-logo + testimonial bars (social proof) but fade them in on scroll.

## 🔒 ENTRY 7 — Portfolio as "Real Wedding Highlights" magazine covers  ·  *WANT*
**Source:** portfolio row of tall vertical cards, each a magazine cover (couple names top e.g. "TRACY + VY", huge serif title e.g. "A WILDFLOWER REVERIE", venue caption bottom).
**What she loves:** each real event styled like an editorial cover — named, titled, venued. This is the honest, luxury way to show her real work (fixes the "photo dump" gap).
**Build in Framer:** horizontal row/scroll of tall cards; hover zoom; each links to the event. Populate with Prestige's REAL events (needs names + titles + venues from Benafsha).

## 🔒 ENTRY 8 — "Check Availability" page (simple)  ·  *WANT*
**Source:** split page — huge serif "CHECK AVAILABILITY!", short intro ("tell us your date/month/season, we'll confirm & send the Services Guide with pricing"), a big photo one side, and a stack of **pill-shaped "bubble" inclusions** (Unlimited Meetings · Vendor Perks · Chauffeured Venue Tours · Transparent fees from $X · Complimentary renders).
**What she wants:** a check-availability page but **NOT overcomplicated** — a short form (name, date/month/season, contact) that emails Benafsha, not a full booking engine.
**Build in Framer:** Framer Forms (name + date/season + email → send-to-email/webhook), split layout, gold pill list with subtle hover. Needs Benafsha's real inclusions + starting price.

## 🔒 ENTRY 9 — Gallery: outline "bubble writing" behind images on scroll  ·  *WANT*
**What she wants:** entering the gallery, big **outlined (stroke) words** emerge from *behind* the images as she scrolls — one line slides in from the **right**, another from the **left**.
**What it's called:** this is the **scroll-velocity opposing-direction kinetic marquee** from [[Entry 5]], layered *behind* the gallery grid (z-index below images). Outline/stroke gold serif; e.g. `Timeless · Bespoke · Unforgettable`.
**Build in Framer:** two Ticker rows (opposite directions) on a layer behind the gallery, or a Code Component using Framer Motion `useScroll`+`useVelocity`; CSS `-webkit-text-stroke` for the hollow letters.

## 🔒 ENTRY 10 — "From the Journal" blog section  ·  *WANT — BOTH treatments*
**Source refs:** hover-reveal editorial index ([Roche Musique](https://www.awwwards.com/inspiration/list-image-hover) / [Codrops](https://tympanus.net/codrops/2018/11/27/image-reveal-hover-effects/)) + "Latest from the Journal" featured block ([Kinfolk](https://www.kinfolk.com/) register).
**What she wants:** BOTH — a **featured post block** (one big post, full-bleed image, serif overline "From the Journal," navy title, fades up on scroll) ABOVE a **hover-reveal index** (vertical list of article titles in big navy serif on cream, gold hairline dividers; hovering a title softly blooms a wedding image beside it).
**Content:** feature only her 3 strongest posts, re-titled editorially (e.g. "The Power of Detail," "The Art of the Guest List," décor piece). Blog is stale (all 20 Jun 2025) — tell Benafsha to post occasionally; not a blocker.
**Build in Framer:** featured = Appear (fade+rise) on an asymmetric block; index = list rows each with a **hover variant** revealing an image layer + gold divider. Both native, no code. AVOID cursor-follow/WebGL (too techy for cream+gold).

## 🔒 ENTRY 11 — Social proof WITHOUT generic counters  ·  *decision*
**Kriti's call (2026-07-05):** rejects the animated count-up stat block — "too generic." Replace with a luxury alternative (pick one/combine): (a) **numbers woven into an editorial serif sentence** ("Over fifty celebrations, one obsession with detail."); (b) **a real Google ★rating badge** linking to reviews (honest, she has real reviews); (c) **a specificity ribbon/marquee** of real couple/venue names ("Tracy & Vy · Athol Hall · …") — ties to the outline-marquee motif; proof by *specificity*, not a count; (d) **static stat column** with gold hairline rules (refined type, no bounce). AVOID: bouncy count-up numbers. Recommended for light+gold = (a) editorial line + (b) Google rating.

---

## ⚠️ OPEN DECISIONS / WEAK POINTS — for Kriti to research her taste & report back
_These aren't covered yet. Kriti researches each, tells Claude her call, Claude stores it here → then writes the Framer prompts._

1. **MOOD — ✅ RESOLVED (2026-07-05): LIGHT + GOLD.** Cream/light editorial dominant with gold accents and navy for depth. The dark refs (MOD/GEM) are *inspiration only* — adapt their motion/layout to Prestige's light navy/gold/cream brand kit, do NOT copy their dark palette.
2. **VIDEO — ⚠️ PART-RESOLVED (2026-07-05).** Confirmed: website = photos only (no video); no real TikTok (the @luxuryprivatespaces / @dubaiprestige.pl results are OTHER companies). Instagram @prestigeplannersuae *may* have Reels but is behind a login wall — **Kriti must check the IG logged in & download any good clips (Claude can't).** Plan: (a) use her real IG Reels if they exist; (b) default = Ken-Burns/parallax motion on her REAL photos (suits light editorial); (c) optional = Higgsfield **image-to-video cinemagraphs made FROM her real photos** (candles/fabric moving) for a hero accent. AVOID fully-synthetic stock video — inauthentic. Note: for a LIGHT editorial look a big *still* hero with motion often reads more luxe than a video hero.
3. **RHYTHM (answers her "is this enriching?" worry).** Don't make *every* section cinematic — that's exhausting and slow. Alternate **loud experiential** beats (hero video, gallery marquee, founder) with **quiet informational** beats (services grid, check-availability). The contrast is what feels enriching. So Entry 6 staying "newsletter-clean" is *correct* — just add hover-motion, don't over-animate it.
4. **NAV STYLE.** Transparent-over-hero (like the refs) vs a full-screen overlay menu (like GEM). Pick one.
5. **TYPE TREATMENT.** Big all-caps serif + italic accents (as in the refs) — confirm she wants that on Fraunces/Playfair.
6. **PRICING — ✅ RESOLVED (2026-07-05): NO pricing on the landing page.** Pricing is delivered *after* enquiry via the "Services Guide." So drop the price pill from the Check-Availability inclusions (Entry 8); the intro can still say "we'll send our Services Guide, which includes pricing."
7. **PRIMARY CTA.** She now has WhatsApp *and* Check Availability. Pick ONE primary so it doesn't dilute.
8. **FOUNDER SECTION.** Editorial "Meet Benafsha" — portrait + story, or a short intro video? Needs her real headshot/bio.
9. **MOBILE.** Most Dubai traffic is phones; heavy motion can break there. Decide mobile priority (it should be high).
10. **INTRO / CURSOR polish (optional).** Logo-reveal loading screen? Custom cursor? Both add luxury but cost load time — taste call.
11. **BLOG.** Refs show "Our Blog" in nav; hers is stale. Include (commit to posting) or hide.
12. **REAL CONTENT still needed from Benafsha:** testimonials (names + event), event titles/venues for the covers, headshot/bio, any press features, inclusions + starting price, and whether any video exists.

### Newly surfaced gaps (2026-07-05) — beyond visuals:
13. **COPY / MESSAGE (biggest missing piece).** She's specced all the *visuals* but none of the *words* — the hero promise/tagline, section headlines, the emotional voice. A luxury page lives or dies on copy. Needs writing.
14. **"WHY BENAFSHA" differentiator section.** Her edge = solo, personal, hands-on, cultural understanding (Dubai). Not yet a section. This is what converts luxury clients.
15. **PROCESS / "How It Works"** — 3-step reassurance (Enquire → Consult → We handle everything). Was in v1; re-confirm for the new design.
16. **HONEST trust signals.** No press/awards → can't fake "As Seen On." Use what's real: Google star rating + named testimonials + event count. Decide the trust bar.
17. **SECTION ORDER / narrative flow.** The sequence of sections (hero → ? → ? → CTA) isn't decided — affects conversion + rhythm.
18. **NEWSLETTER / email capture.** She liked MOD's "A Welcome Gift" newsletter popup — a soft conversion + future-marketing asset. Include a gentle email capture?
19. **BILINGUAL (EN/AR)?** Dubai market; MOD ran EN+AR. Consider even just an Arabic tagline / contact.
20. **DESIGN MOTIF cohesion.** She likes "bubbles" — pill inclusions (Entry 8) + outline bubble words (Entry 9). Make rounded "bubble" shapes a subtle through-line motif for cohesion.
21. **PRACTICAL (not taste, but required):** reduced-motion fallback + mobile-first (heavy motion), proper page titles/meta (audit found hers broken), favicon, custom domain + go-live, and how the enquiry form actually reaches Benafsha.

---

## Prompt library (Framer AI) — filled in as we go
> _Format: paste one block at a time into Framer AI, review, then iterate. Brand colours/fonts are set as Styles first so the AI stays on-brand._

- [ ] Hero (Entry 1) — draft ready on request
- [ ] Instagram section (Entry 2)
- [ ] Services three-column (Entry 6)
- [ ] Portfolio magazine covers (Entry 7)
- [ ] Check Availability page (Entry 8)
- [ ] Gallery outline marquee (Entry 5 + 9)
- [ ] Scroll reveals across sections (Entry 4)
- [ ] …more as Kriti adds references
> _Blocked on the Open Decisions above — resolve mood + video first._
