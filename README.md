# BJJ Timer & Scoreboard

A mobile-first single-page web app for BJJ coaching sessions.

It combines:
- Round timer (`countdown`, `count up`, `tabata`)
- Two-player scoring (`blue` / `white`)
- Large touch interactions for fast score updates
- Minimal Bauhaus-inspired UI for noisy training environments

## Why this project

This tool is designed for real coaching scenarios where you need to:
- keep eyes on the mat,
- operate quickly with one hand,
- avoid complex menus during live rolling.

## Features

- **3 timer modes**
  - Countdown
  - Count up
  - Tabata (work/rest/rounds)
- **BJJ scoring board**
  - Blue/White score display
  - Tap to add score
  - Configurable subtract gesture (double tap / long press)
- **Layouts**
  - Left/Right
  - Top/Bottom
- **Pre-start flow**
  - 3s / 5s ready phase
  - `FIGHT` transition
- **Audio/Haptic feedback**
  - Configurable sound preset
  - Optional vibration (if browser/device supports)
- **Mobile shortcut support**
  - `manifest.webmanifest`
  - App icons for home screen install

## Tech stack

- Plain HTML + CSS + Vanilla JavaScript
- Single-page, no framework, no bundler required

## Project structure

- `index.html` - main app (single-file runtime)
- `manifest.webmanifest` - PWA metadata
- `icons/` - app icons (`180`, `192`, `512`)
- `releases/` - packaged deployment zip files
- `docs/` - project notes and handoff docs

## Run locally

### Option 1: open directly
Double-click `index.html` in browser.

### Option 2: local server (recommended)
Use any static server so manifest/icons behave consistently:

```bash
npx serve .
```

## Deploy

### Netlify Drop (fastest)
1. Open [Netlify Drop](https://app.netlify.com/drop)
2. Drag a zip from `releases/`
3. Get a public HTTPS URL

### Netlify + GitHub (recommended)
1. Push this repository to GitHub
2. In Netlify: **Add new site -> Import from Git**
3. Select this repo
4. Build command: _(leave empty)_
5. Publish directory: `.`

## Install as app shortcut

### iOS (Safari)
1. Open deployed URL in Safari
2. Share -> **Add to Home Screen**

### Android (Chrome)
1. Open deployed URL
2. Menu -> **Add to Home screen** / **Install app**

## Notes

- Some haptics/audio policies vary by browser (especially iOS Chrome).
- For best iOS install behavior, use Safari for Add to Home Screen.

## License

This repository currently has no explicit license file.
Add one if you want others to reuse your code.
