---
name: site-template
description: >
  Reusable single-file HTML template for skill landing pages (Framer-style light theme, 64 placeholders, GitHub Pages ready) Use this skill when working with site template tasks or workflows.
---

# Skill Site Template v1.0

A reusable single-file HTML template for skill landing pages. Light theme, Framer-inspired, mobile-first, no build step.

**📖 See [TEMPLATE_README.md](TEMPLATE_README.md) for the full placeholder list, REPEAT block guide, design tokens, and deploy instructions.**

## Quick Start

```bash
# 1. Copy template
cp index.html ./my-skill-site/index.html

# 2. Find/replace all {{...}} placeholders (see TEMPLATE_README.md)
# 3. Duplicate REPEAT blocks for more steps/features/use cases
# 4. Push to GitHub Pages (Settings → Pages → main / root)
```

## Example Implementations

- [diamitani/asana-organizer-site](https://github.com/diamitani/asana-organizer-site) — built from this template
- [diamitani/pae-landing](https://github.com/diamitani/pae-landing) — same design language, hand-built

## Structure (10 sections)

Nav → Hero → About → How It Works → Features → Use Cases → Technical → Install → CTA → Footer

## Design Tokens (locked in CSS)

- bg `#FFFFFF`, secondary `#F8FAFC`, text `#0F172A`, accent `#2563EB` (cobalt)
- Inter font (Google Fonts, 400/500/600/700/800)
- Hero title: `clamp(2.25rem, 5vw, 4rem)`, weight 800
- Container max-width 1200px, padding 0 1.5rem
- Section padding: 6rem desktop / 4rem mobile
- Responsive: 480/768/1024/1280px breakpoints

## Built-in Features

- Sticky nav with backdrop-blur on scroll
- Mobile hamburger menu (vanilla JS toggle)
- Smooth scroll on anchor links
- IntersectionObserver fade-in animations (respects `prefers-reduced-motion`)
- Copy-to-clipboard on install code block ("Copied!" feedback for 2s)
- No build step — single HTML file, deploy anywhere

## Counts

- **Lines:** 1,947
- **Placeholders:** 70 unique `{{...}}` tokens
- **Sections:** 10 (Nav, Hero, About, How, Features, Use Cases, Technical, Install, CTA, Footer)
- **REPEAT blocks:** 6 (stat, step, feature, usecase, tech, requirement)
- **File size:** 56 KB
