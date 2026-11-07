# Jonas Risbrandt

Source for [jonasrisbrandt.github.io](https://jonasrisbrandt.github.io/), my personal landing page.

The page introduces my programming background, my commercial products and selected side projects, with links to GitHub and LinkedIn. It is a single self-contained HTML file with inline CSS and JavaScript, and no package installation or build step.

The hero is an amber CRT screen rendered by a WebGL2 fragment shader: a ray-marched twisted torus that twists and billows at random moments, a scrolling grid floor, and a sine scroller drawn on the curved glass. The scroller text is rendered to a texture and clipped to the content column.

Performance: ray-marching only runs inside a bounding sphere around the object, the canvas stays within a pixel budget (lower on touch devices), resolution adapts to measured frame times, the shader compiles in the background where supported, and rendering pauses while the hero is off-screen or the tab is hidden. Reduced-motion users get a single still frame. Without WebGL2 the page falls back to a static gradient.

## Preview

From the repository root:

```sh
python -m http.server 8080 --bind 127.0.0.1
```

Open http://127.0.0.1:8080/.

## Publishing

GitHub Pages publishes the repository root from `master`. Commit and push changes to that branch.

## Files

- `index.html`: visible content, styles, the hero shader and its runner, title/description, canonical URL, social metadata and ProfilePage/Person JSON-LD. Experience years are derived from the start years (1986 and 1998) at runtime; the HTML carries the current values for crawlers.
- `assets/favicon.svg`: site icon.
- `robots.txt`: crawler access and sitemap location.
- `sitemap.xml`: the current personal landing page. Update `lastmod` only when the page changes meaningfully.

The earlier homepages remain recoverable in Git history. Other existing experiment pages and their assets are retained.

## Search discovery

All profile content and metadata are served in HTML. Search engines do not need to run JavaScript; the shader is decoration only. The canonical URL is `https://jonasrisbrandt.github.io/`.

After verifying this GitHub Pages URL-prefix property in Google Search Console, submit `sitemap.xml` and inspect the homepage. This does not provide ownership of the separate `github.com/jonasrisbrandt` profile. Search indexing and rankings remain up to search engines.
