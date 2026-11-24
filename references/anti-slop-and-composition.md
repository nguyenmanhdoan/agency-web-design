# Anti-AI-Slop Rules & 12-Pattern Section Composition Catalog

Distilled from **Taste Skill** art-direction principles and adapted strictly for **pure CSS + ACSS + Bricks Builder** (zero Tailwind, zero React/Framer Motion).

## 1. The Anti-AI-Slop Ban List (Hard Violations)

Reject and immediately rewrite any section containing these generic LLM tells:

1. **The Stacked 3-Card Disease:** Putting 3 equal rounded white cards with a centered icon inside a pastel circle (`48px`), a short bold title, and 2 lines of generic text — especially repeating that pattern across two or more sections.
2. **Purple-Blue AI Gradients & Glowing Orbs:** Mesh blobs, neon radial blurs, or purple-to-cyan button gradients on non-gaming/non-AI-hype client sites.
3. **Unrequested "Card Polish":** Wrapping every image, metric, or list item in a `border-radius: 16px` white box with `box-shadow: 0 10px 30px rgba(0,0,0,0.08)` when the approved Archetype calls for sharp edges, flat surfaces, or borderless editorial photography.
4. **Gratuitous Glassmorphism:** Frosted `backdrop-filter: blur()` cards floating over busy photos where contrast drops below `4.5:1`.
5. **Emoji Icons & Mixed Icon Packs:** Using `🚀`, `✨`, `✅` as UI icons, or mixing FontAwesome solid icons with thin outline SVGs. Always use **one single SVG icon family** (e.g., Lucide, Phosphor, or Tabler) with uniform `stroke-width` (`1.5px` or `1.75px`) site-wide.
6. **Center-Aligned Everything:** Defaulting every hero, section header, and card to `text-align: center`. Left-aligned editorial headers with clear horizontal rhythm almost always feel more authoritative and scannable.
7. **Empty Marketing Copy:** Headlines like *"Giải pháp toàn diện cho tương lai số"* or *"Nâng tầm trải nghiệm của bạn"*. Write concrete, domain-specific headlines anchored in real client outcomes, numbers, or craft.

---

## 2. The 12-Pattern Section Composition Catalog

**Mandatory Rhythm Rule:** **Never stack two adjacent sections using the same composition pattern.** Alternate visual weight, column asymmetry, and surface tone (`light` -> `subtle tint` -> `light` -> `dark anchor`) so the page reads with intentional editorial pacing.

| # | Pattern Name | Structural Layout | Best Used For |
| :--- | :--- | :--- | :--- |
| **P1** | **Full-Bleed Atmospheric Hero** | `min-height: 100dvh` full-bleed real photography/video with calibrated dark scrim, bottom-left or asymmetric typographic lockup, 1 primary CTA. | Architecture, Hospitality, Real Estate, Luxury, Studio |
| **P2** | **Asymmetric Split Hero (55/45 or 60/40)** | Left column: Eyebrow + sharp H1 + concise lead + single CTA + micro-proof strip. Right column: High-craft framed visual or UI showcase. | B2B, SaaS, Healthcare, Consulting, Education |
| **P3** | **Editorial Statement / Manifesto Band** | Left 4 cols: small sticky eyebrow/index (`01 / TRIẾT LÝ`). Right 8 cols: oversized typographic statement (`--h2`/`--h3`) + concise 2-col body split below. | Brand story, About intro, Positioning |
| **P4** | **Metrics & Proof Strip (Hairline Grid)** | 3–4 key verifiable numbers separated by vertical `1px` hairlines (`border-inline-start`), tabular numerals (`--h1`), zero card boxes. | Credibility bar, Capacity, Track record |
| **P5** | **Hairline Index Rows (Service / Capability List)** | Full-width horizontal rows separated by `1px` top/bottom borders: `[01]` + `[Title]` + `[Concise description]` + `[Arrow link]`. Subtle hover highlight. | Practice areas, Services, Capabilities, Menu |
| **P6** | **Asymmetric 40/60 Feature Split (Alternating)** | 40% narrative column (eyebrow, title, 2–3 concrete bullet points) paired with 60% large-format media (`4:3` or `16:10`). Flip direction only purposefully. | Deep-dive services, Product craft, Facility tour |
| **P7** | **Hierarchical Bento Grid (Unequal Weights)** | 12-col CSS Grid with **unequal spans** (e.g., 1 hero tile spanning 7 cols + 1 tall 5-col tile, followed by 5 + 7 or 4 + 4 + 4 with distinct visual types). Never 6 identical tiles. | SaaS features, Ecosystem overview, Highlights |
| **P8** | **Editorial Portfolio / Case Study Showcase** | Large borderless `16:10` or `4:3` images with clean metadata row underneath (Category · Location · Year) and concise outcome headline. Staggered 2-col (`60/40` or `50/50`) with generous gap. | Projects, Case Studies, Works, Spaces |
| **P9** | **Sticky Narrative + Scrolling Steps** | Left column (`position: sticky; top: var(--space-xl)`): Section headline & summary. Right column: Numbered process steps (`01`..`05`) with hairline dividers. | Production process, Patient journey, Methodology |
| **P10** | **Dark Anchor Conversion / Proof Band** | High-contrast dark surface (`--bg-dark` + `--text-light`) breaking up light sections; holds either flagship testimonial/case metric or primary consultation CTA. | Mid-page break, Executive quote, Pre-footer CTA |
| **P11** | **Structured Comparison / Spec Table** | Clean semantic `<table>` or CSS grid spec sheet with crisp hairline borders, sticky first column on mobile scroll, zero bloated pricing card fireworks. | B2B specs, Engagement models, Pricing tiers |
| **P12** | **Split Consultation & Form Section** | Left 5 cols: Direct contact info, office address, response SLA, real team contact. Right 7 cols: Clean, accessible form with `>= 44px` inputs and clear primary submit. | Contact page, Bottom-of-funnel RFQ / Booking |

---

## 3. Visual Richness Floor (Anti-Skeleton Mandate)

Never deliver bare, text-only sub-pages or Archive/Single templates. Every page — Homepage, About, Services, Contact, Archive, Single — must meet this baseline:

* **Cohesive Media Direction:** Every image slot uses a deliberate, consistent `aspect-ratio` (`16/9`, `4/3`, `3/4`, `1/1`) matching the approved palette and mood. Never stretch, squash, or mix random unstyled ratios.
* **Structured Micro-Hierarchy:** Every card/row/header includes intentional metadata (eyebrow/category tag, index number, date/location, or concise spec) so pages feel authored, not stripped-down.
* **Single SVG Icon Family:** Uniform `stroke-width` and size scale (`16px` inline, `20px` UI controls, `24px` section accents). Zero emoji placeholders.
* **Tactile Interactive States:** Every link, button, input, and interactive row defines explicit `:hover`, `:focus-visible`, and `:active` states with smooth `150–250ms` transitions respecting `@media (prefers-reduced-motion: reduce)`.
