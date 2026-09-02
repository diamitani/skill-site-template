# Skill Site Template v1.0

A reusable single-file HTML template for skill landing pages. Light theme, Framer-inspired, mobile-first, no build step.

**See [TEMPLATE_README.md](TEMPLATE_README.md) for the full placeholder list and usage guide.**

## Quick Start

```bash
# 1. Copy template
cp index.html ./my-skill-site/index.html

# 2. Find/replace all {{...}} placeholders
# 3. Duplicate REPEAT blocks for more steps/features/use cases
# 4. Push to GitHub Pages (Settings → Pages → main / root)
```

## Example Implementations

- [diamitani/asana-organizer-site](https://github.com/diamitani/asana-organizer-site) — built from this template

## Structure (10 sections)

Nav → Hero → About → How It Works → Features → Use Cases → Technical → Install → CTA → Footer

## Design Tokens (locked in CSS)

- bg `#FFFFFF`, accent `#2563EB` (cobalt)
- Inter font (Google Fonts, 400/500/600/700/800)
- Hero title: `clamp(2.25rem, 5vw, 4rem)`, weight 800
- Container max-width 1200px
- Responsive: 480/768/1024/1280px breakpoints

## Built-in Features

- Sticky nav with backdrop-blur
- Mobile hamburger menu (vanilla JS)
- Smooth scroll
- IntersectionObserver fade-in (respects `prefers-reduced-motion`)
- Copy-to-clipboard on install code block
