# Durgabhavani Birthday Website — Self-Contained Edition 🎂💗

This version is a **single HTML file**. Both images are embedded directly
inside `index.html` as base64 data — there is no `assets` folder and no
separate image files, so there are no broken image paths after deployment.
Pure HTML5, CSS3, and vanilla JavaScript. No build step, no dependencies,
no backend.

## Project structure

```
durgabhavani-birthday/
├── index.html   ← everything (HTML + CSS + JS + both images) lives in here
├── render.yaml
└── README.md
```

## Deploy on Render (recommended)

1. Create a new **GitHub repository** (public or private).
2. Upload `index.html` and `render.yaml` to the repository root.
3. Go to [render.com](https://render.com) and log in.
4. Click **New +** → **Static Site**.
5. Connect your GitHub account and select this repository.
6. Select the **main** branch.
7. Leave **Build Command** empty.
8. Set **Publish Directory** to `.` (also pre-filled via `render.yaml`).
9. Click **Create Static Site** / **Deploy**.

Your live link will look like:

```
https://durgabhavani-birthday.onrender.com
```

## Deploy on GitHub Pages (alternative)

1. Create a **public** GitHub repository.
2. Upload `index.html`.
3. Go to **Settings → Pages**.
4. Choose **Deploy from a branch → main → / (root)** and save.
5. Your public link will look like:

```
https://YOUR-USERNAME.github.io/durgabhavani-birthday/
```

## Why this fixes "images not displaying"

The earlier version referenced `./assets/birthday-gift.png` and
`./assets/birthday-teddy.png` as separate files. If those files weren't
uploaded to the exact same relative location on GitHub (or the repo
structure got flattened during upload), the images would break. This
version has no external image files at all — the pictures are baked
directly into the page code, so as long as `index.html` loads, the images
load with it, on any host.

## Notes

- Fonts (Playfair Display, Dancing Script, Quicksand) still load from Google
  Fonts over a standard `<link>` tag — this needs an internet connection but
  is not a backend/API dependency.
- The file is larger than before (~1.2 MB) because the images are embedded
  as text inside the HTML, but it still loads fast on any normal connection.
- The countdown targets the next September 30 in the visitor's own timezone
  and switches to a "It's Your Birthday! 🎉" banner on the day itself.
