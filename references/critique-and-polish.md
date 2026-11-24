# Art-Director Critique Rubric, Steering Verbs & Playwright Visual QA

Distilled from **Impeccable** craft review standards and aligned with `bricks-acss-stack` Bounded Verification.

## 1. Pre-Presentation Self-Critique Rubric (Score 1–5)

Before presenting ANY FE Demo or Gate 1B sub-page preview to the user/client, inspect the rendered Playwright screenshots and score all 5 dimensions honestly. **Any score below 4 MUST be fixed before presenting.**

1. **First-Viewport Authority (Above the Fold):**
   * Does the hero communicate *who this is for, what they do, and what to do next* within 3 seconds?
   * Is the visual hierarchy unmistakable (1 clear H1, 1 primary CTA, zero clutter)?
   * Does the hero hold its proportions cleanly at `1440x900` and `390x844` using `100dvh`?
2. **Typographic Craft & Vietnamese Legibility:**
   * Are heading-to-body size jumps bold and intentional (not timid `24px` H2s)?
   * Are all Vietnamese diacritics rendering cleanly with zero clipping or fallback font mismatch?
   * Is body line length constrained (`60–75ch` desktop) with comfortable leading (`1.55–1.7`)?
3. **Compositional Rhythm & Anti-Slop Discipline:**
   * Do consecutive sections alternate layouts (zero repeated 3-col icon-card stacks)?
   * Are surface transitions (`light` -> `subtle tint` -> `dark anchor`) and spacing (`--section-space-*`) consistent and generous?
   * Are `border-radius`, borders, and shadows strictly faithful to the chosen Archetype (zero unrequested card polish)?
4. **Visual Richness & Media Cohesion:**
   * Do images share a cohesive mood, palette, and locked `aspect-ratio`?
   * Are icons from a single SVG family with uniform `stroke-width`?
   * Do sub-pages and Archive/Single templates feel just as crafted as the Homepage?
5. **UX & Accessibility Floor:**
   * Contrast `>= 4.5:1` for body text and `>= 3:1` for large headings/UI controls?
   * Mobile body font `>= 16px`, touch targets `>= 44x44px` with `>= 8px` gap?
   * Zero horizontal overflow, zero broken images, zero console errors?

---

## 2. Steering Vocabulary (Targeted Refinement Verbs)

When the user requests design revisions, execute the exact verb without breaking locked ACSS tokens or introducing unrequested styling:

| Verb | Meaning & Concrete Action |
| :--- | :--- |
| **`critique`** | Deliver a blunt Art Director & UX review (visual hierarchy, pacing, AI tells, weakest section) with concrete fix proposals before editing. |
| **`audit`** | Run an objective technical check (WCAG contrast, ACSS token usage, BEM naming, DOM semantics, responsive overflow, Core Web Vitals/CLS). |
| **`polish`** | Final precision pass tightening micro-alignment, optical padding, hover/focus transitions, border opacities, and mobile spacing within current tokens. |
| **`bolder`** | Increase typographic scale contrast, sharpen surface/ink contrast, introduce a high-impact dark anchor band, and tighten visual punch. |
| **`quieter`** | Strip visual noise, remove decorative borders/shadows/badges, widen whitespace (`--section-space-l`), and soften secondary chrome. |
| **`distill`** | Cut redundant sections, cards, or text blocks by 20–40% to sharpen focus and reduce cognitive load. |
| **`clarify`** | Rewrite vague headlines, button labels, form labels, and proof metrics into concrete, humanized B2B/industry language. |
| **`de-slop`** | Aggressively strip every AI cliché (generic 3-col icon cards, repetitive symmetry, weak gradients, stock-feeling copy) and replace with catalog patterns (`P3`, `P5`, `P8`, `P9`). |

---

## 3. Bounded Visual Verification via `playwright-cli`

Always verify visually in a real browser — never judge layout quality from raw HTML/CSS alone:

1. **Desktop Pass (`1440x900`):** Open the local static demo, capture full-page screenshot, inspect hero framing, grid alignment, typography scale, image aspect ratios, and hover states.
2. **Mobile Pass (`390x844`):** Resize to `390x844`, capture full-page screenshot, verify:
   * `document.documentElement.scrollWidth <= window.innerWidth` (zero horizontal overflow).
   * Mobile navigation drawer opens/closes cleanly.
   * All touch targets `>= 44x44px`, body font `>= 16px`, zero overlapping text.
3. **Runtime Health Check:** Confirm zero console errors, zero broken `<img>` (`naturalWidth === 0`), and all CSS variables resolve cleanly (no missing `var(--*)`).
4. **Bounded Loop Rule:** Collect all findings, fix them in **one batch**, re-verify with **at most one confirmation screenshot pass**, and present the screenshots + concise summary to the user.
