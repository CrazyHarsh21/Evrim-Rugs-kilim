# Evrim Rugs

A luxury rug archive website with a hand-woven logo preloader and a rotating product showcase.

## Preview locally

Open a terminal in this folder and run:

```powershell
& 'C:\Users\CrazyHarsh\.cache\codex-runtimes\codex-primary-runtime\dependencies\python\python.exe' -m http.server 4174 --bind 127.0.0.1
```

Then visit `http://localhost:4174`.

Alternatively, `npm start` (or `npm run dev`) launches the included `server.js` (Express) on its configured port.

## Deploy to Vercel

This is a static site—no build command or framework preset is required.

1. Push the contents of this folder to the root of a GitHub repository.
2. In Vercel, choose **Add New → Project** and import that repository.
3. Select the **Other** framework preset; leave the build command blank and set the output directory to `.`.
4. Deploy. Vercel automatically serves `index.html` and applies the cache headers in `vercel.json`.

## Project structure

```text
evrim-rugs/
├── index.html       # Website, styles, logo preloader, and GSAP animations
├── assets/          # Logo, favicons, and gallery images
└── README.md
```

## Features

- Museum-style rug archive with collection, provenance, motifs, and inquiry sections.
- A GSAP-driven logo preloader: the Evrim Rugs mark weaves in, then curtains slide away to reveal the homepage.
- A live `CRAFTING THE EXPERIENCE — 0–100%` progress label.
- A rotating hero specimen showcase and a 14-item spotlight carousel with smooth CSS-transition progress bars and sliding image transitions.
- Reduced-motion support: the preloader exits quickly without the full animation.

## Customization

- Swap `assets/images/evrim_rugs_logo.png` to update the logo everywhere (header, footer, and preloader).
- Update the `heroSpecimens` array and the carousel slide/thumbnail markup in `index.html` to change the showcased products.
- Change animation timing in the GSAP timelines near the end of `index.html`.

## Notes

The site loads GSAP, Tailwind CSS, and Google Fonts from public CDNs. An internet connection is needed for those external resources; the product images themselves are local.
