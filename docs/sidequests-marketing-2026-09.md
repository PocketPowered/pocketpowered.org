# Sidequests capture-led website refresh — September 2026

The promotional page uses the approved pigeon-with-camera icon and current native app screenshots from PocketPowered/sidequests-nyc commit 6ec3ffb, `assets/marketing/2026-09/`. Source kit: https://drive.google.com/drive/folders/1udUYwoqBscEWcggLTtHRU3mjTh1l0yRM

The lead sequence is capture → requirement-by-requirement grading → completed find. Pack and profile screenshots support the sequence. The page retains existing beta enrollment, email signup, legal links, and pack artwork.

## Asset provenance

`public/sidequests/assets/marketing-2026-09/` contains web-sized derivatives of the existing approved material. Native iPhone screenshots are resized to 660 × 1434 WebP (quality 86); the pigeon icon is 224 × 224 WebP (quality 90). The Play feature graphic is copied without alteration for social previews. No customer data is pictured.

Screens show production app UI rendered in an isolated marketing harness using a sample photo and deterministic demo grading. They are not evidence of a live camera session or backend grading call. The page labels them as demo results. Water tower photo: Martin Thoma, July 8, 2014, CC0, https://commons.wikimedia.org/wiki/File:Water-Tower-in-NYC-1.jpg

Source mapping:

- `01-capture.webp` ← `raw/iphone/01-capture.png`
- `02-verdict.webp` ← `raw/iphone/04-verdict.png`
- `03-result.webp` ← `raw/iphone/05-result.png`
- `06-pack.webp` ← `raw/iphone/02-pack.png`
- `07-profile.webp` ← `raw/iphone/05-profile.png`
- `pigeon-icon.webp` ← `app-icon-1024.png`
- `play-feature-graphic.png` ← same-named source

## Deployment context

At update time, origin/main (bed70e5) differs from the current production snapshot (5502b21 plus the existing Google verification meta tag). The local website checkout also contains unrelated uncommitted work. This PR is intentionally based on origin/main and changes only the Sidequests page, scoped stylesheet, assets, and this note.

For the authorized direct website publish, these changes are overlaid on a copy of the current production snapshot, retaining its BrandMark header and favicon. The output comparison against that production artifact shows exactly one changed existing file (`sidequests/index.html`), eight new Sidequests assets/styles, and no deleted files. Other pages, functions, routes, headers, and verification files are preserved. A future deployment from main should first reconcile the existing production snapshot with main to avoid reverting the studio's earlier unpublished changes.

Validation: Astro check; 35 existing tests; production build; local-link validation; Impeccable detector (no findings); desktop and mobile browser inspection, walkthrough controls, and access CTA.
