# Portfolio Improvement Prompt

## Context

This is Derek Nagel's personal portfolio site, live at **dereknagel.site** and deployed on Vercel. It's a single `index.html` file (~2,400 lines) with inlined CSS and JS — no framework, no build step. The site uses a dark navy/green color scheme inspired by Brittany Chiang's v4 portfolio.

The codebase is intentionally simple: one HTML file, a PDF resume, an OG image SVG, and ~18 images in `images/`. Deployed via `vercel.json` with zero config.

## Current Sections

1. **Hero** — greeting, name, tagline, two CTAs (See my work / Resume)
2. **About** — bio, skills list, headshot with green border effect
3. **Experience** — tabbed layout (Tesla, Salt Creek, Pipeline)
4. **Projects** — featured projects (Tesla battery rebuild, ADS-B tracker, LED display) + smaller project cards + YouTube video embeds
5. **Education** — George Mason, coursework, stats row
6. **Contact** — email CTA, social links

Also has: scroll progress bar, lightbox for images, scroll-reveal animations, a Tesla "charging" scrolljack section, hamburger mobile nav, left/right fixed sidebars.

## What to Improve

Make the site more impressive, polished, and memorable. Derek is a senior ME student applying for engineering internships — the site should stand out. Here are specific areas to explore:

### Visual / UX
- The hero is generic — consider adding a particle background, animated mesh gradient, or subtle 3D element (Three.js is fine if lightweight)
- The scroll-reveal animations are basic fade-ups. Consider staggered reveals, parallax effects, or scroll-triggered transitions
- The Tesla "charging" scrolljack section is clever but janky on some screen sizes — polish or reimagine it
- Image loading could use blur-up placeholders or skeleton states
- Add a dark/light mode toggle (the current dark-only palette is limiting)
- Consider micro-interactions: hover states on project cards, magnetic cursor effects on CTAs, smooth section transitions

### Content / Structure
- The About section skills list is plain — consider an interactive skills visualization (radar chart, animated progress bars, or grouped category cards)
- Projects could use filtering/sorting by tech stack
- Missing a "What I'm Working On Now" or timeline component showing current projects
- No testimonials or recommendations section
- The stats row in Education is static — animate the numbers counting up on scroll

### Performance
- All CSS and JS is inlined — consider extracting critical CSS and lazy-loading the rest
- Images are not optimized (no WebP, no srcset, no lazy loading beyond what the browser does natively)
- Font loading could be improved (the current print-media trick is good but FOUT is noticeable)

### Technical
- No service worker or PWA features
- No structured data / JSON-LD for SEO
- The phone number in the sidebar (847-624-4222) appears to be wrong — Derek's actual number is 847-226-3311
- Console has no errors but also no Easter eggs — add something fun for devs who inspect

### Constraints
- Keep it as a single `index.html` if possible (no build tooling, no framework migration)
- Must stay deployable on Vercel with zero config
- Don't remove any existing sections or content — only enhance
- Keep the dark navy/green brand but feel free to add depth (gradients, glassmorphism, etc.)
- Mobile-first responsive — test at 375px, 768px, and 1440px
- The resume PDF link must stay functional
- Respect `prefers-reduced-motion`

## Files

```
index.html          — the entire site (HTML + CSS + JS inlined)
Derek_Nagel_Resume.pdf
og-image.svg
vercel.json         — {"cleanUrls": true}
images/             — 18 JPG/PNG assets (headshot, projects, Tesla, volleyball, aviation)
```

## How to Test

```bash
cd /Users/Nagel/Code/Web/Derek_Nagel_Portfolio_v2
npx serve .
# or just open index.html in Safari
```

The site is deployed automatically on push — Vercel project is "portfolio" under dnage76-beep.
