# Compute Tycoon developer website

Public website for Compute Tycoon: Idle AI Game by Kevin Mok, with App Store and Google Play downloads. Static HTML/CSS with local game artwork and fonts. No JavaScript, analytics, cookies, or build dependencies.

## Preview

Run `python3 -m http.server 4173` in this directory, then open http://localhost:4173.

## Publication

The GitHub Actions workflow publishes only the website files and assets to GitHub Pages. Repository settings → Pages → Source must be GitHub Actions.

Live website: https://mightyjuke.github.io/data-center-typhoon-public/

Developer root: https://mightyjuke.github.io/

## AdMob requirement

This project contains the verified `app-ads.txt` record. For a GitHub Pages project URL, AdMob checks **https://mightyjuke.github.io/app-ads.txt**, not the project subfolder. That root file is published from the companion repository https://github.com/mightyjuke/mightyjuke.github.io and was verified to return HTTP 200, `text/plain; charset=utf-8`, and the exact publisher record on September 15, 2026.

After the root URL serves the exact record with HTTP 200, set the App Store **Marketing URL** to the public developer website and request an AdMob update. Website deployment alone does not establish AdMob verification. See https://support.google.com/admob/answer/9363762.

Use `https://mightyjuke.github.io/data-center-typhoon-public/` as the Marketing URL. App Store metadata was not changed by this website deployment.

## Content

The site links to the existing Medium privacy policy. It does not change the game's privacy disclosures. Screenshots and campus artwork are from the companion game repository. Outfit's license is included in `assets/OFL.txt`.

### Version 2 imagery

The September 21, 2026 refresh adds v2 campaign artwork and current in-game campus and gameplay captures. Captions distinguish the campaign illustration from actual gameplay; gameplay images link to their full-size local files. Images use optimized local WebP, with a JPEG for social sharing. The page retains native links and disclosures and works without JavaScript.

All paths below are relative to the companion `data-center-typhoon` repository; output files live in this site's `assets/` directory.

| Website asset | Source |
| --- | --- |
| `v2-campaign.webp`, `v2-campaign-small.webp`, `v2-share.jpg` | `docs/store/google-play-2026-09-21/masters/feature-original.png` |
| `v2-campus.webp` | `docs/validation/campus-atmosphere/01-campus-overview.png` |
| `v2-research.webp` | `docs/validation/campus-atmosphere/03-research-link-gardens.png` |
| `v2-cooling.webp` | `docs/validation/cooling-infrastructure/02-cooling-plant.png` |
| `v2-logistics.webp` | `docs/validation/dock-logistics/04-order-cargo-handoff.png` |
| `v2-build.webp` | `docs/store/google-play-2026-09-21/sources/phone-01-build.png` |
| `v2-contracts.webp` | `docs/store/google-play-2026-09-21/sources/phone-03-contracts.png` |
| `v2-crew.webp` | `docs/store/google-play-2026-09-21/sources/phone-04-crew.png` |

Assets were mechanically resized and converted from these existing sources; no new scenes were generated. The refresh extends the existing visual system recorded in `DESIGN.md` and `.impeccable/design.json`.
