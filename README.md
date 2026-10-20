# Jonas Risbrandt

Source for [jonasrisbrandt.github.io](https://jonasrisbrandt.github.io/), my personal landing page.

The page introduces my programming background and links to selected public projects, GitHub and LinkedIn. It is plain HTML and CSS, with no JavaScript runtime, package installation or build step.

## Preview

From the repository root:

```sh
python -m http.server 8080 --bind 127.0.0.1
```

Open http://127.0.0.1:8080/.

## Publishing

GitHub Pages publishes the repository root from `master`. Commit and push changes to that branch.

## Files

- `index.html`: visible content, title/description, canonical URL, social metadata and ProfilePage/Person JSON-LD.
- `assets/profile.css`: responsive layout, focus styles and reduced-motion support.
- `assets/favicon.svg`: site icon.
- `robots.txt`: crawler access and sitemap location.
- `sitemap.xml`: the current personal landing page. Update `lastmod` only when the page changes meaningfully.

The earlier shader homepage remains recoverable in Git history. Other existing experiment pages and their assets are retained.

## Search discovery

All profile content and metadata are served in HTML. Search engines do not need to run JavaScript. The canonical URL is `https://jonasrisbrandt.github.io/`.

After verifying this GitHub Pages URL-prefix property in Google Search Console, submit `sitemap.xml` and inspect the homepage. This does not provide ownership of the separate `github.com/jonasrisbrandt` profile. Search indexing and rankings remain up to search engines.
