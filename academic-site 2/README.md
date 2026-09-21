# Your Academic Website

A simple, self-contained website (`index.html` + `style.css`) built to run on
**GitHub Pages** for free, no build tools or frameworks required. This
README covers two things: how to publish it, and how to edit it afterward.

---

## 1. Publish it on GitHub Pages

You have two options. Option A gives you a URL like `yourname.github.io`
(a personal site). Option B gives you a URL like
`yourusername.github.io/academic-site` (a project site) and is a good choice
if you already use `yourusername.github.io` for something else.

### Option A — personal site (recommended)

1. On GitHub, create a **new repository** named exactly:
   `YOUR-GITHUB-USERNAME.github.io`
   (replace with your actual username; it must match exactly, and it must be public).
2. Upload these files into the **root** of that repository. Easiest way,
   with no command line:
   - Open the new repo on github.com
   - Click "Add file" -> "Upload files"
   - Drag in `index.html`, `style.css`, `README.md`, and the `cv/` and
     `assets/` folders
   - Commit the changes
3. Go to the repo's **Settings -> Pages**.
4. Under "Build and deployment", set Source to **Deploy from a branch**,
   branch **main**, folder **/ (root)**. Save.
5. Wait 1-2 minutes, then visit `https://YOUR-GITHUB-USERNAME.github.io`.

### Option B — project site

1. Create a repository with any name, e.g. `academic-site`.
2. Upload the same files into its root (same steps as above).
3. Settings -> Pages -> Source: Deploy from a branch, branch **main**,
   folder **/ (root)**.
4. Your site will be at `https://YOUR-GITHUB-USERNAME.github.io/academic-site`.

### If you prefer the command line

```bash
git init
git add index.html style.css README.md cv assets
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

Then enable Pages as in step 3/4 above.

### Custom domain (optional)

If you own a domain (e.g. `alexrivera.com`), add a file named `CNAME`
(no extension) containing just the domain, e.g.:

```
alexrivera.com
```

and point your domain's DNS at GitHub Pages per GitHub's instructions
("Managing a custom domain for your GitHub Pages site").

---

## 2. Fill in your real content

Everything you need to change is in **`index.html`**. Search for these and
replace them:

- `Alex Rivera` — your name (also update the `<title>` tag at the top)
- The role/affiliation line under your name
- The tagline sentence describing your research
- The **About** paragraph and the research-interest tags
- The **Publications** section — duplicate a `<li class="pub-item">` block
  for each paper; delete the placeholder ones. Each entry has:
  - `pub-title` — paper title
  - `pub-authors` — wrap your own name in `<strong>` so it stands out
  - `pub-venue` — journal/conference and year
  - `pub-links` — swap the `href="#"` placeholders for real PDF/DOI/code links
- The **Teaching** list (delete this whole `<section id="teaching">` if
  it doesn't apply to you)
- Email address and social links in the footer (Google Scholar, ORCID,
  GitHub, LinkedIn, X) — delete any `<a>` you don't want
- Add your CV as `cv/CV.pdf` (see `cv/README.txt`)
- Optionally add a headshot (see `assets/img/README.txt`)

No build step is needed — just edit the HTML text directly (GitHub's web
editor, the pencil icon on any file, works fine for small edits) and commit.
Pages will redeploy automatically within a minute or two of any push.

## 3. Customize the look

All colors, fonts, and spacing are controlled from the top of `style.css`
in the `:root { ... }` block. The accent color defaults to Cornell
carnelian (`#B31B1B`); change `--accent` and `--accent-ink` to switch the
whole site's accent color in one place. Fonts are loaded from Google Fonts
in the `<head>` of `index.html` if you'd like to try different serif
pairings.
