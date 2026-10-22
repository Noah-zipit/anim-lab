# Motion Studies — Live UI Animation Playground

A single-file playground of live, working UI animation: every animation on the
page is real and functional, not a mockup. Built with vanilla HTML/CSS/JS plus
GSAP 3 and ScrollTrigger (CDN) in one `index.html`.

**Design brief:** see [`DESIGN.md`](DESIGN.md) — warm paper palette with one
signal-orange accent, editorial layout, Bricolage Grotesque / Archivo /
IBM Plex Mono type.

## The studies

- **Hero** — kinetic type: the MOTION letters spring in with a GSAP stagger,
  a rotating word ticker (springs / kinetics / easing / physics), and a
  signature scroll moment where the hero word scales and is clip-path-cropped
  under ScrollTrigger scrub, with an accent scroll-progress bar on top.
- **Player** — a dark music-player card with a WebAudio-synthesized looping
  arpeggio and a live scrubber.
- **Springs** — toggle switches with real spring physics.
- **Data** — an animated view-count chart and numbers that count.
- **Buttons** — magnetic buttons and tactile feedback states.
- **Reveals** — scroll-triggered reveal studies.

## Notes

- Initial states are set by GSAP, never hidden in CSS — if GSAP fails, the
  content is still visible.
- `prefers-reduced-motion` disables the heavy animation and shows final states.
- Mobile-first: no horizontal scroll, touch targets at least 44px, no
  device-type gating.
- Icons are pure graphics — never letters or words inside icon shapes.

## Run it

Open `index.html` in a browser, or serve the folder with any static server:

```bash
npx serve .
```
