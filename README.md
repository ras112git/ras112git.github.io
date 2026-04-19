# Personal Portfolio — GitHub Pages

A single-file portfolio website (`index.html`) ready to deploy on GitHub Pages.

## Deploy in 5 minutes

1. **Create a new repository** on GitHub.
   - For a site at `https://<username>.github.io/` → name it exactly `<username>.github.io`.
   - For a site at `https://<username>.github.io/portfolio/` → any name works (e.g. `portfolio`).

2. **Push this file** to the repo:
   ```bash
   git init
   git add index.html README.md
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to your repo → **Settings** → **Pages**
   - Under *Build and deployment*, set **Source** to `Deploy from a branch`
   - Select branch `main`, folder `/ (root)`, and click **Save**
   - Wait ~1 minute, then visit your URL

## Adding your photo

The hero expects a file at `assets/photo.jpg` — create an `assets/` folder next to `index.html` and put the photo inside it.

1. Pick a portrait photo — ideally at least 720×900 px (4:5 ratio works best), good lighting, professional framing.
2. Name it `photo.jpg` and place it at `assets/photo.jpg`.
3. Commit and push. The photo is displayed as a clean rectangle with a subtle desaturation effect that restores to full color on hover.

If your file is `.png` or `.webp`, either rename it or change the `src="assets/photo.jpg"` attribute in the `<img class="portrait">` tag inside `index.html`.

Tip: export the photo at around 800×1000 px at 80–85% JPEG quality — plenty for the portrait display and keeps the file under ~150 KB.

## What to customize

Open `index.html` and search/replace these placeholders:

| Placeholder | Where |
|---|---|
| Hero subtitle | `<section class="hero">` — edit the `.hero-sub` paragraph |
| About text (3 paragraphs) | `<section id="about">` |
| Project cards (4 of them) | `<section id="projects">` — update title, description, tags, and `href` to point to each repo/case study |
| Skill lists | `<section id="skills">` — edit the `<li>` entries |
| Work experience | `<section id="experience">` — update dates, roles, companies |
| Email | `mailto:you@example.com` |
| LinkedIn URL | `linkedin.com/in/yourname` |
| GitHub URL | `github.com/yourusername` |
| Résumé link | `/resume.pdf` — drop a `resume.pdf` into the repo root |

## Changing the accent color

In the CSS `:root` block near the top, change:
```css
--accent: #ff4d1f;        /* main accent */
--accent-soft: #fff1ec;   /* soft tint for backgrounds */
```
Any solid hex works — try `#0066ff` (blue), `#0a7d4f` (green), `#7c3aed` (violet), etc.

## Adding a custom domain (optional)

1. Add a file named `CNAME` in the repo root with just your domain (e.g. `raul.dev`).
2. In your domain registrar, add a `CNAME` record pointing to `<username>.github.io`.
3. GitHub Pages will provision HTTPS automatically.

## Notes

- Everything is in one file — no build step, no frameworks.
- Fonts load from Google Fonts (Plus Jakarta Sans, Instrument Serif, JetBrains Mono).
- Responsive down to ~380px width.
