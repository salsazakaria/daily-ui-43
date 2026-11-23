# Salsa — Agent UI Kit (live bento)

**Live site:** https://daily-ui-43.netlify.app

A live, animated crypto & AI bento UI kit. Every card runs its own loop
(typing, swaps, approvals, toggles) over frosted glass on a looping tulip video.

Plain static site: no build step, no dependencies.

```
index.html            page, styles and animation (single file)
assets/fonts/         Geist + Geist Mono (woff2)
assets/video/         background + flower loops (WebM with MP4 fallback)
assets/img/           posters, avatar chip, favicon, social preview
netlify.toml          Netlify config (publish the repo root, asset caching)
```

## Run locally

```
python3 -m http.server 8000
# open http://localhost:8000
```

## Publish

1. Create an empty repo on GitHub, then from this folder:
   ```
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
2. On Netlify: **Add new site → Import an existing project → GitHub**, pick the repo.
   Leave the build command empty; the publish directory is `.` (already set in `netlify.toml`).
   Every push to `main` redeploys.

## Notes

- The 1920×1080 composition scales to fit any window, so it looks identical on any 16:9 screen.
- Visitors who have "reduce motion" turned on see a still frame.
