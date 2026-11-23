# تقرير الأداء وإمكانيات مستشفيات القاهرة

Interactive dashboard (Arabic, RTL) for 17 Cairo Health Directorate hospitals, July – October 2026.
A static site, so GitHub Pages can host it as-is. No build step is needed to publish.

## Publish on GitHub Pages
1. Create a new repository on GitHub, e.g. `cairo-hospitals-dashboard`.
2. Upload **all files in this folder** (drag them all at once).
3. Repo → **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)` → Save.
4. After ~1 minute the site is live at `https://<your-username>.github.io/cairo-hospitals-dashboard/`.

## Mobile
- Fully responsive; tap charts for tooltips, swipe tables sideways (first column stays pinned).
- "Add to Home Screen" installs it like an app (icon + full-screen).
- Shareable links: `#h=3` opens a specific hospital, `#compare` opens the comparison view.

## Editing
- Data lives in `HOSPITALS_DATA` inside `index.html`.
- If you add **new Tailwind classes**, rebuild the CSS:
  ```bash
  npm install
  npx tailwindcss -i tailwind.input.css -o styles.css --minify
  ```
