# Bricks Builder + ACSS + BEM Pure CSS Handoff Specification

Every template and FE Demo produced by `agency-web-design` MUST follow this specification so it converts **1-to-1 with zero rewrite** into Stage 2 of `bricks-acss-stack` (WordPress + Bricks Builder + ACSS + JetEngine + SureRank via MCP Novamira Pro).

## 1. Deliverable Bundle Structure

```text
<project-demo>/
├── DESIGN.md              # Approved 3-Layer Art Direction, 3 Dials, explicit visual constraints & Do/Don't rules
├── design-system.json     # DTCG-compatible design tokens for direct import into Novamira Design
├── tokens.css             # Exact Automatic.css (ACSS) variable mirror (:root)
├── styles.css             # Pure CSS: base reset, ACSS grid utilities, 1-level BEM component classes
├── main.js                # Lightweight vanilla JS (mobile nav drawer, tabs/accordions, subtle scroll reveals)
├── index.html             # Homepage FE Demo (Gate 1)
└── pages/                 # Optional Gate 1B static previews reusing the EXACT same tokens.css & styles.css
    ├── about.html
    ├── services.html
    ├── archive.html
    ├── single.html
    └── contact.html
```

**Hard Tech Ban:** Never use Tailwind CSS, Bootstrap, React, Vue, Sass preprocessors, or external UI component libraries. Pure semantic HTML5 + modern CSS + lightweight vanilla JS only.

---

## 2. Exact ACSS-Mirror Token Contract (`tokens.css`)

Use **exact Automatic.css token names** (context-agnostic pure scale — never invent `--pad-m` or `--margin-s`):

* **Colors:** `--primary`, `--primary-dark`, `--primary-light`, `--primary-ultra-light`, `--secondary`, `--accent`, `--base`, `--neutral`, `--shade`, `--bg-light`, `--bg-ultra-light`, `--bg-dark`, `--text-dark`, `--text-light`, `--border-color`, `--white`, `--black`
* **Spacing:** `--space-xxs`, `--space-xs`, `--space-s`, `--space-m`, `--space-l`, `--space-xl`, `--space-xxl`
* **Section & Layout:** `--section-space-xs`, `--section-space-s`, `--section-space-m`, `--section-space-l`, `--section-space-xl`, `--content-width`, `--gutter`
* **Typography:** `--font-heading`, `--font-body`, `--h1`..`--h6`, `--text-xs`, `--text-s`, `--text-m`, `--text-l`, `--text-xl`, `--text-xxl`
* **Radius (Demo-Gated Only):** `--radius-none: 0px`, `--radius-xs`, `--radius-s`, `--radius-m`, `--radius-l`, `--radius-circle: 50%`

---

## 3. Native Bricks DOM & 1-Level BEM Rules

Structure every section so it maps directly to Bricks Builder's element tree (`Section` > `Container` > `Block` / `Div`):

```html
<!-- [BRICKS-TEMPLATE: section-services] -->
<section class="services-band" aria-labelledby="services-heading">
  <div class="container">
    <header class="section-head">
      <p class="section-head__eyebrow">Năng lực cốt lõi</p>
      <h2 id="services-heading" class="section-head__title">Giải pháp kỹ thuật trọn gói</h2>
    </header>

    <!-- [JETENGINE-LOOP: cpt=services] -->
    <div class="grid--3 gap--l">
      <!-- [BRICKS-COMPONENT: service-item] -->
      <article class="service-item">
        <span class="service-item__index">01</span>
        <h3 class="service-item__title">Gia công cơ khí chính xác</h3>
        <p class="service-item__excerpt">Dung sai ±0.01mm trên dây chuyền CNC 5 trục chuẩn ISO 9001.</p>
        <a href="#" class="service-item__link">Xem chi tiết</a>
      </article>
      <!-- [/BRICKS-COMPONENT: service-item] -->
    </div>
    <!-- [/JETENGINE-LOOP: cpt=services] -->
  </div>
</section>
```

### BEM & Utility Discipline
* **Max 1 Level Deep:** `.block`, `.block__element`, `.block--modifier`. Never chain `.block__body__header__title`.
* **Layout Utilities Mirror ACSS:** `.container`, `.grid--2`, `.grid--3`, `.grid--4`, `.grid--l-2`, `.grid--m-1`, `.gap--xs`..`.gap--l`.
* **Zero `#id` Styling & Zero `!important`:** Style exclusively via BEM classes so Bricks Cascade Layers (`@layer bricks`) stay clean.
* **Handoff Annotations:** Always wrap reusable components, dynamic loops, and global templates in exact HTML comments:
  * `<!-- [BRICKS-TEMPLATE: header / footer / archive / single] -->`
  * `<!-- [BRICKS-COMPONENT: component-name] -->`
  * `<!-- [JETENGINE-LOOP: cpt=slug] -->`

---

## 4. DTCG `design-system.json` Format (Novamira Design Ready)

Every finalized template must include a clean DTCG-compatible `design-system.json` capturing palette, typography, spacing, radii, and **explicit fidelity constraints** so Stage 2 locks visual grammar with zero drift:

```json
{
  "$schema": "https://design-tokens.github.io/community-group/format/",
  "meta": {
    "archetype": "Swiss Corporate",
    "surfaceMode": "Persuade",
    "dials": { "variance": 3, "motion": 2, "density": 5 },
    "iconFamily": "Lucide (1.5px stroke)",
    "fidelityConstraints": [
      "Sharp 0px corners on all images and cards",
      "No box-shadow on content cards",
      "Use 1px hairline dividers instead of boxed wrappers"
    ]
  },
  "color": {
    "primary": { "$value": "#0F2942", "$type": "color" },
    "accent": { "$value": "#D96B27", "$type": "color" },
    "base": { "$value": "#F7F6F2", "$type": "color" },
    "textDark": { "$value": "#16181D", "$type": "color" },
    "textLight": { "$value": "#F7F6F2", "$type": "color" },
    "border": { "$value": "rgba(22, 24, 29, 0.12)", "$type": "color" }
  },
  "typography": {
    "fontHeading": { "$value": "Be Vietnam Pro", "$type": "fontFamily" },
    "fontBody": { "$value": "Be Vietnam Pro", "$type": "fontFamily" }
  },
  "radius": {
    "default": { "$value": "0px", "$type": "dimension" }
  }
}
```
