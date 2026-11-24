# Multi-Industry Design Intelligence & 6 Agency Visual Archetypes

Distilled from structured multi-industry design systems (UI/UX Pro Max methodology) and calibrated for **agency client websites** built on pure CSS + ACSS + Bricks Builder.

## 1. The 6 Agency Visual Archetypes

Every client brief maps first to **one primary Archetype** (establishing the agency's craft baseline), then adapts using the **Industry Matrix** below.

| Archetype | 3 Dials (Var / Mot / Den) | Visual Grammar & Signature | Radius / Surface Rules | Ideal Sectors |
| :--- | :--- | :--- | :--- | :--- |
| **1. Swiss Corporate (Trust-First B2B)** | `3 / 2 / 5` | Disciplined 12-col grid, hairline dividers (`1px`), crisp data tables, muted high-contrast surfaces, authoritative sans typography. | `0px` or `2px–4px` sharp edges; flat surfaces, zero heavy shadows. | Manufacturing, Engineering, Logistics, Industrial B2B, Law, Finance |
| **2. Editorial Luxury (Gallery & Craft)** | `8 / 4 / 2` | Generous whitespace, dramatic Serif + clean Sans contrast, full-bleed or asymmetric photography, quiet muted neutrals, minimal UI chrome. | `0px` borderless media; no card boxes around photos; subtle tonal shifts. | Architecture, Interior Design, Luxury Real Estate, Boutique Hospitality, Fashion |
| **3. Modern Conversion (High-Clarity Growth)** | `6 / 5 / 4` | Strong value-proposition hero, structured bento/split feature bands, high-contrast single accent CTA, crisp social proof & comparison tables. | `8px–12px` intentional radius; subtle `1px` border on light surfaces; restrained elevation. | SaaS, B2B Services, Digital Agencies, EdTech, Consulting |
| **4. Clean Clinical (Calm Authority)** | `4 / 2 / 4` | Airy warm-white/sage/slate surfaces, high readability, reassuring human photography, clear step-by-step process & credentials. | `6px–10px` soft edges; zero harsh black (`#000`), use deep slate/charcoal text. | Healthcare, Dental Clinics, Aesthetics/Derm, Wellness, Education |
| **5. Bold Studio (Expressive Identity)** | `9 / 7 / 3` | Oversized display typography, stark light/dark section contrast, editorial marquee/strips, kinetic hover states, strong art direction. | Deliberate contrast (`0px` brutalist or `16px+` pill/editorial); bold accent blocks. | Creative Studios, F&B Brands, Events, Consumer Lifestyle, Entertainment |
| **6. Modular Commerce (Catalog & DTC)** | `5 / 4 / 6` | High-scanability product grids, consistent aspect-ratio frames, sticky filter/summary bars, trust badges, clear pricing hierarchy. | `0px–6px` consistent media frames; neutral studio backdrop (`#F6F6F4`) behind products. | E-commerce, Retail Brands, Furniture Catalogs, Cosmetics, Specialty Food |

---

## 2. 12-Industry Design Blueprint Matrix

Before designing any template, locate the client's sector below and apply its **Section Flow, Color Psychology, Proof Signals, and Industry Anti-Patterns**.

### 2.1. B2B Manufacturing, Industrial & Engineering
* **Default Archetype:** Swiss Corporate (`3 / 2 / 5`) · **Surface Mode:** `Persuade`
* **Color Psychology:** Deep Navy / Steel Slate (`--primary`), Industrial Amber or Safety Blue (`--accent`), Cool Concrete Neutral (`--neutral`).
* **Recommended Section Flow:** Hero (facility/product photography + key capability metrics) -> Trust/Certification Bar (ISO, capacity numbers) -> Core Capabilities (asymmetric split or spec-grid, NOT icon circles) -> Featured Projects / Case Studies -> Production Process / QA Standards -> Technical Download / RFQ Form CTA.
* **Industry Anti-Patterns:** Abstract 3D floating blobs, stock handshake photos, playful pastel colors, vague slogans without capacity/tolerance/ISO numbers.

### 2.2. Architecture, Interior Design & Construction
* **Default Archetype:** Editorial Luxury (`8 / 4 / 2`) · **Surface Mode:** `Experience`
* **Color Psychology:** Warm Stone / Alabaster (`--base`), Charcoal / Espresso (`--text-dark`), Terracotta / Brushed Bronze / Olive (`--accent`).
* **Recommended Section Flow:** Full-bleed Architectural Hero (`100dvh`, minimal caption) -> Philosophy / Studio Statement (typographic split) -> Selected Works (asymmetric editorial gallery with project metadata: location, area m², year) -> Design-Build Process (numbered horizontal or sticky list) -> Materiality / Craft Proof -> Private Consultation CTA.
* **Industry Anti-Patterns:** Heavy borders/shadows around project photos, cramped 4-column grids that shrink photography, loud neon CTAs, cluttered floating chat widgets covering imagery.

### 2.3. Healthcare, Dental & Medical Clinics
* **Default Archetype:** Clean Clinical (`4 / 2 / 4`) · **Surface Mode:** `Persuade`
* **Color Psychology:** Crisp Ivory / Soft Mist (`--base`), Deep Teal / Medical Navy (`--primary`), Warm Sand or Sage (`--secondary`).
* **Recommended Section Flow:** Reassuring Hero (real clinic/doctor imagery + clear booking CTA) -> Credentials & Equipment Proof -> Key Treatments (scannable tabbed or structured list with outcomes) -> Doctor Team (real portraits, qualifications, years of experience) -> Patient Journey / Sterilization Standards -> Verified Reviews & Location/Booking Band.
* **Industry Anti-Patterns:** Cold sterile pure `#FFFFFF` + `#00FF00` hospital clichés, aggressive red urgency banners, tiny body text (`< 16px`), unverified generic stock smiles.

### 2.4. Real Estate & Property Development
* **Default Archetype:** Editorial Luxury or Swiss Corporate (`6 / 4 / 3`) · **Surface Mode:** `Experience` / `Persuade`
* **Color Psychology:** Deep Forest / Midnight Navy (`--primary`), Warm Champagne Gold / Sand (`--accent`), Warm Off-White (`--base`).
* **Recommended Section Flow:** Atmospheric Hero (architectural render/aerial + location tag) -> Key Project Metrics (scale, handover, legal status) -> Masterplan / Location Connectivity (split map + travel times) -> Product/Unit Types (structured tabs + floorplan specs) -> Amenities Editorial Strip -> Developer Track Record -> Consultation / Brochure Form.
* **Industry Anti-Patterns:** Overloaded popups, low-contrast gold text on white backgrounds (fails `4.5:1`), walls of unformatted legal text, inconsistent photo aspect ratios.

### 2.5. Law, Finance, Accounting & B2B Consulting
* **Default Archetype:** Swiss Corporate (`3 / 2 / 5`) · **Surface Mode:** `Read` / `Persuade`
* **Color Psychology:** Oxford Navy / Deep Charcoal (`--primary`), Burgundy / Muted Brass / Slate Blue (`--accent`), Paper White (`--base`).
* **Recommended Section Flow:** Authoritative Hero (clear specialization + direct consultation CTA) -> Practice Areas (clean hairline-divided index, zero cartoon icons) -> Representative Outcomes / Client Sectors -> Leadership / Partners (editorial portraits + bar/license credentials) -> Insights / Legal Updates (clean editorial list) -> Confidential Inquiry Form.
* **Industry Anti-Patterns:** Startup gradients, quirky illustrations, playful rounded pill badges everywhere, hiding phone/office/credentials deep in the footer.

### 2.6. SaaS, Software & Tech Services
* **Default Archetype:** Modern Conversion (`6 / 5 / 4`) · **Surface Mode:** `Persuade`
* **Color Psychology:** High-contrast Ink/Slate (`--text-dark`), Crisp Neutral Surface (`--base`), 1 disciplined Electric Blue / Emerald / Indigo (`--primary`).
* **Recommended Section Flow:** Value-Prop Hero (headline + crisp UI product visual + single primary CTA) -> Customer Logo Strip -> Problem vs. Outcome Contrast -> Core Capabilities (hierarchical Bento or alternating 40/60 UI splits) -> Integration / Architecture Proof -> Transparent Pricing or Engagement Models -> FAQ -> Final Demo CTA.
* **Industry Anti-Patterns:** Purple-to-pink glowing mesh gradients, fake 3D isometric illustrations, 6 identical feature cards in a 3x2 grid with generic Lucide icons inside tinted circles.

### 2.7. Education, Academies & Training Centers
* **Default Archetype:** Modern Conversion or Clean Clinical (`5 / 4 / 4`) · **Surface Mode:** `Persuade`
* **Color Psychology:** Royal Navy / Deep Indigo (`--primary`), Warm Ochre / Amber (`--accent`), Clean Light Warm Neutral (`--base`).
* **Recommended Section Flow:** Outcome-Focused Hero (student/classroom authenticity + enrollment CTA) -> Measurable Outcomes (graduation/placement/score metrics) -> Programs / Curriculum Overview (filterable or structured cards with duration & level) -> Instructors / Mentors -> Student Projects / Testimonials -> Admissions Process -> Consultation Form.
* **Industry Anti-Patterns:** Cluttered rainbow colors per card, overly childish clip-art on adult/professional courses, hiding tuition/schedule/syllabus structure.

### 2.8. F&B, Restaurants, Cafes & Hospitality
* **Default Archetype:** Bold Studio or Editorial Luxury (`8 / 6 / 3`) · **Surface Mode:** `Experience`
* **Color Psychology:** Rich Espresso / Forest / Terracotta / Deep Burgundy (`--primary`), Warm Cream (`--base`), Organic Accent (`--accent`).
* **Recommended Section Flow:** Sensory Full-Bleed Hero (signature dish/space photography + Reserve/Order CTA) -> Brand Story & Ingredients (asymmetric photo + editorial note) -> Curated Menu Highlights (clean typographic menu layout — not clunky e-commerce cards) -> Space & Ambience Gallery -> Locations, Hours & Reservation Block.
* **Industry Anti-Patterns:** PDF-only unreadable menus on mobile, cold corporate blue palettes, sterile white boxes around moody food photography, tiny reservation buttons.

### 2.9. Beauty, Spa, Aesthetics & Wellness
* **Default Archetype:** Editorial Luxury or Clean Clinical (`7 / 4 / 2`) · **Surface Mode:** `Experience` / `Persuade`
* **Color Psychology:** Warm Linen / Blush Stone / Soft Oat (`--base`), Deep Plum / Olive / Espresso (`--primary`), Muted Rose-Bronze (`--accent`).
* **Recommended Section Flow:** Serene Hero (high-craft editorial visual + Book Appointment CTA) -> Signature Rituals / Treatments (typographic list with duration & benefits) -> Space & Philosophy -> Specialists & Hygiene/Product Standards -> Client Transformations / Reviews -> Direct Booking Section.
* **Industry Anti-Patterns:** Oversaturated hot pink gradients, cluttered discount banners, cheap stock spa-stone photos, unreadable thin script fonts for body text.

### 2.10. E-commerce, DTC & Product Catalogs
* **Default Archetype:** Modular Commerce (`5 / 4 / 6`) · **Surface Mode:** `Persuade` / `Operate`
* **Color Psychology:** Studio Neutral (`#F6F6F4` / `#FFFFFF`) letting product photography carry color, high-contrast Ink (`--text-dark`), 1 clear Action Accent (`--primary`).
* **Recommended Section Flow:** Editorial Campaign Hero -> Category Navigation Strip -> Featured / Bestseller Grid (strict uniform aspect ratio, clear price + quick spec) -> Product Craft / Material Story Split -> Social Proof / UGC Gallery -> Shipping, Warranty & Return Policy Bar -> Newsletter Capture.
* **Industry Anti-Patterns:** Mismatched product photo ratios, distracting colored backgrounds fighting product colors, weak price/CTA hierarchy, unclickable card surfaces.

### 2.11. Creative Agency, Production & Digital Studio
* **Default Archetype:** Bold Studio (`9 / 7 / 3`) · **Surface Mode:** `Experience`
* **Color Psychology:** Stark Monochrome (Off-Black `#0F1115` + Chalk `#F7F7F5`) + 1 razor-sharp Signal Accent (Vermilion, Cobalt, Acid Lime, or Cobalt Blue).
* **Recommended Section Flow:** Typographic / Showreel Hero -> Selected Case Studies (large-format alternating aspect ratios with discipline tags & results) -> Capabilities Index (clean horizontal rows) -> Approach / Manifesto -> Client Roster -> Direct Project Inquiry.
* **Industry Anti-Patterns:** Over-animated scroll hijacking that breaks usability, unreadable low-contrast gray-on-black text, generic "We are a full-service digital agency" copy.

### 2.12. Logistics, Supply Chain & Enterprise Operations
* **Default Archetype:** Swiss Corporate (`3 / 2 / 5`) · **Surface Mode:** `Persuade` / `Operate`
* **Color Psychology:** Deep Maritime Blue / Slate (`--primary`), Signal Orange / Teal (`--accent`), Light Industrial Gray (`--neutral`).
* **Recommended Section Flow:** Operational Hero (fleet/port/warehouse photography + Quote / Track CTA) -> Network & Volume Metrics -> Service Lines (Freight, Warehousing, Customs — structured grid with clear specs) -> Coverage Map / Corridor Highlights -> Compliance & SLA Guarantees -> B2B Quote Request Form.
* **Industry Anti-Patterns:** Decorative playful rounded cards, stock globe illustrations from 2010, burying tracking/quote entry points below the fold.
