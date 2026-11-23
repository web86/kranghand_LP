# Kranghand Design — Renovatie & Verbouwing Leiden

Landing page prototype for **complete interior renovation and remodeling in Leiden, Netherlands**, designed for Kranghand Design.

## Preview with GitHub Pages

The demo is a standalone HTML page at [`index.html`](./index.html).

To publish it through GitHub Pages:

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose **main** and **/(root)**, then press **Save**.
4. After deployment, open **https://web86.github.io/kranghand_LP/**.

> This GitHub Pages URL is the expected address **after** Pages has been enabled and deployment completed. The repository alone does not guarantee the public preview is live.

## Contents

- `index.html` — responsive Dutch landing page, including hero, services, portfolio, process, FAQ and contact CTA.
- `docs/MODX-implementation.md` — integration guidance for MODX 2 + Fenom + Localizator and production SEO considerations.

## Important notes

- **Draft only.** The preview contains `<meta name="robots" content="noindex,nofollow">`, intentionally excluding it from indexing as a duplicate of planned production content. Remove or change this only when publishing the *canonical* live version on `kranghanddesign.com`.
- The preview loads project images remotely from the Kranghand Design website. Their availability depends on the original server and image paths.
- Enquiry buttons currently navigate to the live Kranghand Design contact page; there is no embedded SendIt form in this static preview.
- Prices, guarantees, dates and geographical service promises should be approved by Nadia before public advertising.
- The production canonical URL is planned as `https://kranghanddesign.com/nl/renovatie-leiden`.

## Website

https://kranghanddesign.com/

## Design update — November 2026

The prototype now includes:

- A reduced monochrome palette and the main site's compact SVG favicon mark displayed alongside the studio name. The header uses a text fallback when the remote SVG is unavailable.
- A three-image project carousel with circular previous/next buttons, automatic transitions, keyboard access, reduced-motion support and pause on hover/focus.
- A link to the existing Google Business Profile, showing **4.7/5 from 3 reviews** as checked on 23 November 2026. These numbers are a static snapshot, **not** live Google API data: recheck periodically before production.
- An in-page contact **mockup** that accepts no submissions on GitHub Pages. The form blocks submission and directs visitors to the actual contact page; do not treat this as an active lead form.
- An address/contact panel with a Google Map iframe injected **only after the visitor clicks** “Kaart laden”. This is a standalone-preview consent gate; in MODX integrate with Cookie Consent Manager (External category) and ensure the embed and its Google link match the existing site.

### Production form integration

Copy the working SendIt form markup/configuration from the NL contact page **verbatim** into the landing-page template/chunk; retain `data-si-form`, `data-si-preset`, hidden fields/honeypot, `enctype` for attachments, CSRF measures, validation and any site-specific JS hooks. The prototype deliberately does not attempt to call live MODX AJAX endpoints from GitHub Pages because cross-origin/session/security policies make that brittle.

### Before going live

Verify the exact favicon URL, privacy-policy URL, real map location, approved user-facing wording, live Google review count, and form integration. The remote image URLs need confirmation and suitable production optimization. Keep the noindex directive for GitHub Pages; give the production page its own correct canonical and hreflang.
