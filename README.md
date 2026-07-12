# France d'Agrain — Academic Website

Personal academic website (static HTML/CSS) for France d'Agrain, PhD candidate in
Economics at CERNA, Mines de Paris – PSL.

## Structure

```
index.html        Home
research.html     Working Papers + Work in Progress
cv.html           CV summary (+ link to CV.pdf)
seminars.html     Seminars & Conferences
teaching.html     Teaching
media.html        Media / press
assets/style.css  Shared stylesheet
CV.pdf            Downloadable CV
photo_CV_londres.jpg   Portrait used on the home page
```

No build step, no dependencies — plain HTML and one CSS file (fonts loaded from Google Fonts).

## Editing

- **Papers, seminars, teaching, media:** open the relevant `.html` file and duplicate an
  existing block (`<article class="paper">` or `<div class="entry">`), then edit the text.
- **Links marked `href="#"`** are placeholders — replace them with real URLs (PDF, The
  Conversation article, etc.).
- **Colors / fonts:** edit the variables at the top of `assets/style.css`.

## Publishing on GitHub Pages

1. Create a repository on GitHub. To get the address `https://france-dagrain.github.io/`,
   name the repo **`france-dagrain.github.io`**. For a project page
   (`https://<user>.github.io/france-dagrain/`), name it **`france-dagrain`**.
2. Push these files to the repository, e.g.:

   ```bash
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin https://github.com/<user>/<repo>.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment → Source: “Deploy from a branch”**,
   branch **`main`**, folder **`/ (root)`**. Save.
4. Wait ~1 minute; the site goes live at the URL shown on the Pages settings screen.

The `.nojekyll` file tells GitHub Pages to serve the files as-is (no Jekyll processing).
