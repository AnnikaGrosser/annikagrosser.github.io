# Portfolio

Static HTML/CSS portfolio. No build step: GitHub Pages serves the files as-is.

```
index.html            home page: bio, project list, toolkit
style.css             all styling (colors/fonts are tokens at the top)
projects/project-N.html   one methodology page per project
images/               headshot + one folder per project (images/project-1/thumb.jpg, hero.jpg …)
cv.pdf                add your CV here (linked from the nav)
.nojekyll             tells GitHub Pages not to run Jekyll
```

## Add a project
1. Copy `projects/project-1.html` to `projects/my-new-slug.html` and fill it in.
2. In `index.html`, copy one `<a class="project">…</a>` block and point `href` at the new page.
3. Put images in `images/my-new-slug/`. Swap the `thumb-placeholder` divs for
   `<img class="thumb" src="images/my-new-slug/thumb.jpg" alt="…">` (home page) or a `<figure>` (project page).
4. Update the "next:" link at the bottom of each project page so they chain together.

## Preview locally
```
python3 -m http.server 8000
```
Then open http://localhost:8000.

## Deploy to GitHub Pages
1. Create a public repo named **`<your-username>.github.io`** on GitHub.
2. From this folder:
   ```
   git init && git add . && git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. On GitHub, go to repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main` / root.
4. The site goes live at `https://<your-username>.github.io` within a minute or two.
