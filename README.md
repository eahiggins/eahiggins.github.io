# Emma Higgins – personal website

Built with [Quarto](https://quarto.org) and hosted free on GitHub Pages.
The finished site is already built in the `docs/` folder, so it will go live
as soon as you upload it.

## 1. Put it online (one-off, about 30 minutes)

1. Create a free account at <https://github.com>. Pick your username
   carefully: it becomes your web address (`username.github.io`).
2. Click **New repository**. Name it exactly `username.github.io`
   (with your username). Set it to **Public** and click **Create**.
3. On the new repo page, click **uploading an existing file**, drag in
   **everything inside this folder** (including the `docs` folder), and
   click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment* choose
   **Deploy from a branch**, branch **main**, folder **/docs**, and **Save**.
5. After a minute or two the site is live at `https://username.github.io`.
6. Open `_quarto.yml` and replace `YOUR-GITHUB-USERNAME` with your username.

Tip: installing **GitHub Desktop** makes uploading changes a one-click job.

## 2. Edit it on your computer

1. Install Quarto from <https://quarto.org/docs/get-started/> (works inside RStudio).
2. Open this folder in RStudio as a project.
3. Edit any `.qmd` page, then in the Terminal run:

   ```
   quarto preview      # live preview while you edit
   quarto render       # rebuild the docs/ folder before uploading
   ```

4. Upload the changed files to GitHub (or click *Push* in GitHub Desktop).

## 3. Swap in your photos

Every image in `images/` is a placeholder. Replace each with your own photo
**using the same file name** and the site updates automatically:

| File | Where it appears |
| --- | --- |
| `hero.jpg` | Home-page banner (mangrove photo, landscape) |
| `portrait.jpg` | Profile photo (square) |
| `images/projects/*.jpg` | One photo per research project (names match `projects.yml`) |
| `selati.jpg`, `kanahau.jpg`, `stackpole.jpg`, `belize.jpg` | Field sites |
| `teaching.jpg` | Teaching page |

Before uploading photos:

- **Remove GPS location data.** On Windows: right-click the photo →
  Properties → Details → *Remove Properties and Personal Information*.
  This matters for rhino, pangolin and other poached species.
- **Resize** to about 2000 px wide (1200 px for cards) so pages load fast.
- To add a caption to the banner, put `<span class="tag hero-credit">Your caption</span>` inside the hero section in `index.qmd`.

## 4. Common edits

- **Add a project:** in `projects.yml`, copy a block and edit it. Put its photo in `images/projects/`. `featured: true` also shows it on the home page; `categories` become the filter buttons on the Research page.
- **Contact links:** edit the profile icons and the Get in touch list in `index.qmd`, and the menu icons in `_quarto.yml`.
- **Add a paper:** in `publications.qmd`, copy one `<div class="pub">` block and edit it.
- **Add code:** list repositories on `code.qmd`. Any `.qmd` page can contain
  R code chunks; Quarto runs them and shows plots and maps in the page.
- **Colours and fonts:** `styles/theme.scss` (light) and `styles/dark.scss` (dark).
- **Menu:** the `navbar` section of `_quarto.yml`.

## 5. Your own domain (optional)

Buy a domain (e.g. from Cloudflare or Namecheap), then in **Settings → Pages →
Custom domain** enter it and follow GitHub's DNS instructions.
