# EVM Group — 25 Years of Legacy

## Project Overview
Premium single-page promotional website for EVM Group celebrating 25 years in the automotive industry. Showcases automotive, hospitality, and entertainment sectors.

## Tech Stack
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Animations**: CSS keyframes, IntersectionObserver, Lenis smooth scroll
- **Fonts**: Google Fonts — Inter, Playfair Display, Satisfy
- **Server**: Python `http.server` on port 5000

## Key Files
- `index.html` — Full page structure (1,295+ lines)
- `assets/css/custome.css` — All styles + animation keyframes (6,200+ lines)
- `assets/js/main.js` — All interactivity & animation logic (930+ lines)
- `assets/images/` — Brand images, hero Porsche, 25-year graphic
- `assets/videos/` — Hero background MP4

## Animation System

### Intro Sequence (on page load)
1. **Cinematic Preloader** (`#evmPreloader`): Full-screen black screen with italic *EVM* logo, "25 YEARS OF LEGACY" tagline, and animated red gradient loading bar. Dismisses at ~2.3s.
2. **Car Drive-By** (`.hero-intro-car`): Porsche image animates right→left across hero, starts at 2.8s (CSS `animation-delay`), duration 3.6s.
3. **Speed Lines** (`#heroSpeedLines`): Horizontal light streaks flash when car passes the center (~4.9s mark).
4. **Hero Content Reveal** (`.hero-intro-reveal`, `.hero-25-reveal`): EVM 25-year graphic and text fade+slide in after car exits (~6.5s), with smooth 1.1–1.3s cubic-bezier transitions and staggered delays.

### Scroll Animations
- Classes: `.reveal`, `.reveal-left`, `.reveal-right`, `.reveal-up`, `.reveal-scale`, `.reveal-fade`
- Triggered by IntersectionObserver; adds `.revealed` class
- 1.2s transitions with `cubic-bezier(0.16, 1, 0.3, 1)` premium easing
- Delay utilities: `.delay-50` through `.delay-500`

### Count-Up Numbers
- Stat elements use `class="count-up" data-count="68" data-suffix="+"`
- Animated via `requestAnimationFrame` with easeOut cubic curve when scrolled into view

### Other Animations
- Dealer accordion: auto-rotates every 4s, supports drag/swipe/hover
- Achievement & testimonial sliders with fade transitions
- Floating header that pills/hides on scroll
- Dark mode toggle with smooth theme transitions

## Workflow
- **Start application**: `python3 -m http.server 5000`
