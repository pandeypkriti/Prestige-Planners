# Framer, Explained Simply — Your Guide to Building the Prestige Planners Landing Page

Hi Kriti. This is your plain-English guide to **Framer**, written specifically for the Prestige Planners job. No coding, no jargon left unexplained. By the end you'll understand what Framer is, how it works, exactly how to build *this* luxury landing page in it, how to make it actually work live, and — importantly — whether you should build it in Framer at all or let me hand-build it for you. Let's go.

Quick reminder of the mission, so everything below stays anchored to it:

> Build **one stunning landing page** for **Prestige Planners** (a solo female luxury wedding/event planner in Dubai) to **wow the client and close the deal**. No CRM, no giant website yet. Just gorgeous + high-converting, with a big **WhatsApp** button (WhatsApp is the #1 way people book in Dubai). Upsell the full site later.

Your brand kit for this project:
- **Colours:** Navy `#002F5F`, Gold `~#C4A24C`, Cream `#F3ECDC` (the three main ones), plus Rust `#903E1F` and Sage `#A4C0AA` as accents.
- **Fonts:** Headlines in *Cofo Raffine Bold* (that one's paid — free web stand-ins are **Fraunces** or **Playfair Display**). Body text in *Museo Sans* (free stand-ins: **Poppins** or **Mulish**).
- **Logo:** the luxury gold serif logo.

---

## 1) What Framer Actually Is

**Framer is a visual, no-code website builder.** "No-code" means you build the site by dragging things around on a screen with your mouse and clicking buttons — you never write code. You design the page and Framer turns it into a real, live website on the internet with its own web address (URL).

Think of it like designing a poster in Canva… except when you hit **Publish**, that poster becomes a real working website anyone in the world can visit.

### How it's different from the tools you may have heard of

**Framer vs Figma.** Figma is a *design-only* tool — it makes beautiful pictures of websites (mockups), but those pictures aren't real websites. You can't give someone a Figma link and have them book a call. Framer looks and feels a lot like Figma to work in, but it actually *publishes a live site*. So Framer = "Figma that goes live."

**Framer vs Wix / Squarespace.** Wix and Squarespace are also no-code builders, and they're fine. But designers reach for Framer because the finished sites simply *look more expensive* — smoother animations, more precise control over spacing and layout, and less of that "I've seen this template before" feeling. For a **luxury** brand like Prestige Planners, that visual polish is the whole point. Wix/Squarespace can feel a bit "small business template." Framer can feel like a high-end agency built it.

### What Framer is genuinely great at
- **Beautiful, custom-looking landing pages** with silky animations — exactly your use case.
- **Fast hosting built in** — the site loads quickly, which matters for conversions.
- **Easy editing later** — you (or the client) can tweak text and images without breaking anything.
- **Reusable** — once you learn it, you can spin up sites for *future* clients much faster.

### Its honest limits
- It's a **subscription** — to connect a real custom domain (like prestigeplanners.ae) you need at least the paid **Basic** plan (about **$10/month**, billed yearly). The free plan only gives you a `something.framer.website` address.
- It's **not** a heavy database/booking-system tool. It's brilliant for beautiful marketing pages (perfect here), less suited to complex apps. For this landing page, that limit doesn't affect you at all.
- There's a **small learning curve**. It's friendly, but it's a new tool. (Section 5 is all about whether that curve is worth it for you — read it.)

---

## 2) How Framer Works — The Beginner's Tour

Here are the only concepts you need. I'll define each one.

**The Canvas.** This is your big workspace — the infinite white area in the middle of the screen where your website lives while you build it. You zoom in and out and move things around here, just like in Figma or Canva.

**Pages.** A website can have multiple pages (Home, About, Contact…). For *this* job you only need **one page** — the landing page. Nice and simple.

**Frames / Sections.** A **frame** is just a box that holds content. Your landing page is a stack of big frames from top to bottom — one for the Hero, one for Portfolio, one for Services, and so on. Framer calls the full-width horizontal bands "**sections**." Mentally: your page = a stack of sections.

**The Insert Menu.** This is your toolbox. You click **Insert** (or press a shortcut) and get a menu of things to drop onto the page: text, images, buttons, forms, embeds, ready-made components, etc. This is how you add basically everything.

**Components.** A **component** is a reusable design element — a button, a card, a testimonial block — that you can drop in repeatedly. Change the "master" once and every copy updates. Framer also has a **Marketplace** full of pre-made components (including ready-to-go WhatsApp buttons — handy for you).

**Styles / Tokens (this is the big time-saver).** A **style** (sometimes called a "token") is a saved setting you name once and reuse everywhere. You create a **Color Style** called "Navy" set to `#002F5F`, and from then on you just pick "Navy" instead of retyping the hex code. Same for fonts via **Text Styles**. **You set your whole brand kit up once as styles, and the entire site stays perfectly consistent.** If the client later says "make the gold slightly warmer," you change it in one place and it updates everywhere. This is the single most important habit — do it first (see Section 3).

**Breakpoints (responsiveness).** A **breakpoint** is a version of your page for a specific screen size. Framer gives you three: **Desktop**, **Tablet**, and **Mobile**. "**Responsive**" just means the site rearranges itself to look great on each. You design Desktop first, then click into Tablet and Mobile to nudge things (usually: make text smaller, stack columns into a single column). In Dubai a huge share of traffic is on phones, so **Mobile has to look flawless** — you'll spend real time here.

**Framer AI (describe-to-build).** Framer has AI helpers where you *type what you want in words* and it builds a starting point:
- **Wireframer** — describe a page ("a luxury wedding planner landing page with a hero, portfolio gallery, and testimonials") and it generates a rough responsive layout you then restyle.
- **Workshop** — describe an interactive piece ("a scroll progress bar," "a tabbed gallery") and it creates that custom element for you, no code.
These give you a fast head-start; you then apply your brand styles on top. Treat AI as the *first draft*, not the finished product.

**Templates.** Pre-built designs you can start from instead of a blank page. There are luxury/wedding/agency templates you could adapt — a legitimate shortcut. Just make sure you restyle it with the brand kit so it doesn't look generic.

**Publish.** The magic button. Click **Publish** and Framer puts your site live on the internet. Free = a `prestige-planners.framer.website` address. Paid = you connect the **custom domain** (her real prestigeplanners.ae) so visitors see her brand, not Framer's. You can re-publish anytime you make changes — it updates in seconds.

---

## 3) Building *This* Landing Page in Framer — Step by Step

Here's the concrete build. Follow it top to bottom.

### Step A — Set up the brand kit first (do this before anything else)
1. Start a new project (blank page, or a luxury template you'll restyle).
2. Open the **Styles / Colors** panel and create **Color Styles**, naming each one:
   - Navy `#002F5F`, Gold `#C4A24C`, Cream `#F3ECDC`, Rust `#903E1F`, Sage `#A4C0AA`.
3. Add your fonts. Framer includes Google Fonts, so add **Fraunces** (or **Playfair Display**) for headlines and **Poppins** (or **Mulish**) for body — these are the free stand-ins for Cofo Raffine and Museo Sans. *(If the client buys the real Cofo Raffine / Museo Sans licences later, you can upload those font files and swap them in.)*
4. Create **Text Styles**: e.g. "Heading XL," "Heading," "Subheading," "Body," "Button" — set each to the right font, size, weight, and colour once.

Doing this first means every section you build afterward is automatically on-brand. **Cream** is likely your main background, **Navy** your main text, **Gold** your accents and buttons.

### Step B — Build the sections (top to bottom)
Insert a full-width **section** frame for each of these:

1. **Hero** (the first thing people see — the most important section).
   - Big headline in your Heading XL style. A luxury promise, not a description. Something like *"Dubai's Most Unforgettable Weddings & Celebrations, Designed Just for You."*
   - One short supporting line underneath.
   - **One** clear button — the **primary call-to-action (CTA)**. A "call-to-action" is the single thing you want visitors to do. Yours is **"Enquire on WhatsApp."** Make it Gold on Navy (or Navy on Cream) so it stands out. *One* CTA only — luxury = focused, not cluttered.
   - Background: a stunning full-width hero image or subtle video of an elegant event.

2. **Portfolio / Gallery.** A grid of gorgeous event photos (weddings, showers, yacht/desert parties, corporate). Use a **Gallery** component from the Insert menu. Big, high-quality images do the selling here — keep captions minimal.

3. **Services.** A short, elegant row of what she offers: Weddings · Bridal Showers · Corporate Events · Yacht & Desert Parties. Icon or small image + a one-line description each. Use **Gold** for the little headings.

4. **Founder Story.** She's a solo female planner — that's a *strength* for luxury clients who want a personal, trusted touch. A portrait photo + a warm short paragraph in her voice. This builds the personal connection that closes high-end bookings.

5. **Testimonials.** Real client quotes (or clearly labelled placeholders until she gives you real ones — never fabricate). Simple quote cards. Social proof is a major conversion driver.

6. **Booking / WhatsApp CTA.** A closing band that repeats the ask: a warm line like *"Let's plan something extraordinary,"* and the big **WhatsApp** button again. This is where you seal the click.

7. **Footer.** Logo, contact details, Instagram link, WhatsApp, a discreet copyright line. Keep it clean and dark (Navy background, Cream/Gold text reads as premium).

### Step C — Add the WhatsApp button (the key conversion element)
The simplest reliable method:
1. Add a **Button** from the Insert menu (or grab a ready-made **WhatsApp Chat Button** from the Framer Marketplace).
2. Set its link to a **click-to-chat URL** in this format:
   `https://wa.me/<number in full international format>`
   Example for a UAE number +971 50 123 4567 → `https://wa.me/971501234567`
3. Optional but recommended — pre-fill a message so the enquiry basically writes itself:
   `https://wa.me/971501234567?text=Hi%20Prestige%20Planners%2C%20I%27d%20love%20to%20enquire%20about%20planning%20my%20event`
   (The `%20` bits are just how spaces are written in a link — Framer or a generator will do this for you.)
4. Style it Gold, make it prominent, and place it in the **Hero** and the **closing CTA**. On mobile, consider a **sticky** WhatsApp button that stays on screen as they scroll.

### Step D — Make it responsive
Switch to the **Tablet** and then **Mobile** breakpoint at the top of the editor. On each, check that text isn't too big, columns **stack into one column**, images still look great, and the WhatsApp button is easy to tap. **Do not skip Mobile** — most Dubai visitors are on phones, and a broken mobile view kills a luxury impression instantly.

### Step E — Add tasteful animation (the luxury feel)
Framer's superpower. Keep it *subtle and elegant* — luxury whispers, it doesn't shout.
- **Fade / rise on scroll:** sections gently fade and slide up as you scroll to them. (Framer calls these scroll/appear effects — you turn them on per element.)
- **Slow gentle zoom** on the hero image.
- **Soft hover** on buttons and portfolio images (a light lift or glow in Gold).
Restraint is the brief. Two or three refined effects beat twenty flashy ones.

### Step F — Add images
- Drag image files straight onto the canvas, or use **Insert → Image**.
- Use **high-resolution** photos — for luxury, image quality *is* the product.
- If she doesn't have professional photos yet, use tasteful high-end stock as placeholders and clearly flag them as temporary. (Never pass off stock as her real work to the client.)

---

## 4) Making It Actually Work (Live + Functional)

You said *"I need it to work."* For a showcase landing page, **"working" means three things:**
1. It's **live** at a real web address anyone can open.
2. It's **mobile-perfect**.
3. The **CTA / WhatsApp / any form actually do something** when clicked.

Here's how each piece works.

**Getting it live (Publish).**
- **Free option:** hit Publish and it goes live at `prestige-planners.framer.website`. Great for *showing the client the draft* to close the deal — costs nothing.
- **Real option:** on the **Basic plan (~$10/month, billed yearly)** you connect a **custom domain** so it lives at her real address (e.g. prestigeplanners.ae or a subdomain). First year of a domain is free on a yearly plan. **Budget for Basic from day one on any paid client work** — a `.framer.website` address looks unfinished to a paying luxury client.

**An enquiry form that actually sends (optional here).** Since there's **no CRM**, you likely don't even need a form — **WhatsApp is the booking channel.** But if you want one: Insert → **Forms**, drag it in, and in the settings set **"Send To" → your email** (submissions land in an inbox) or a **webhook** (a webhook is just a link that hands the form data to another tool like a Google Sheet or Zapier). Keep it lightweight: name, event type, date, WhatsApp number. That's it.

**Built-in booking (if she ever wants scheduled calls).** Framer has a **Calendly** integration — Calendly is a free tool that lets people book a time slot from her calendar. You drop it in via an **Embed** (an Embed is a component that displays another tool inside your page). Nice for consultations later; **not needed for v1** — WhatsApp covers it.

**How the WhatsApp button "works."** It's just a special link (Section 3C). Tapping it opens WhatsApp — app on mobile, WhatsApp Web on desktop — with a chat to her number already open and your pre-filled message ready to send. Nothing to install, nothing to maintain. This is genuinely the most reliable "it works" element on the whole page.

**Meta Pixel — later, not now.** A "Meta Pixel" is a tiny snippet of tracking code from Facebook/Instagram that measures who visits and lets her run retargeting ads. Framer supports adding it via **custom code / site settings on the Pro plan**. Because there's **no CRM and no ad spend yet**, **skip it for v1.** Note it as a future upsell ("later I can add ad tracking so we can run Instagram campaigns"). Keeps v1 clean and cheap.

**Bottom line on "working":** For this project, "working" = published live, flawless on mobile, and the WhatsApp button reliably opens a chat. Everything else is optional polish you can upsell later.

---

## 5) Framer vs "Claude Design" — The Real Decision (read this carefully)

There are two honest ways to build the *real, final* page. Let me lay both out plainly, then give you a straight recommendation.

### Option A — **Framer** (you build it visually, I guide design + copy)
You assemble the page yourself in Framer, and I hand you the layout, the words, the colour/spacing decisions, and step-by-step direction.
- **Upsides:** You have full control in a friendly editor. **You can edit it yourself forever** — change a photo, a price, a headline — without needing me. You **learn a skill you'll reuse on every future client**, and you can build faster each time. The client can even be handed simple editing rights.
- **Downsides:** You have to **learn Framer and do the assembly** (a real few hours the first time). It's a subscription (~$10/month).

### Option B — **"Claude Design"** (I hand-build the page in code for you)
Here, *I* write the actual website code (HTML/CSS — the raw language browsers read) and produce a finished, pixel-perfect page. It gets hosted live for free on a service like **Netlify, Vercel, or GitHub Pages** (these take a folder of code and put it online at a real URL).
- **Upsides:** **Fast** and **pixel-precise** — I control every detail exactly. **No tool for you to learn.** Could be free to host.
- **Downsides:** **You can't easily edit it yourself.** Every change ("swap this photo," "change the price") means coming back to me or touching code you're not comfortable with. For a **non-technical owner who wants to maintain and reuse** this, that's a real long-term handicap. It's a great *sprint*, a poor *foundation*.

### My honest recommendation for *your* situation

Your two goals pull in slightly different directions:
1. **Close the deal fast** — get something gorgeous in front of the client *now*.
2. **Own, edit, and reuse it** — you're a non-technical freelancer building a *repeatable side business*, not a one-off.

Goal 1 favours speed (Option B). Goal 2 strongly favours Framer (Option A). So use a **hybrid — and this is my primary recommendation:**

> **Recommended path: "Fast draft to close, then build the real thing in Framer."**
>
> 1. **To win the deal quickly:** I build you a **fast live HTML draft** (Option B) and publish it free (Netlify/GitHub Pages) so you can show the client a real, beautiful, working page within a day. This is your *sales tool* — it wows them and closes the deal with almost no effort from you.
> 2. **As the paid deliverable:** you rebuild it properly in **Framer** (Option A), with my design + copy guidance. **This** is what you actually hand over and get paid for — because *you can maintain it, the client can be given editing access, and you can reuse the whole approach for the next Dubai client.*

**Why this order wins:** you get the *speed* of code for the sales pitch and the *ownership + reusability* of Framer for the real product. You're not betting your business on a page only I can touch.

**A cleaner variation** if you'd rather skip the code step entirely: **I design the page in Figma → you import/rebuild it in Framer.** (Framer can bring in Figma designs, and I can produce the Figma design for you.) That keeps everything in the visual, no-code world you prefer, start to finish. If the idea of *any* code — even a temporary draft — makes you uneasy, **take this variation instead:** Figma design from me → Framer build by you.

**One-line answer:** Build the **final page in Framer** (that's your maintainable, reusable, sellable asset). Optionally let me produce a **fast draft** (live HTML *or* a Figma design) purely to wow the client and close fast. Framer is the home; the draft is just the hook.

---

## 6) Your Simple Build Plan / Checklist (zero → live)

Rough times are for a **first-timer** — you'll get much faster on client #2.

**Phase 0 — Close the deal (½–1 day)**
- [ ] Ask me for a **fast draft** (live HTML page *or* a Figma design) to show the client. *(15–30 min of your time; I do the building.)*
- [ ] Show the client, get the yes. ✅

**Phase 1 — Set up (about 1 hour)**
- [ ] Create a free **Framer** account and a new project.
- [ ] Build the **brand kit as styles**: Navy/Gold/Cream/Rust/Sage + Fraunces & Poppins text styles. *(Section 3A — do NOT skip.)*

**Phase 2 — Build the page (3–5 hours)**
- [ ] Hero (headline + one WhatsApp CTA + hero image) — *~45 min*
- [ ] Portfolio gallery — *~45 min*
- [ ] Services row — *~30 min*
- [ ] Founder story — *~30 min*
- [ ] Testimonials — *~30 min*
- [ ] Closing WhatsApp CTA band — *~20 min*
- [ ] Footer — *~20 min*

**Phase 3 — Make it work + shine (2–3 hours)**
- [ ] Add the **WhatsApp click-to-chat** link (her real number). *~20 min*
- [ ] Add **subtle scroll/hover animations**. *~45 min*
- [ ] Fix **Tablet** then **Mobile** breakpoints — get mobile perfect. *~1 hour*
- [ ] Drop in **high-res images** (real or clearly-flagged placeholder). *~30 min*

**Phase 4 — Go live (½–1 hour)**
- [ ] **Publish** to the free `.framer.website` link and test on your phone. *~15 min*
- [ ] Upgrade to **Basic (~$10/mo yearly)** and connect the **custom domain**. *~30 min*
- [ ] Final test: page loads live ✅, mobile is flawless ✅, WhatsApp button opens a chat ✅.

**Later upsells (note, don't build now):** full multi-page website, enquiry form to email, Calendly booking, Meta Pixel + Instagram ad tracking, real professional photography.

**Total for a beginner:** roughly **1.5–2 focused days** for the Framer build. The deal-closing draft can be in the client's hands **within a day.**

---

### The one thing to remember
Set up your **brand styles first**, keep it **elegant and uncluttered**, make the **WhatsApp button impossible to miss**, and obsess over **mobile**. Do those four things and you'll have a page that looks like a high-end agency made it — and a repeatable playbook for every Dubai client after this one. You've got this. 💛

---
*Sources: [Framer](https://www.framer.com/) · [Framer AI](https://www.framer.com/ai/) · [Framer Pricing](https://www.framer.com/pricing) · [Framer Forms + Webhooks](https://www.framer.com/help/articles/framer-form-webhook-setup/) · [Adding a contact form](https://www.framer.com/help/articles/how-can-i-add-a-contact-form-to-my-framer-website/) · [Framer custom domains](https://www.framer.com/domains/) · [WhatsApp click-to-chat button in Framer](https://designchillout.co/resources/how-to-add-a-whatsapp-click-to-chat-button-to-your-framer-site) · [Framer Review 2026](https://effloow.com/articles/framer-review-ai-website-builder-guide-2026)*
