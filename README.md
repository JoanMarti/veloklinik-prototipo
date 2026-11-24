# VeloKliniK — Website Prototype

An interactive, client-ready prototype of a redesigned [velo-klinik.ch](https://velo-klinik.ch/), built to be shown to the client.

**Live demo:** https://joanmarti.github.io/veloklinik-prototipo/

Repository: https://github.com/JoanMarti/veloklinik-prototipo

## What it includes

- **Hero** with a large workshop photo, booking call to action and key figures, followed by a ticker of bike types.
- **Service finder.** A three-question quiz (how the bike is used, when it was last serviced, bike type) that recommends a package and shows it as a "diagnosis ticket" linking to online booking.
- **Packages.** Bronze, Silver, Gold and Platinum with prices and service intervals; the package recommended by the finder is highlighted. Includes a link to the price list.
- **Extras.** Test and rental (coming soon), repair course and upgrades.
- **Locations.** Europaallee Zürich HB, Altstetten Zürich and Sattel Schwyz, each with a photo, live open/closed status from the visitor's browser clock, and buttons for directions and booking.
- **Process and trust.** A four-step walkthrough (drop-off, estimate, repair, pick-up) and a reviews block.
- **Newsletter.** An integrated sign-up section with e-mail validation, consent checkbox and topic chips.
- Four languages: German (default), French, Italian and English.
- Responsive layout: on mobile the workshop cards and the service packages become swipeable carousels with dot navigation. No dependencies and no build step.

## Newsletter setup

The form works in demo mode by default: it validates the input and shows a confirmation, but **stores nothing**. To collect real sign-ups, set the `NEWSLETTER_ENDPOINT` constant in the second `<script>` block of `index.html` to a URL that accepts a JSON `POST` (for example a Brevo, Mailchimp or Formspree endpoint, or your own backend). Also add a link to the real privacy policy next to the consent checkbox.

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
