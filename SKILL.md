---
name: agency-web-design
description: >-
  Multi-industry agency web design system, anti-AI-slop art direction, and
  craft critique skill engineered specifically for pure HTML5/CSS,
  Automatic.css (ACSS) tokens, 1-level BEM, and 1-to-1 handoff into Bricks
  Builder (bricks-acss-stack). Use whenever designing website templates,
  creating Stage 1 / Gate 1B FE Demos, defining brand Design Specs (DESIGN.md /
  design-system.json), or critiquing and polishing visual craft across client
  industries without Tailwind or React.
---

# Agency Web Design — Multi-Industry Craft & Anti-AI-Slop System

A **3-layer agency design governance skill** distilling multi-industry design intelligence (**UI/UX Pro Max**), editorial art direction & anti-slop discipline (**Taste Skill**), and craft critique/polish workflows (**Impeccable**), locked 100% to **pure HTML5 + CSS + ACSS tokens + 1-level BEM** for zero-rewrite handoff into `bricks-acss-stack`.

## Mandatory Pre-Build Gate (Design Spec Before Code)

Never jump straight into writing HTML/CSS from a brief. Complete **Phase 0** and **WAIT for user confirmation** before generating template code:

1. **One-Line Design Read:**
   *"Reading this as: `<page kind>` for `<industry & audience>`, in `<Surface Mode>` mode, anchored in the `<Archetype>` visual language."*
2. **Lock the 3-Layer Spec (`DESIGN.md` summary presented for sign-off):**
   * **Layer 1 — Industry & Archetype:** Select 1 of the 6 Agency Visual Archetypes and the matching industry blueprint from [industry-archetypes.md](./references/industry-archetypes.md) (hero strategy, conversion flow, proof types, industry anti-patterns).
   * **Layer 2 — Visual Calibration:** Set Surface Mode (`Persuade` | `Read` | `Experience` | `Operate`), the **3 Dials** (`DESIGN_VARIANCE` / `MOTION_INTENSITY` / `VISUAL_DENSITY` on 1–10), exact color roles (60-30-10 mapped to ACSS), Vietnamese-safe font pairing from [typography-and-color-vn.md](./references/typography-and-color-vn.md), and a **single cohesive SVG icon family** with uniform `stroke-width`.
   * **Layer 3 — Section Composition Plan:** List every section with its **distinct layout composition pattern** (from [anti-slop-and-composition.md](./references/anti-slop-and-composition.md)), image aspect ratios, and CTA placement. **No two adjacent sections may share the same layout pattern.**
3. **WAIT for Confirmation:** Only write `tokens.css`, `styles.css`, `design-system.json`, and HTML templates after the user approves the Design Spec (or gives overrides).

## Core 4-Step Template Creation Workflow

### Step 1 — Spec & Token Lock
* Output `DESIGN.md` (human-readable art direction + explicit visual constraints) and `design-system.json` (DTCG-compatible, ready for **Novamira Design**).
* Output `tokens.css` mirroring exact **Automatic.css (ACSS)** variable names (`--primary`, `--secondary`, `--accent`, `--base`, `--neutral`, `--space-xs`..`--space-xxl`, `--section-space-*`, `--text-*`, `--h1`..`--h6`, `--radius-*`, `--content-width`).

### Step 2 — Pure HTML5 + CSS + BEM Template Build
* Build the Homepage FE Demo (`index.html`, `styles.css`, `main.js`) following [bricks-acss-handoff.md](./references/bricks-acss-handoff.md):
  * Native Bricks DOM hierarchy (`section` > `.container` > `.grid--*` / `.block`).
  * 1-level BEM Global Classes (`.block`, `.block__element`, `.block--modifier`) consuming only `var(--*)` ACSS tokens.
  * Handoff comments (`<!-- [BRICKS-COMPONENT: name] -->`, `<!-- [JETENGINE-LOOP: cpt=slug] -->`, `<!-- [BRICKS-TEMPLATE: name] -->`).
  * Real, humanized copy (zero Lorem Ipsum, zero AI clichés) and cohesive imagery with consistent `aspect-ratio`.
* For inner pages & dynamic templates (Gate 1B): **strictly reuse the exact approved `tokens.css` and `styles.css`** — never re-initialize tokens or ship bare text-only skeletons.

### Step 3 — Art Director Critique & Playwright Visual QA
* Run a self-critique against the 5-dimension rubric in [critique-and-polish.md](./references/critique-and-polish.md) before presenting to the user.
* Capture Desktop (`1440x900`) and Mobile (`390x844`) full-page screenshots via `playwright-cli`, check console errors, horizontal overflow, contrast (`>= 4.5:1`), touch targets (`>= 44x44px`), and `100dvh` hero stability.
* Fix all visual or spacing defects in one tight polish pass before presentation.

### Step 4 — Steering Refinement & Bricks Handoff
* Refine in place using targeted steering verbs (`critique`, `audit`, `polish`, `bolder`, `quieter`, `distill`, `clarify`, `de-slop`).
* Once approved, lock all visual constraints into `DESIGN.md` / `design-system.json` (e.g., *"sharp 0px corners, borderless editorial photography, Lucide 1.5px icons"*) and hand off cleanly to Stage 2 of `bricks-acss-stack`.

## Hard Guardrails (Non-Negotiable)

* **Zero Tailwind / Bootstrap / React:** Never output utility frameworks or React/Framer Motion components. Every style must map 1-to-1 to pure CSS + ACSS tokens + Bricks BEM classes.
* **Anti-AI-Slop Bans:** Never use glowing purple-blue gradients, stacked 3-column icon-in-circle cards across consecutive sections, gratuitous glassmorphism, heavy generic drop shadows, emoji icons, or unstyled default Inter/Roboto.
* **Strict Fidelity (Zero Unrequested Styling):** Never invent `border-radius`, `border`, `box-shadow`, or extra card wrappers unless explicitly declared in the approved `DESIGN.md` / Archetype. If the design calls for sharp `0px` edges and borderless media, enforce `border-radius: 0; border: none; box-shadow: none;` strictly.
* **Visual Richness Floor:** Every sub-page and dynamic template (Archive, Single, About, Services, Contact) must match the Homepage's craft density — cohesive SVG icon family, palette-matched media with locked aspect ratios, structured metadata/eyebrows, and crisp interactive states.
* **Vietnamese Diacritic Safety:** Never select a Google Font that breaks or falls back on Vietnamese diacritics (`ă, â, đ, ê, ô, ơ, ư` and stacked tone marks). Always pick from the verified pairings in [typography-and-color-vn.md](./references/typography-and-color-vn.md) unless the client mandates a licensed brand font.

## Reference Library (Load Only What Current Task Needs)

* Multi-industry blueprints & 6 Agency Visual Archetypes (UI/UX Pro Max distilled): [industry-archetypes.md](./references/industry-archetypes.md)
* Vietnamese-safe typography pairings, ACSS fluid scales & 60-30-10 color system: [typography-and-color-vn.md](./references/typography-and-color-vn.md)
* 12 non-generic section compositions, rhythm rules & Anti-AI-Slop bans (Taste Skill distilled): [anti-slop-and-composition.md](./references/anti-slop-and-composition.md)
* Art-director critique rubric, steering verbs & Playwright visual QA (Impeccable distilled): [critique-and-polish.md](./references/critique-and-polish.md)
* Bricks + ACSS + BEM pure CSS handoff specification & DTCG `design-system.json` format: [bricks-acss-handoff.md](./references/bricks-acss-handoff.md)
