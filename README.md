# Portfolio site

A single-file static site — no build step, no dependencies. Just `index.html`.

## Deploy to GitHub Pages (takes ~5 minutes)

1. Create a new GitHub repo (public), e.g. `yourname.github.io` for a root domain,
   or any name (e.g. `portfolio`) for a project page.
2. Push this folder's contents to the repo:
   ```
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Source → Deploy from a branch → main / (root)**.
4. Your site goes live at:
   - `https://YOUR_USERNAME.github.io` (if repo is named `YOUR_USERNAME.github.io`), or
   - `https://YOUR_USERNAME.github.io/YOUR_REPO` (any other repo name)

## Before you push

- Swap `you@example.com` in the Contact section for your real email (or a form/LinkedIn link).
- Update the four "Selected work" cards if you want different projects featured, or add more.
- Optional: add a custom domain via **Settings → Pages → Custom domain**.

## Editing the homepage

Layout, copy, and colors for the main page live in `index.html`. Shared styling for the whole
site (homepage + blog) lives in `assets/style.css`. No build tooling to run — edit and push,
GitHub Pages redeploys automatically within a minute or two.

## Adding a new blog post

1. Duplicate `blog/first-post.html` and rename it, e.g. `blog/my-new-post.html`.
2. Edit the title, date, and heading near the top of the file.
3. Replace the placeholder content in `<section class="post-body">` with your real post —
   plain HTML: `<p>` for paragraphs, `<h2>`/`<h3>` for subheadings, `<ul><li>` for lists.
4. Open `blog/index.html` and add a new `<article class="post-entry">` block near the top
   (most recent first), copying the pattern already there but pointing to your new file.
5. Optional: add/update the single featured link in the homepage's Writing section
   (`index.html`, `id="writing"`) if you want it to feature a different post.
6. Commit and push — no other setup needed.
