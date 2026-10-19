# VeloKliniK — UX Improvement Prototype

An interactive prototype presenting three user-experience improvements for the current [velo-klinik.ch](https://velo-klinik.ch/) website, built to be shown to the client.

**Live demo:** https://joanmarti.github.io/veloklinik-prototipo/

Repository: https://github.com/JoanMarti/veloklinik-prototipo

## The three ideas

1. **Interactive service finder.** A three-question quiz (how the bike is used, when it was last serviced, bike type) that recommends the Bronze, Silver, Gold or Platinum package with its price, presented as a "diagnosis ticket" that links to online booking.
2. **Live workshop locations.** The three workshops (Europaallee Zürich HB, Altstetten Zürich and Sattel Schwyz) show whether they are open right now, based on the visitor's browser clock, with direct buttons for directions and booking.
3. **Process and trust.** A four-step walkthrough (drop-off, estimate, repair, pick-up) and a reviews block to reduce the uncertainty of leaving a bike with a new workshop.

## Features

- Full-screen hero with a workshop photo.
- Four languages: German (default), French, Italian and English, with a switcher in the top bar.
- Responsive layout for mobile.
- No dependencies and no build step: a single `index.html` plus the `assets/` folder.

## Project structure

```
index.html          Full page (HTML, CSS and JavaScript)
README.md           This file
assets/
  hero.jpg          Hero photo (reference)
  europaallee.jpg   Photo of the Europaallee workshop
  altstetten.jpg    Photo of the Altstetten workshop
  sattel.jpg        Photo of the Sattel workshop
```

## Run locally

Open `index.html` in a browser. To serve it from a local web server instead:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Sample data

- **Packages, prices and addresses** are taken from the current VeloKliniK website.
- **Opening hours** for each workshop are sample values, not the real ones.
- **Reviews** are fictional texts labelled as examples and should be replaced with real Google reviews.
- **Photos** are visual references for the prototype. The hero photo shows another workshop, and the workshop photos come from Google Maps or screenshots, so they should be replaced with VeloKliniK's own photos before any final release.

## Deployment

The site is served with GitHub Pages from the `main` branch, root folder. To enable it: **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`**. The public URL is `https://joanmarti.github.io/veloklinik-prototipo/`.

## Updating the site

Edit `index.html` or replace the images in `assets/` (keeping the file names), then commit and push to `main`. GitHub Pages republishes automatically within a minute or two.
