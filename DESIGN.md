# Motion Studies — Design Brief

Source reference: Instagram reel (DetWpkASgsT) — a showreel of UI animations made in code:
a dark music-player card with a live scrubber, spring-physics toggle switches, an animated
view-count chart. This page recreates those motion kinds as working demos, not mockups.

## Hard rules
- Palette: warm paper `#F4F1EA` (never pure white), ink `#141310`, ONE accent — signal
  orange `#FF4D00`. Dark cards `#131311`. No gradients on text, no purple/blue radial
  gradients, no glowing orbs, no liquid glass.
- Type: Bricolage Grotesque (display, 700/800), Archivo (body 400/500/600),
  IBM Plex Mono (labels/readouts). No Inter, no Space Grotesk.
- Layout: EDITORIAL. Magazine-style varied composition, left-aligned headlines, varied
  widths, generous negative space, hairline rules, mono micro-labels ("MOTION STUDY —
  PLAYER"). No uniform card grid, no centered hero template, no "01/02/03" numbered
  headers, no pill buttons (small-radius rectangles), no checkmark bullets, no fake
  testimonials or logos.
- Icons are pure graphics — never letters/words inside icon shapes.

## Stack
- One file: `index.html`. Vanilla HTML/CSS/JS + GSAP 3 + ScrollTrigger (cdnjs CDN).
- Initial states are set BY GSAP, never hidden in CSS — if GSAP fails, content is visible.
- `prefers-reduced-motion`: heavy animation disabled, final states shown.
- Mobile-first, no horizontal scroll, touch targets ≥ 44px, no device-type gating.

## Studies (all live, all functional)
- HERO — kinetic type: "MOTION" letters spring in (GSAP stagger); rotating word ticker
  (springs / kinetics / easing / physics); signature scroll moment — hero word scales and
  is clip-path-cropped under ScrollTrigger scrub; accent scroll-progress bar on top.
- PLAYER — dark card recreating the reel's: WebAudio-synthesized looping arpeggio (no
  audio files), play/pause morph, real-time progress over a 2:59 track, draggable scrubber
  (pointer events, touch included), live elapsed / remaining counters, ±30s / restart
  skips, analyser-driven equalizer bars and album-tile canvas.
- SPRINGS — three working toggles on a custom spring integrator: status readout switch,
  day/night switch that actually themes its panel, gravity switch that drops and bounces
  a ball with restitution physics.
- DATA — count-up to 84,320 views on scroll into view; SVG line/area chart that draws
  itself with a travelling dot; 7 spring-grown day bars; pointer scrub crosshair with a
  live readout.
- BUTTONS & FEEDBACK — magnetic button, add-to-list with morph + real list append,
  like button with particle burst + counter, springy toast with working dismiss.
- REVEALS & LOADERS — skeleton/content toggle card, spring-height accordion (one open),
  scroll-triggered staggered spring-rise text blocks.
- MARQUEE — infinite CSS strip: "KINETIC TYPE — SPRING PHYSICS — 60 FPS — MADE IN
  CODE —", paused under reduced motion.
- FOOTER — mono line: "Motion studies. Built as a single HTML file. Every animation on
  this page is live."
