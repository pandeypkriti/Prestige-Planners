# Prestige Planners — Master Brief & Build Plan
_Meta-ads landing page + Calendly booking + CRM with workflows_
_Prepared for Kriti · Stack: **Framer (UI) + Claude (functionality) + Make.com (CRM workflows)**_

---

## 0. TL;DR (read this first)

- **Client:** Prestige Planners — a solo luxury event/wedding planner in Dubai. She already has a site (`prestigeplanners.ae`) but it's a *brochure, not a booking machine*.
- **Your job:** a Meta-ads landing page that takes an Instagram ad-clicker → booked consultation in under 60 seconds, with every lead tracked in a CRM so none slip away.
- **Build split:** **Framer** builds the beautiful on-brand page. **Claude** builds the functionality (copy, layout spec, code embeds, tracking, and the CRM automations). **Make.com** is the glue that runs the CRM workflows.
- **Cost:** ~**$30–55/month** all-in (Framer Pro $30 + HubSpot free + Make free/$9 + Calendly free/$10). Cheaper build works too (Framer Basic $10) — see §5.
- **Pitch line:** _"You've built a beautiful brand — but your site is a brochure, not a booking machine. I'll turn it into a page that converts Instagram ads into booked consultations, with every lead tracked so none slip away."_

---

## 1. The Brand Kit (decoded from her guidelines)

A genuinely luxury system — navy + gold + cream is the timeless "expensive" combo.

### Colours
| Role | Colour | Hex | Use for |
|---|---|---|---|
| Primary | Navy | `#002F5F` | Backgrounds, headers, text on cream |
| Primary | Gold (metallic) | `#C4A24C` | Buttons, accents, the logo, shimmer |
| Primary | Cream | `#F3ECDC` | Page background, breathing room |
| Secondary | Rust | `#903E1F` | Warm accent, small highlights |
| Secondary | Sage | `#A4C0AA` | Soft accent, dividers |

### Fonts
- **Headlines:** *Cofo Raffine Bold* (high-fashion display serif)
- **Body / subheads:** *Museo Sans* (300 / 500 / 700 / 900), *Acumin Variable* as alt
- **⚠️ Both are paid.** Free web substitutes that look near-identical: **Fraunces** or **Playfair Display** (serif) + **Poppins** or **Mulish** (body). These load fast and cost nothing.

### Logo
Gold serif "Prestige" with an elegant swash + "PLANNERS" spaced in caps. Reads premium. Sits beautifully on navy or cream.
_Files: `~/Downloads/prestige brand guidelines.pdf` and `~/Downloads/Prestige final logo jpeg .jpg.jpeg`_

---

## 2. The Company Dossier

