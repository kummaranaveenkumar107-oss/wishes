# Durgabhavani Birthday Website — Premium Edition 🎂💗

A more elegant, "keepsake card" take on the birthday page: a medallion-framed
photo, a gold-and-plum palette, an unfolding letter, flip-card wishes, and a
polaroid-style gallery. Pure HTML5, CSS3, and vanilla JavaScript — no build
step, no dependencies, no backend. Works by opening `index.html` directly in
a browser, and deploys cleanly to **Render** or **GitHub Pages**.

## Project structure

```
durgabhavani-birthday/
├── index.html
├── render.yaml
├── README.md
└── assets/
    ├── birthday-gift.png
    └── birthday-teddy.png
```

## Deploy on Render (recommended)

1. Create a new **GitHub repository** (public or private).
2. Upload the contents of this folder to the repository root:
   - `index.html`
   - `render.yaml`
   - the `assets/` folder
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

(Render may append a few random characters if that exact name is taken.)

## Deploy on GitHub Pages (alternative)

1. Create a **public** GitHub repository.
2. Upload `index.html` and the `assets/` folder (keep the folder structure).
3. Go to **Settings → Pages**.
4. Choose **Deploy from a branch → main → / (root)** and save.
5. Your public link will look like:

```
https://YOUR-USERNAME.github.io/durgabhavani-birthday/
```

## Notes

- Fonts (Playfair Display, Dancing Script, Quicksand) load from Google Fonts
  over a standard `<link>` tag — this needs an internet connection but is not
  a backend/API dependency, so it deploys fine on Render or GitHub Pages.
- All images are local (`./assets/...`) — nothing else is loaded externally.
- The countdown targets the next September 30 in the visitor's own timezone
  and switches to a "It's Your Birthday! 🎉" banner on the day itself.
- No environment variables, database, or server are required.
