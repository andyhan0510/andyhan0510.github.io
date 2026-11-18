# Xuzheng (Andy) Han — Personal Academic Website

Live site: **https://andyhan0510.github.io**

A lightweight static website (plain HTML + CSS). No Jekyll, build step, or dependencies are required; GitHub Pages serves the files directly.

## Site structure

| Page | File | Content |
|---|---|---|
| About (home) | `index.html` | Bio, research interests, current research, news |
| Publications | `publications.html` | Peer-reviewed articles and manuscripts in preparation |
| Talks | `talks.html` | Conference presentations |
| Projects | `projects.html` | Project list, most recent first (title, dates, one-line summary, cover image) |
| Project details | `projects/*.html` | One page per project: background, key findings, significance, methods, related outputs |
| CV | `cv.html` | Education, experience, research, publications, presentations, skills, PDF download |

Assets:

- `assets/style.css` — shared stylesheet for all pages
- `assets/profile.jpg` — profile photo
- `assets/figures/` — figures used on the project pages (from the Ph.D. dissertation and M.S. thesis)
- `assets/Xuzheng_Han_CV.pdf` — public version of the CV
- `.nojekyll` — tells GitHub Pages to serve files as-is without Jekyll processing

## Local preview

Open `index.html` in any web browser. All links are relative, so navigation works offline.

## Editing the site (no software needed)

1. In this repository on GitHub, open the file you want to change and click the ✏️ (**Edit this file**) button.
   - **News / bio** → `index.html`: copy an existing `<li>…</li>` inside `<ul class="news">` and edit the date and text.
   - **New publication** → `publications.html`: copy an `<li>…</li>` inside `<ol class="pubs">` and edit authors, title, and journal. When a manuscript is published, move it from "Manuscripts in Preparation" to "Peer-Reviewed Journal Articles".
   - **New talk** → `talks.html`. **Education / skills** → `cv.html`.
   - **New project** → copy an `<article class="pf-item">…</article>` block in `projects.html`, then duplicate any page in `projects/` and update its content and file name.
2. The sidebar (photo, email, Google Scholar, ORCID) is repeated on every page, so update it in each HTML file.
3. Click **Commit changes…** → **Commit changes**. The live site updates within 1–2 minutes (use `Cmd + Shift + R` to force-refresh the browser).
4. To replace a file (e.g., a new CV PDF or photo), open the `assets` folder → **Add file → Upload files** and upload a file with the **same name** to overwrite it.

Every change is versioned; previous versions can be restored from the file's **History**.

## Optional improvements

- Replace the Google Scholar search links next to each paper with DOI links (`https://doi.org/...`) once available.
- Add LinkedIn / ResearchGate links by filling in the commented-out lines in the sidebar.
- Use a higher-resolution square photo (at least 400 × 400 px) saved as `assets/profile.jpg`.