**Confirmed identity:** `prestigeplanners.ae` · IG [@prestigeplannersuae](https://www.instagram.com/prestigeplannersuae/) · WhatsApp +971 50 911 8505 · email contact@prestigeplanners.ae · Meydan Grandstand, Dubai.
_Ruled out name-clashes: @prestigeweddings (different company) and "Melle Prestige" (bills in USD)._
**To get from her:** her own name — it appears nowhere online, and it's central to the pitch.

### Services
Weddings · engagements · showers · gender reveals · birthdays · corporate · yacht & desert parties. Broad "we do every occasion" menu. **No packages or prices published.**

### Positioning today
Aspirational-luxury copy ("bespoke, timeless, exclusive") but **generic and unproven** — she claims the same space as established players with no proof to back it. Early-stage online presence (small following, new FB page, no TikTok).

---

## 3. The Pitch — Gaps to Sell Against (all honest & specific)

1. **No portfolio gallery** — luxury clients buy with their eyes. *Biggest gap.*
2. **No booking flow** — just a basic contact form; no "book a free consultation."
3. **WhatsApp buried** — in the UAE a floating WhatsApp button is the #1 booking channel. Hers isn't prominent.
4. **Founder invisible** — solo-founder brands win on a face + story. Every strong competitor names their founder; she hides.
5. **Thin social proof** — few testimonials, no awards/press.
6. **No single clear CTA** — the page pulls three directions.
7. **Running zero ads** — 100% organic, which is tiny. A landing page is the *prerequisite* before she spends on Meta.

### What "good" looks like in Dubai (benchmark)
| Competitor | Does well |
|---|---|
| [Couture Events](https://coutureeventsworldwide.com/) | WhatsApp-first + free consultation; blue-chip client logos (Emirates, Vogue, Bulgari) |
| [JAM Wedding Planner](https://www.jamweddingplanner.com/) | Multi-path lead capture, free-consultation CTA, named testimonials, award badges |
| [Vivaah Celebrations](https://www.vivaahcelebrations.com/) | Deep portfolio case studies + awards wall + founder-led |

**Winning formula:** named founder story + real portfolio + awards/logo proof + WhatsApp-first free-consultation CTA. Several big names *still* have clunky booking — so a smooth booking funnel is a genuine edge.

### What Dubai luxury clients expect from a booking page
Visual proof first · WhatsApp as primary CTA · a "book a free consultation" path that qualifies the lead · trust signals (founder face, named testimonials, awards) · elegant + flawless on mobile · clear service scope.

---

## 4. How We Build It — Framer (UI) + Claude (Functionality)

A clean split that produces a *nicer* result than an all-in-one builder for a luxury brand.

### Framer handles the UI (its strength)
- The beautiful on-brand page (navy/gold/cream, serif headlines, smooth scroll)
- Auto mobile-responsive
- Publishing live + connecting the domain (**free custom domain since Jan 2026**)
- **Built-in Calendly component** (Insert menu — no code) and **native HubSpot form integration**
- **Custom code** (Meta Pixel in `<head>`) — a **Pro-plan** feature

### Claude ("Claude design") handles functionality
- All **copy**, on-brand + Meta-ad-optimized
- Full **page structure / wireframe** — can be designed in **Figma** and imported straight into Framer (Figma→Framer)
- **Code embeds** you paste into Framer: Calendly, floating **WhatsApp button**, **Meta Pixel + "Lead" event**, form→webhook
- The **backend logic + CRM workflows** in Make.com (see §7)
- Click-by-click Framer instructions

### Honest limitation
Claude has direct connectors to **Figma, Lovable, Higgsfield — but not Framer.** So Claude can't click inside your Framer canvas. Instead Claude hands you ready-to-paste design/copy/code, or designs in **Figma → you import to Framer** (smoothest path).

### Build order
1. Confirm she owns the **domain** login (or use a free `.framer.website` URL to start).
2. **Design** the page (Claude → Figma or a written wireframe + copy).
3. **Build in Framer** — sections: Hero + CTA · Portfolio gallery · Services · Founder story · Testimonials · Booking (Calendly) · Footer with WhatsApp.
4. **Add the Calendly component** (built-in) to the booking section + a floating **WhatsApp** button.
5. **Install Meta Pixel** in Framer custom code (`<head>`) and fire a **Lead** event on form submit (needs Framer **Pro**).
6. **Connect the form** → Framer webhook → Make.com (or native HubSpot integration for the simple push).
7. **Publish** + connect the custom domain; verify domain in Meta.
8. **Build the CRM workflows** in Make.com (§7).
9. **Test end-to-end** with a fake lead + fake booking.
10. Hand over **ad creative** made in Higgsfield (images/short video).

---

## 5. The Stack & Costs

| Job | Tool | Cost |
|---|---|---|
| Landing page UI | **Framer Pro** (custom code for Pixel) | $30/mo ($45 if monthly) |
| Booking | **Calendly** (built into Framer) | Free–$10/mo |
| CRM | **HubSpot Free** | $0 |
| Workflow glue | **Make.com** (Free → Core) | $0–9/mo |
| Ad tracking | **Meta Pixel + Conversions API** | $0 |
| Ad creative | **Higgsfield** | usage-based |
| Domain | she likely owns `prestigeplanners.ae` | ~$12/yr |

**≈ $30–55/month.**

**Cheaper build:** **Framer Basic ($10/mo)** gets custom domain + unlimited forms, but **not** site-wide custom code — install the Pixel via an Embed component or rely on **server-side CAPI through Make** instead. Total then ≈ **$10–20/mo**.

_Framer pricing: [framer.com/pricing](https://www.framer.com/pricing) · [Framer pricing 2026 breakdown](https://www.nocode.mba/articles/framer-pricing)_

---

## 6. What Makes a Meta-Ads Page Convert

Someone tapped your ad mid-scroll with 3 seconds of patience. The page must do **one** job fast:

1. **One goal, one button** — "Book a free consultation." No menus, no distractions.
2. **Message match** — the page headline echoes the ad ("Luxury Weddings in Dubai"). Mismatch = bounce.
3. **Mobile-first** — nearly all Meta traffic is phones.
4. **Fast load** — under ~2–3s; keep images light.
5. **Hero + CTA above the fold** — headline + subhead + button visible without scrolling.
6. **Social proof** — portfolio photos, named testimonials, logos.
7. **Short form** — name, email, phone, event type/date. Every extra field loses people.
8. **Tracking** — Meta **Pixel** + **Conversions API (CAPI)**. Meta recommends BOTH in 2026; there's now near one-click CAPI setup in Events Manager. Capture the hidden `fbclid` tag with each lead so ads get credited correctly.

_Meta tracking refs: [Conversions API guide](https://www.dataally.ai/blog/how-to-set-up-meta-conversions-api) · [Pixel + CAPI 2026 updates](https://segwise.ai/blog/meta-pixel-conversions-api-ai-updates-2026)_

---

## 7. The CRM + Its Workflows (the automation core)

**CRM in plain terms:** the business's memory. Every form submission becomes a contact card that moves along a pipeline. **HubSpot Free** is the recommended CRM (genuinely free, easy, unlimited contacts).

### The pipeline (contact stages)
`New Lead → Contacted → Consultation Booked → Proposal Sent → Won / Lost`

### The workflows (built in Make.com — the "glue")
Make.com watches for an event, then runs steps automatically. The four Prestige needs:

**Workflow 1 — New lead capture**
`Trigger:` Framer form submitted (via webhook) →
`Actions:` create HubSpot contact (stage = New Lead) · store event type/date/budget + the `fbclid` · email the planner an alert.

**Workflow 2 — Instant response (the UAE money-maker)**
`Trigger:` new lead created →
`Actions:` send the planner an instant **WhatsApp/SMS** ("New lead: Sarah — wedding — June, budget X") · send the lead an **auto-reply** ("Thank you — Prestige Planners will reach out within the hour").
_Speed-to-lead is the single biggest conversion lever._

**Workflow 3 — Booking made**
`Trigger:` Calendly consultation booked →
`Actions:` move HubSpot contact to **Consultation Booked** · add to the planner's calendar · schedule reminder(s) to reduce no-shows · fire Meta **Lead**/booking event (with `fbclid`) so the ad gets credited.

**Workflow 4 — After the call**
`Trigger:` consultation status = complete (or +1 day) →
`Actions:` if won → move to **Proposal Sent** + task to send proposal; if no-show → send a friendly re-book link. After the event → auto-request a Google review + testimonial (fixes her social-proof gap).

**Glue tool:** **Make.com** (recommended — generous free tier, multi-step, cheap to scale) or **Zapier** (slightly simpler, pricier). Framer forms POST JSON to a webhook, so both plug in cleanly.

_Refs: [Framer form → webhook](https://www.framer.com/help/articles/framer-form-webhook-setup/) · [Make vs Zapier 2026](https://www.softr.io/blog/make-vs-zapier)_

---

## 8. What Claude Still Needs From You

1. **Her name + a photo/short bio** — the founder story anchors the whole page.
2. **What "ng2" is** — couldn't find any file by that name.
3. **Real event photos** — to fill the portfolio (the #1 gap), or confirm she's pre-first-client.
4. **Domain login** for `prestigeplanners.ae` (to connect the live page).
5. **Her budget / what she's paying you** — to pick the $10–20 vs $30–55 build.

---

## 9. Sources
- Company: [prestigeplanners.ae](https://prestigeplanners.ae/) · [Linktree](https://linktr.ee/prestigeplanners) · [@prestigeplannersuae](https://www.instagram.com/prestigeplannersuae/)
- Competitors: [Couture Events](https://coutureeventsworldwide.com/) · [JAM](https://www.jamweddingplanner.com/) · [Vivaah](https://www.vivaahcelebrations.com/)
- Framer: [pricing](https://www.framer.com/pricing) · [pricing 2026](https://www.nocode.mba/articles/framer-pricing) · [form webhook](https://www.framer.com/help/articles/framer-form-webhook-setup/) · [Calendly on Framer](https://www.storylane.io/tutorials/framer-calendly-integration)
- Automation & tracking: [Make vs Zapier](https://www.softr.io/blog/make-vs-zapier) · [Meta CAPI](https://www.dataally.ai/blog/how-to-set-up-meta-conversions-api) · [Pixel+CAPI 2026](https://segwise.ai/blog/meta-pixel-conversions-api-ai-updates-2026)
