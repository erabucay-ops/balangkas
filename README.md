# BALANGKAS Planning Laboratory — Website

A single-page, self-contained website for the BALANGKAS Planning Laboratory
(DCERP · College of Human Ecology · UP Los Baños).

- `index.html` — the entire site (HTML + CSS + inline SVG logo). No build step, no dependencies.
- `assets/` — logo files (used for the social-share image; the page itself has the logo inlined).

## Deploy to GitHub Pages (temporary site)

**Option A — upload in the browser (easiest)**
1. Create a new repository on GitHub, e.g. `balangkas` (Public).
2. Click **Add file → Upload files**, drag in `index.html` and the `assets/` folder, then **Commit**.
3. Go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Branch: **main**, folder: **/ (root)**. Click **Save**.
6. Wait ~1 minute. Your site appears at:
   `https://<your-username>.github.io/<repo-name>/`

**Option B — command line**
```bash
git init
git add index.html assets
git commit -m "BALANGKAS website"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
# then enable Pages in Settings → Pages (main / root)
```

## Taking it down (it's temporary)
- **Unpublish:** Settings → Pages → set Source to **None**, or
- **Delete the repo:** Settings → (bottom) **Delete this repository**.

## Editing
- All text lives in `index.html` between the `<section>` tags — edit directly.
- Colors are CSS variables at the top of the `<style>` block
  (`--maroon #7B1113`, `--green #0C7A46`, `--gold #C79A3A`).
- The logo is inline SVG (search `viewBox="-130 -130`), so it stays crisp at any size.

## Notes
- The page uses a system font stack (no external fonts), so it loads fast and works offline.
- Objective 3 was lightly edited for grammar; see the comment in `index.html` if you want the original wording.
