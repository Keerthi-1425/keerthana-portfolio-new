# Keerthana Bathini — Portfolio Website

Personal portfolio site for Keerthana Bathini, Software Engineer.

Built as a static site (HTML, CSS, vanilla JS) — no build step required, ready to deploy to GitHub Pages.

## File Structure

```
.
├── index.html         # Main portfolio page
├── 404.html           # Custom not-found page
├── style.css          # All styles
├── script.js          # Mobile menu + scroll fade-in
├── .nojekyll          # Tells GitHub Pages to skip Jekyll processing
├── README.md          # This file
└── assets/
    ├── resume.pdf     # Resume (linked from the Download Resume button)
    └── profile.jpg    # Your portrait — YOU NEED TO ADD THIS (see below)
```

## Before You Deploy: Add Your Photo

The site references `assets/profile.jpg` for the hero portrait. Drop your photo file at that exact path and name. If the file is missing, the page falls back to a styled "KB" placeholder so the layout doesn't break.

Recommended: a square crop, ~600×600 px or larger, JPEG or PNG (rename to `.jpg`).

## Deploy to GitHub Pages — Step-by-Step

Your GitHub username: **keerthi-1425**

You have two options. Option 1 gives you a "user site" at `https://keerthi-1425.github.io` — the cleanest URL. Option 2 is a "project site" at `https://keerthi-1425.github.io/<repo-name>/` if you'd rather keep your username site free for something else.

### Option 1 — User site at `keerthi-1425.github.io` (recommended)

1. On GitHub, create a new public repository named **exactly** `keerthi-1425.github.io`. Don't initialize it with a README.
2. From a terminal in the folder containing these files:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/keerthi-1425/keerthi-1425.github.io.git
   git push -u origin main
   ```
3. On GitHub, open the repo → **Settings** → **Pages**. Under "Build and deployment", set the source to **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. Wait 1–2 minutes, then visit **https://keerthi-1425.github.io**.

### Option 2 — Project site at `keerthi-1425.github.io/portfolio`

1. Create a public repo with any name, e.g. `portfolio`.
2. Push the same way as above:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/keerthi-1425/portfolio.git
   git push -u origin main
   ```
3. **Settings** → **Pages** → Source: **Deploy from a branch**, branch **main**, folder **/ (root)**.
4. The site will live at **https://keerthi-1425.github.io/portfolio/**.

## Local Preview

To check the site before pushing, just open `index.html` in a browser — it works as a plain file. For a closer-to-real experience, run a tiny local server:

```bash
# Python 3
python -m http.server 8000
# then open http://localhost:8000
```

## Customizing the Content

Most edits are plain text in `index.html`:

- **Hero tagline** — edit the `<p class="hero-tagline">` text inside `<section id="hero">`.
- **Projects** — there are 3 placeholder cards in `<section id="projects">`. Replace the titles, stacks, descriptions, and links (`href="#"`) with your real projects and GitHub URLs.
- **Contact links** — already filled in with your email, phone, location, and GitHub.
- **Colors** — change the CSS variables at the top of `style.css` (`--color-primary`, `--color-accent`, etc.).

## What's Included

- Sticky top navigation with smooth scroll
- Hero section with photo + intro + CTA buttons
- About section
- Skills grid (8 categories pulled from your resume)
- Experience timeline (MetLife + Rlogical Techsoft)
- Projects section (3 placeholder cards — fill these in)
- Education (UH + NIT Warangal)
- Contact cards (email, phone, location, GitHub)
- Resume download button (top hero + bottom contact)
- Mobile-responsive layout
- Custom 404 page

## Tech

Pure static — no frameworks, no build step. Just HTML, CSS, and a small JS file. Loads fast, ranks well, and is easy to maintain.