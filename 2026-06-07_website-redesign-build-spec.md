# Website redesign — build spec

**Site:** sayantanhroy.github.io (Jekyll / AcademicPages fork of Minimal Mistakes)
**Date:** 2026-06-07
**Purpose:** Hand to Claude Code to implement against the repo. Captures the palette, type, nav, per-page structure, copy drafts, and accessibility rules agreed during the design pass.
**Audience the site serves:** academic search committees *and* PhD-level industry roles (tech-economist / applied-scientist at firms like Amazon and Meta, and economic consulting). Research and projects carry equal weight.

---

## 0. Workflow — preview before going live

- GitHub Pages builds the live site from the main branch. Do all redesign work on a separate branch (e.g. `redesign`).
- Preview locally: `bundle exec jekyll serve --livereload` → http://localhost:4000. (Or the Docker option AcademicPages ships, to avoid the Ruby setup.) Nothing is public until the branch is pushed and merged.
- Commit as you go — git history is the safety net; no need for parallel "copy" folders.

---

## 1. Design tokens

### Color (light theme, plum accent)

| Role | Hex |
|---|---|
| Page background | `#faf8f6` |
| Body text (ink) | `#221f24` |
| Muted text | `#56525c` |
| Faint text / meta | `#8a8590` |
| Accent — links, rules, eyebrows (plum) | `#6b4e71` |
| Accent fill — pills, photo background | `#efe9f1` |
| Featured tint — job market paper block | `#f6f1f7` |
| Pill / accent-on-fill text | `#4a3550` |
| Hairline border | `rgba(0,0,0,0.12)` |

Accessibility: plum on the page background is ~6.6:1 contrast (passes WCAG AA and is colorblind-safe across deuteranopia/protanopia/tritanopia). Links must be **underlined**, never distinguished by color alone.

### Typography

- Headings / display: **serif** — Source Serif 4 (alt: Newsreader).
- Body / UI: **sans** — Inter (alt: Source Sans 3).
- Mono (rare): JetBrains Mono or system mono.

Scale (desktop):

| Element | Spec |
|---|---|
| Hero name | 33px serif |
| Page title | 26px serif |
| Section subhead | 16px serif, with a 0.5px hairline underline |
| Paper title | 15–16px serif |
| Project title | 15px sans |
| Body | 15–16px sans, line-height 1.65 |
| Meta / secondary | 13px |
| Eyebrow / label | 11px, uppercase, letter-spacing 0.13em, plum |

Sentence case for all headings. Two weights only (regular + medium).

### Shape & spacing

- Border radius: 8px general, 12px cards. All borders 0.5px hairline.
- Photo: **arched duotone** — your photo mapped to plum (`#6b4e71`) over `#efe9f1`; shape `border-radius: 44px 44px 10px 10px`. Provide descriptive alt text.

---

## 2. Navigation

`Home · Research · Projects · Teaching · CV / résumé`

Projects is a new top-level page — add it to `_data/navigation.yml`.

---

## 3. Pages

### Home
- Arched duotone photo (left) beside the name (serif, 33px).
- Hero line — recommended draft (rewrite in your voice): *"Fifth-year Economics PhD candidate at Purdue, pairing structural macro and causal inference with a data-science background in large-scale ML."*
- About block — recommended, **first person** (rewrite in your voice): *"I'm a fifth-year Economics PhD candidate at Purdue, studying how government spending mitigates economic shocks and why its effects vary with the size of local labor markets. My job market paper estimates these effects across U.S. counties and explains them with a multi-region model. Before the PhD, I was a data scientist at American Express, building credit- and fraud-risk models on large transaction data. I work mostly in Python, JAX, Julia, and Stata."*
- Links row: CV · Résumé · GitHub · LinkedIn · Email (plum, underlined).
- Hairline divider.
- Two equal columns:
  - Selected research — job market paper: title, one-line finding, links (PDF · slides · code).
  - Selected projects — two featured: title, one-line description, tech tags, link.

### Research
- Page title + a fields line (macroeconomics · spatial/regional economics · fiscal policy · international trade).
- Featured job market paper in a plum-tint (`#f6f1f7`) block: eyebrow "Job market paper", serif title, one-line finding (always visible), then a meta row — `Abstract` toggle · PDF · Slides · Code. Abstract hidden by default, expands on click.
- Working papers / work-in-progress below as a plain list: title, coauthors, one-line finding, expandable abstract, links.
- Click-to-expand: use a real `<button>` with `aria-expanded`, toggling a hidden `.abs-body`. Must be keyboard-operable. (Reference implementation built during design.)

### Projects (the industry engine)
- Title + one-line intro.
- Each entry: category eyebrow, title (sans), a one-line recruiter-legible description, tech-tag pills (plum), and a **link slot that varies by what actually exists** — `GitHub ↗`, or `Draft · Slides`, or `In progress · code on request`, or `proprietary`. No dead links, no empty placeholder repos.
- Drafted shortlist (trim / reorder; add a number wherever legitimate):
  1. **Numerical methods** — Regional dynamic IO tariff model: JAX Newton–Krylov steady-state solver, 48×41 scale. *(in development — no link yet)*
  2. **Scientific computing** — DSGE perturbation solver, Julia → Python (SGU/Klein) with SymPy + JAX backends, validated on a two-country IRBC model. *(shareable — candidate for a real repo)*
  3. **Data engineering** — Interwar trade price-index pipeline: Laspeyres/Paasche/Fisher indices + state deflators, 1927–1935.
  4. **Causal inference** — County-level fiscal multipliers: narrative IV (Stata) + multi-region NK model with search frictions.
  5. **Production ML** — Credit & fraud risk models at American Express: XGBoost on large transaction data (PySpark, Hive, SQL). *(proprietary)*
  6. **Structural modeling** — Brokers in public service delivery: queuing model, Cournot competition, value-function iteration.

### Teaching
- Courses: ECON 380, ECON 612 (Purdue), as teaching assistant. Optional materials / evaluations.

### CV / résumé
- Two clickable cards:
  - Academic CV — full PDF, for faculty/postdoc committees.
  - Résumé — 1-page PDF, for economist/applied-scientist/consulting roles.
  - Each card: icon, title, one-line "who it's for", format + updated date, `View ↗ · Download`.
- Highlights strip beneath (for skimmers who won't open a PDF): Now / Research / Before / Toolkit (4 lines).
- The full CV body text does **not** render on the page anymore — it lives in the PDF.

---

## 4. CV PDF reorganization (the document, not the page)

The current CV is missing a research section; for a job-market CV that is the spine.

- Section order: Education → **Research** → Professional experience → Presentations → Teaching → Technical skills → Grants & awards → References.
- Add the research section (job market paper + working papers).
- Put numbers in the American Express bullets (accounts scored, $ exposure, lift, automation rate).
- Drop the 2018 IIT research-assistant line (old/minor for a PhD CV).
- Add presentations (Midwest Macro 2026, ISI Delhi 2025), teaching, and references — **verify all of these against reality.**

---

## 5. Accessibility checklist

- Links underlined, not color-only.
- Contrast ≥ 4.5:1 (palette passes; plum ~6.6:1).
- Photo has descriptive alt text.
- Expandable abstracts use real `<button>` + `aria-expanded`, keyboard operable.
- Never encode meaning by color alone — pair with text or an icon.

---

## 6. Open items to fill before launch

- Per-project link states (which projects have public repos vs slides vs in-progress).
- Real paper abstracts (drafts in the design were placeholders).
- Metrics in the experience bullets.
- PDF page counts + "updated" dates on the CV/résumé cards.
- Final hero + About wording, and confirm first-person voice.
