# Compute Tycoon developer website

Public website for Compute Tycoon: Idle AI Game by Kevin Mok. Static HTML/CSS with local game artwork and fonts. No JavaScript, analytics, cookies, or build dependencies.

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
