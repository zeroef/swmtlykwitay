# swmtlykwitay

A fullscreen image slideshow static website.

## How it works

* Images are served from the `/images` folder.
* The slideshow reads `images/manifest.json` to know which images to display.
* Each image is shown fullscreen for **10 seconds** with a smooth fade transition.

## Adding new images

1. Drop your image files (`.jpg`, `.jpeg`, `.png`, `.gif`, `.webp`, `.avif`, `.svg`, `.bmp`) into the `images/` folder and push to `main`.
2. A GitHub Actions workflow automatically regenerates `images/manifest.json` and commits it back.
3. Reload the page — the new images will appear.

## Running locally

Because the page fetches `images/manifest.json`, you need to serve it over HTTP (opening `index.html` directly via `file://` won't work). Any simple HTTP server works, e.g.:

```bash
# Python 3
python3 -m http.server 8080
```

Then open <http://localhost:8080>.