# Pannellum (minimal)

WebGL panorama viewer with a multi-scene tour (bottom dots). Based on [Pannellum](https://github.com/mpetroff/pannellum) (MIT).

## Run locally

Install dependencies (once) and build the Tailwind stylesheet when you change `src/tailwind-input.css` or add Tailwind classes in `index.html`:

```bash
npm install
npm run build:css
```

Then serve the folder (a static server is required; browsers block panoramas from `file://`):

```bash
python3 -m http.server
```

Open [http://localhost:8000/](http://localhost:8000/). While editing styles, run `npm run watch:css` in another terminal to rebuild `assets/tailwind.css` automatically.

## Styling (Tailwind)

- **Source:** `src/tailwind-input.css` — `@import "tailwindcss"`, `@source` for `index.html`, and `@layer components` for the tour UI (dots, labels, Pannellum chrome overrides).
- **Built file:** `assets/tailwind.css` — linked from `index.html` after the Pannellum CSS files.

## Layout

| Path                     | Purpose                                                         |
| ------------------------ | --------------------------------------------------------------- |
| `index.html`             | Embeds the viewer, scene title overlay, dot navigation          |
| `tour.json`              | Tour: `scenes`, `sceneOrder`, `default.firstScene`, fade timing |
| `assets/`                | Demo panoramas, preview image, **built** `tailwind.css`         |
| `src/tailwind-input.css` | Tailwind entry (edit here, then `npm run build:css`)            |
| `src/`                   | Viewer: `js/`, `css/`, `standalone/`                            |

Edit `tour.json` to add scenes, titles, and panorama paths. The default starting scene is `default.firstScene` (currently `scene2`, “Ons laboratorium”).

## License

See `COPYING` (MIT). Pannellum is © Matthew Petroff and contributors.
