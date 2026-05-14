# PargaDreams.com — Pasha Villas

Static site for Pasha Villas: 6 contemporary villas in Trikoryfo, Parga, Greece.

## Page map

| URL                | File                          |
|--------------------|-------------------------------|
| `/`                | `index.html`                  |
| `/pasha-villas/`   | `pasha-villas/index.html`     |
| `/floor-plans/`    | `floor-plans/index.html`      |
| `/gallery/`        | `gallery/index.html`          |
| `/investment/`     | `investment/index.html`       |
| `/location/`       | `location/index.html`         |

Anchor links (`/#investment`, `/#location`, `/#floorplans`, `/#gallery`) jump to
sections on the homepage — all four IDs confirmed present.

## Deploy

Push to GitHub → Vercel auto-deploys on every commit to `main`.
`vercel.json` enables clean URLs and adds basic security headers.

## Stack

Plain static HTML. Images are currently embedded as base64 inside the HTML
(no external image folder). See note below about file sizes.

## File-size note

`index.html` is ~57 MB and `gallery/index.html` is ~32 MB because every image
is base64-encoded inline. The site will deploy and work, but Core Web Vitals
will fail and mobile load times will be slow. Plan a follow-up to extract
images to a `/images/` folder and reference them by URL.
