# Vietnamese-Safe Typography, ACSS Fluid Scales & 60-30-10 Color System

Agency typography and color rules engineered specifically for **Vietnamese + English bilingual websites** running on **Automatic.css (ACSS)** and **Bricks Builder**.

## 1. Verified Vietnamese-Safe Font Pairings

Never pick a display or serif font without verifying full Vietnamese diacritic support (`ă, â, đ, ê, ô, ơ, ư` plus stacked acute/grave/hook/tilde/dot marks). Broken diacritics instantly destroy agency credibility.

| Archetype / Vibe | Heading Font (`--font-heading`) | Body Font (`--font-body`) | Why It Works |
| :--- | :--- | :--- | :--- |
| **Swiss Corporate / B2B** | `Be Vietnam Pro` (600–700) | `Be Vietnam Pro` (400–500) | Native Vietnamese optical design; crisp diacritics at all weights; zero fallback jitter. |
| **Modern Conversion / SaaS** | `Plus Jakarta Sans` (600–700) | `Be Vietnam Pro` or `Inter` (400–500) | Geometric modern character in headings with rock-solid Vietnamese body legibility. |
| **Editorial Luxury / Architecture** | `Cormorant Garamond` or `Playfair Display` (500–600) | `Be Vietnam Pro` (400) | High-fashion editorial serif contrast paired with ultra-clean Vietnamese sans body. |
| **Authoritative Editorial / Law & Finance** | `Newsreader` or `Lora` (500–600) | `IBM Plex Sans` or `Be Vietnam Pro` (400) | Calm intellectual serif authority; excellent legibility for long-form Vietnamese reading. |
| **Bold Studio / Creative / F&B** | `Bricolage Grotesque` or `Space Grotesk` (600–700) | `Be Vietnam Pro` (400–500) | Expressive, distinctive display personality without sacrificing body readability. |
| **Clean Clinical / Education** | `Lexend` (500–600) | `Source Sans 3` or `Be Vietnam Pro` (400) | Scientifically optimized reading fluency and calm, approachable geometry. |
| **Technical / Engineering / Data** | `IBM Plex Sans` (600) + `IBM Plex Mono` (labels/metrics) | `IBM Plex Sans` (400) | Precision industrial feel; tabular numerals (`font-variant-numeric: tabular-nums`) for specs. |

### Typography Craft Rules
* **Max 2 Font Families** (plus optional `monospace` solely for technical labels, eyebrows, or numeric specs).
* **Tight Display Tracking:** Large headings (`--h1`, `--h2`) use slight negative tracking (`letter-spacing: -0.025em` to `-0.015em`) and tight leading (`line-height: 1.08` to `1.18`).
* **Vietnamese Diacritic Breathing Room:** Never set `line-height` below `1.08` on uppercase Vietnamese headings (stacked accents like `Ế`, `Ổ`, `Ữ` will clip or collide).
* **Eyebrow / Metadata Styling:** `font-size: var(--text-xs); letter-spacing: 0.08em; text-transform: uppercase; font-weight: 600;` — keep short (2–4 words).
* **Optimal Reading Measure:** Body copy `max-width: 65ch` on desktop (`35–60ch` on mobile); mobile body font strictly `>= 16px` (`1rem`).
* **Tabular Figures:** Apply `font-variant-numeric: tabular-nums;` on all metrics, pricing tables, countdowns, and spec grids.

---

## 2. ACSS-Mirror Fluid Type & Spacing Scale (`tokens.css`)

Define fluid scales using `clamp()` mapped to exact ACSS variable names so Stage 2 syncs 1-to-1:

```css
:root {
  /* Typography Scale (ACSS Mirror) */
  --h1: clamp(2.35rem, 1.8rem + 2.6vw, 4.25rem);
  --h2: clamp(1.85rem, 1.5rem + 1.6vw, 3rem);
  --h3: clamp(1.4rem, 1.2rem + 0.8vw, 1.95rem);
  --h4: clamp(1.15rem, 1.05rem + 0.4vw, 1.4rem);
  --h5: clamp(1.05rem, 1rem + 0.2vw, 1.2rem);
  --h6: 1rem;

  --text-xs: 0.8125rem;   /* 13px - metadata/eyebrows only */
  --text-s: 0.9375rem;    /* 15px - secondary UI text */
  --text-m: 1rem;         /* 16px - minimum body floor */
  --text-l: clamp(1.125rem, 1.05rem + 0.35vw, 1.3rem);
  --text-xl: clamp(1.25rem, 1.1rem + 0.6vw, 1.6rem);

  /* Spacing Scale (ACSS Mirror - Pure Context-Agnostic Scale) */
  --space-xxs: 0.25rem;
  --space-xs: 0.5rem;
  --space-s: 0.875rem;
  --space-m: clamp(1.25rem, 1rem + 0.6vw, 1.625rem);
  --space-l: clamp(1.75rem, 1.4rem + 1.2vw, 2.5rem);
  --space-xl: clamp(2.5rem, 2rem + 1.8vw, 3.75rem);
  --space-xxl: clamp(3.5rem, 2.6rem + 3vw, 5.5rem);

  /* Section & Layout Rhythm */
  --section-space-s: clamp(2.75rem, 2rem + 2.5vw, 4.5rem);
  --section-space-m: clamp(4rem, 3rem + 3.5vw, 6.5rem);
  --section-space-l: clamp(5.5rem, 4rem + 5vw, 9rem);
  --content-width: 80rem; /* 1280px standard agency container */
  --gutter: clamp(1.25rem, 3vw, 2.5rem);
}
```

---

## 3. Disciplined 60-30-10 Color System (Mapped to ACSS)

AI designs look amateur when every section uses a different saturated color. Enforce strict color discipline:

* **60% Dominant Surface (`--base`, `--bg-light`, `--white`):** Clean off-white, warm stone, alabaster, or deep charcoal (in dark-mode sections). Avoid harsh sterile `#FFFFFF` paired with pure `#000000`; prefer tinted neutrals (e.g., `#F8F7F4` surface + `#16181D` ink).
* **30% Structural Contrast (`--neutral`, `--bg-dark`, `--shade`):** Alternating surface bands (e.g., light -> subtle warm tint -> light -> deep anchor dark band) to separate sections cleanly **without** heavy boxes or borders.
* **10% Action & Focal Accent (`--primary`, `--accent`):** Reserved strictly for the **single primary CTA per viewport**, active states, key eyebrow highlights, and critical data points. Never flood large card backgrounds with `--primary` unless it is a deliberate single anchor band.

### Mandatory Contrast & Color Guardrails
* Normal body text contrast: **`>= 4.5:1`** (WCAG AA minimum; aim for `>= 7:1` on long-form `Read` surfaces).
* Large headings (`>= 24px` or `18.66px` bold) & UI borders/icons: **`>= 3:1`**.
* **No Off-Palette Drift:** Every color in `styles.css` must reference a `var(--*)` token declared in `tokens.css` and `design-system.json`. Zero stray hex codes inside component CSS.
* **Hairline Dividers Over Heavy Boxes:** Prefer `1px solid var(--border-color)` (at 8%–14% ink opacity) over heavy gray borders or muddy drop shadows.
