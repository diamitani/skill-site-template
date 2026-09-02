# Skill Site Template v1.0

A single-file, self-contained HTML template for shipping beautiful landing pages for any Hermes skill. Fill in `{{PLACEHOLDERS}}`, duplicate the `REPEAT` blocks, and `git push`.

---

## Quick start

1. Copy `index.html` to your skill's repo.
2. Search-and-replace the placeholders listed below.
3. Duplicate the `REPEAT` blocks for stats, steps, features, use cases, and tech cards if you need more (defaults already ship with the correct counts).
4. Push to GitHub Pages (see [Deploy](#deploy)).

The file is fully responsive, has no external JS dependencies, and weighs ~55 KB.

---

## File structure

| Section | Tag | ID | Purpose |
| --- | --- | --- | --- |
| 1. Nav | `<header>` | — | Sticky nav, brand, links, CTA, mobile hamburger |
| 2. Hero | `<section>` | — | Badge, 3-line title (line 2 is gradient), subtitle, CTAs |
| 3. About | `<section>` | `about` | Stats grid (4 cards) |
| 4. How It Works | `<section>` | `how` | Numbered process steps (4 cards) |
| 5. Features | `<section>` | `features` | Feature cards with icons (6 cards) |
| 6. Use Cases | `<section>` | `usecases` | Accented left-border cards (4 cards) |
| 7. Technical | `<section>` | `technical` | Tech-detail cards (4 cards) |
| 8. Install | `<section>` | `install` | Code block + copy button + requirements |
| 9. CTA | `<section>` | — | Dark gradient closing CTA |
| 10. Footer | `<footer>` | — | Brand, nav, resources, copyright |

---

## Placeholders

Search-and-replace all instances. All placeholders are uppercase with underscores.

### Identity

| Placeholder | What goes in it | Example |
| --- | --- | --- |
| `{{SKILL_NAME}}` | Short, human-readable skill name | `Asana Project Organizer` |
| `{{SKILL_SLUG}}` | URL-friendly slug | `asana-organizer` |
| `{{TAGLINE}}` | One-line marketing hook | `Tidy Projects in 30 Seconds, Not 30 Minutes` |
| `{{AUTHOR}}` | Your name / org | `Hermes Team` |
| `{{CATEGORY}}` | Category badge text | `Project Management · Multi-Tool` |
| `{{GITHUB_REPO}}` | Full GitHub URL | `https://github.com/nous/asana-organizer` |

### Hero

| Placeholder | What goes in it | Example |
| --- | --- | --- |
| `{{HERO_BADGE}}` | Tiny label above title | `Project Management · Multi-Tool` |
| `{{HERO_LINE_1}}` | First title line | `Tidy Projects` |
| `{{HERO_LINE_2}}` | Second line (gets gradient) | `in 30 Seconds` |
| `{{HERO_LINE_3}}` | Third title line | `Not 30 Minutes` |
| `{{SUBTITLE}}` | Paragraph under title | `A Hermes skill that scans your Asana workspace…` |

### Stats (4 cards)

| Placeholder | What goes in it |
| --- | --- |
| `{{STAT_1_VALUE}}` | Big number/value (e.g. `30s`, `12×`, `99%`) |
| `{{STAT_1_LABEL}}` | Label under it |
| `{{STAT_2_VALUE}}`, `{{STAT_2_LABEL}}` | (same pattern) |
| `{{STAT_3_VALUE}}`, `{{STAT_3_LABEL}}` | (same pattern) |
| `{{STAT_4_VALUE}}`, `{{STAT_4_LABEL}}` | (same pattern) |

### How It Works (4 steps)

| Placeholder | What goes in it |
| --- | --- |
| `{{STEP_1_TITLE}}` | Step heading |
| `{{STEP_1_DESC}}` | Step body |
| `{{STEP_2_TITLE}}`, `{{STEP_2_DESC}}` | … |
| `{{STEP_3_TITLE}}`, `{{STEP_3_DESC}}` | … |
| `{{STEP_4_TITLE}}`, `{{STEP_4_DESC}}` | … |

### Features (6 cards)

| Placeholder | What goes in it |
| --- | --- |
| `{{FEATURE_1_ICON}}` | Single emoji or 1–2 char glyph (e.g. `⚡`, `🔍`, `📦`) |
| `{{FEATURE_1_TITLE}}` | Feature heading |
| `{{FEATURE_1_DESC}}` | Feature body |
| `{{FEATURE_2_ICON}}` … `{{FEATURE_6_DESC}}` | (same pattern) |

### Use Cases (4 cards)

| Placeholder | What goes in it |
| --- | --- |
| `{{USECASE_1_TITLE}}` | Use-case heading |
| `{{USECASE_1_DESC}}` | Use-case body |
| `{{USECASE_2_TITLE}}`, `{{USECASE_2_DESC}}` | … |
| `{{USECASE_3_TITLE}}`, `{{USECASE_3_DESC}}` | … |
| `{{USECASE_4_TITLE}}`, `{{USECASE_4_DESC}}` | … |

> The eyebrow label ("Use Case 01", "Use Case 02", …) is hard-coded — edit the HTML directly if you want different eyebrows.

### Technical (4 cards)

| Placeholder | What goes in it |
| --- | --- |
| `{{TECH_1_TITLE}}` | Short label (e.g. `STACK`) |
| `{{TECH_1_VALUE}}` | Main value (e.g. `Python 3.11+`) |
| `{{TECH_1_DESC}}` | One-line description |
| `{{TECH_2_TITLE}}` … `{{TECH_4_DESC}}` | (same pattern) |

### Install

| Placeholder | What goes in it |
| --- | --- |
| `{{INSTALL_COMMAND}}` | The exact code in the install box. Keep on one line or pre-format with leading spaces. |
| `{{REQUIREMENTS_LIST}}` | One bullet per `<li>` for the requirements list (duplicate the `<li>` line as many times as needed) |

### Final CTA

| Placeholder | What goes in it |
| --- | --- |
| `{{CTA_HEADING}}` | Headline of the dark closing CTA |
| `{{CTA_SUBTEXT}}` | Supporting paragraph |

---

## REPEAT blocks

Search the file for `<!-- REPEAT:` to find each block. Default counts match the placeholders above. To add more:

| Block | Default | To add more |
| --- | --- | --- |
| Stat cards | 4 | Duplicate the `<div class="stat-card fade-in">` block; add `{{STAT_5_VALUE}}`, `{{STAT_5_LABEL}}` placeholders |
| Steps | 4 | Duplicate the `<div class="step fade-in">` block |
| Feature cards | 6 | Duplicate the `<div class="feature-card fade-in">` block; add `{{FEATURE_N_ICON}}`, `{{FEATURE_N_TITLE}}`, `{{FEATURE_N_DESC}}` |
| Use case cards | 4 | Duplicate the `<div class="usecase-card fade-in">` block |
| Tech cards | 4 | Duplicate the `<div class="tech-card fade-in">` block |
| Requirement `<li>` | 1 | Duplicate the `<li>` inside `.install-requirements ul` |

The CSS grid is set up for **2 / 4 / 6 columns** at the breakpoints. If you add a 5th stat you'll want to change `grid-template-columns: repeat(4, 1fr)` to `repeat(auto-fit, minmax(180px, 1fr))` or similar in `.about-grid`.

---

## Design tokens

| Token | Value | Where it's used |
| --- | --- | --- |
| `--bg` | `#FFFFFF` | Page background |
| `--bg-secondary` | `#F8FAFC` | Alternate section backgrounds |
| `--text` | `#0F172A` | Headings & primary copy |
| `--text-secondary` | `#475569` | Body copy & meta |
| `--accent` | `#2563EB` (cobalt) | CTAs, links, highlights |
| `--accent-hover` | `#1D4ED8` | Hover state |
| `--accent-light` | `#EFF6FF` | Badges & soft fills |
| `--border` | `#E2E8F0` | Card borders, dividers |
| `--success` | `#10B981` | "Copied!" feedback, status dots |

### Typography

- **Font:** Inter (Google Fonts) — weights 400 / 500 / 600 / 700 / 800
- **Hero title:** `clamp(2.25rem, 5vw, 4rem)`, line-height 1.15, weight 800
- **Section title:** `clamp(1.875rem, 4vw, 2.5rem)`, weight 800
- **Body:** 16px, line-height 1.6

### Spacing & layout

- Section padding: `6rem` desktop, `4rem` mobile
- Container: `max-width: 1200px`, padding `0 1.5rem`
- Border radius scale: 8 / 12 / 16 / 20 px

### Shadows

- Default: `0 1px 3px rgba(0, 0, 0, 0.05)`
- Hover: `0 4px 24px rgba(0, 0, 0, 0.06)` + `translateY(-2px)`

### Breakpoints (mobile-first)

| Width | Layout change |
| --- | --- |
| `≥ 480px` | (default mobile) |
| `≥ 768px` | Stats → 4 col · Steps → 2 col · Features → 2 col · Use cases → 2 col · Tech → 2 col · Nav links appear |
| `≥ 1024px` | Hero splits into 2 columns · Steps → 4 col · Features → 3 col |
| `≥ 1280px` | (max container width hits 1200px) |

---

## Critical UX features (all wired up)

- ✅ **Sticky nav with backdrop-blur** — adds `.scrolled` class on scroll for border + shadow
- ✅ **Mobile hamburger** — vanilla JS toggle, animated bars, ESC to close, auto-close on resize
- ✅ **Smooth scroll** — all `a[href^="#"]` get offset for sticky nav; respects `prefers-reduced-motion`
- ✅ **IntersectionObserver fade-in** — `.fade-in` elements animate as they enter viewport; falls back to instant if reduced motion is on
- ✅ **Copy-to-clipboard** — install code block has a Copy button with "Copied!" feedback for 2 seconds, plus a fallback for non-secure contexts
- ✅ **Fully responsive** — mobile-first CSS with the breakpoints above

---

## Deploy (GitHub Pages)

The template is a single static file. Three steps:

```bash
# 1. Drop the file into a fresh repo (or your skill's existing repo)
cp index.html /path/to/your-repo/

cd /path/to/your-repo
git init   # if new
git add index.html
git commit -m "Add skill landing page"
git branch -M main
git remote add origin git@github.com:YOUR_ORG/YOUR_SKILL_REPO.git
git push -u origin main

# 2. Enable Pages: repo Settings → Pages → Source: "Deploy from a branch" → main / (root)
# 3. Your site is live at https://YOUR_ORG.github.io/YOUR_SKILL_REPO/
```

That's it — no build step, no npm install.

---

## Worked example: Asana Organizer

Reference fill-ins for the Asana Project Organizer skill (assumed values for illustration):

| Placeholder | Value |
| --- | --- |
| `{{SKILL_NAME}}` | `Asana Project Organizer` |
| `{{SKILL_SLUG}}` | `asana-organizer` |
| `{{TAGLINE}}` | `Tidy Projects in 30 Seconds, Not 30 Minutes` |
| `{{HERO_BADGE}}` | `Project Management · Multi-Tool` |
| `{{HERO_LINE_1}}` | `Tidy Asana Projects` |
| `{{HERO_LINE_2}}` | `in 30 Seconds` |
| `{{HERO_LINE_3}}` | `Not 30 Minutes` |
| `{{SUBTITLE}}` | `A Hermes skill that scans your Asana workspace, archives stale tasks, fills in missing assignees, and surfaces what's actually blocking your team — all from a single slash command.` |
| `{{GITHUB_REPO}}` | `https://github.com/nous/asana-organizer` |
| `{{CATEGORY}}` | `Project Management` |
| `{{AUTHOR}}` | `Hermes Team` |
| `{{INSTALL_COMMAND}}` | `npx hermes-skill install asana-organizer` |
| `{{CTA_HEADING}}` | `Ship cleaner projects today` |
| `{{CTA_SUBTEXT}}` | `Free, open-source, and installs in under a minute.` |

See `/tmp/asana-organizer-site/index.html` for a completed 1,872-line example built from this template.

---

## Customising beyond placeholders

Most of the template is content-driven by placeholders. If you need deeper changes:

- **Different accent colour** — change `--accent` and `--accent-hover` in `:root`
- **Different font** — swap the `<link>` to Google Fonts and update `--font-sans`
- **Add a section** — copy any `<section>` block and replace its content; section padding is handled globally
- **Add an icon SVG** — replace the emoji `{{FEATURE_N_ICON}}` with an inline `<svg>` (the `.feature-icon` wrapper handles sizing)
- **Remove a section** — delete the whole `<section>` block; remember to also remove the matching nav link in `.nav-links`

---

## License

MIT — copy, modify, ship.