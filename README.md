# Pannellum (minimal)

WebGL panorama viewer with a single full-page demo. Based on [Pannellum](https://github.com/mpetroff/pannellum) (MIT).

## Run locally

From this directory:

```bash
python3 -m http.server
```

Open [http://localhost:8000/](http://localhost:8000/). A local server is required (browsers block panoramas from `file://`).

## Layout

| Path | Purpose |
|------|---------|
| `index.html` | Full-page iframe into the standalone viewer |
| `assets/` | Demo equirectangular image + preview |
| `src/` | Viewer: `js/`, `css/`, `standalone/` |

Swap in your own panoramas by changing the `panorama` / `preview` parameters in `index.html` (paths are relative to `src/standalone/pannellum.htm`).

## License

See `COPYING` (MIT). Pannellum is © Matthew Petroff and contributors.
