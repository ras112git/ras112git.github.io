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

The hero expects a file called `photo.jpg` in the **same folder as `index.html`** (the repo root).

1. Pick a square photo of yourself — ideally at least 720×720 px, good lighting, shoulders visible.
2. Rename it to `photo.jpg` and drop it into the repo root.
3. Commit and push. The circular crop happens automatically via CSS.

If your file is `.png` or `.webp`, either rename it or change the `src="photo.jpg"` attribute in the `<img class="portrait">` tag inside `index.html`.

Tip: to keep the repo small, export the photo at around 800×800 px at 80–85% JPEG quality — that's plenty for a circular avatar and keeps the file under ~100 KB.

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
