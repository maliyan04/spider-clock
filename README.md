# 🕷️ Spider Clock

A realistic animated spider that tells the real time. The spider sits at the center of a dew-covered web, and three of its legs are the clock hands.

**Live demo:** https://maliyan04.github.io/spider-clock/

## Features

- **Real-time clock:** always shows your device's current time
- **Legs as hands:** each hand is a jointed, hairy spider leg
  - 🟡 **Hours:** short, thick leg
  - 🔵 **Minutes:** long leg
  - 🔴 **Seconds:** thin leg that steps once per second with a small bounce
- **Realistic spider:** shaded body, 8 eyes, fangs, fuzzy hair, and a breathing abdomen
- **Living details:** the other five legs wiggle on their own
- **Detailed dial:** spiral web with dew drops, numbered badges, and minute tick marks
- **Light and dark mode:** follows your device theme automatically
- **"How to read the clock" button:** opens a small legend for first-time viewers
- **Responsive:** works on phones, tablets, and desktops

## Getting started

No install or build step is needed.

1. Download `index.html`.
2. Open it in any modern browser.

To host it free with GitHub Pages, go to **Settings → Pages**, choose the `main` branch, and save.

## Tech

Plain HTML, CSS, and JavaScript in a single file, with no libraries. The clock is drawn as SVG and animated with `requestAnimationFrame`.

## Customize

Colors and sizes are easy to change:

| What | Where |
|------|-------|
| Hand colors, spider colors, background | CSS variables at the top of the `<style>` block (`--hr`, `--min`, `--sec`, `--leg`, ...) |
| Hand lengths | `setLeg(...)` calls inside `tick()` (hour `80`, minute `128`, second `152`) |
| Second-hand movement | `step` in `tick()`. Use `s * 6` instead for a smooth sweep |
| Web density and dew drops | The spiral loop near the top of the script (`N` and the dew condition) |

## Browser support

Chrome, Edge, Firefox, and Safari (current versions).

## License

MIT. Free to use and modify.
