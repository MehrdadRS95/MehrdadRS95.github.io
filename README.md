# Mehrdad Rostamzadeh — Personal Website

A fast, static multi-page portfolio for an **AI Security researcher & Data Scientist**.
No build step, no framework — just HTML, CSS, and a little vanilla JavaScript. Deploys directly to GitHub Pages.

## Pages

| File | Page |
|------|------|
| `index.html` | Home / About — hero, summary, core competencies, featured work, education |
| `experience.html` | Full professional timeline + skills matrix + education |
| `research.html` | Research focus areas + publications (with live links) |
| `projects.html` | Selected projects (research + engineering) |
| `contact.html` | Contact links + CV download |

## Design

- **Theme:** academic + tech hybrid — serif display headings (Newsreader), Inter body, JetBrains Mono accents.
- **Dark mode:** toggle in the navbar; remembers your choice and respects the system setting.
- **Responsive:** works from phone to desktop, with a mobile menu.
- **Motion:** subtle scroll-reveal and count-up stats (disabled for `prefers-reduced-motion`).

## Deploy to GitHub Pages

1. Create a repo named **`MehrdadRS95.github.io`** (your username, exactly).
2. Push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Launch portfolio"
   git branch -M main
   git remote add origin https://github.com/MehrdadRS95/MehrdadRS95.github.io.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source → Deploy from branch → `main` / root**.
4. Your site goes live at **https://mehrdadrs95.github.io** within a minute or two.

(The included `.nojekyll` file tells GitHub Pages to serve the files as-is.)

## Before you publish — quick checklist

- [ ] **Profile photo:** drop `assets/profile.jpg` in, then in `index.html` uncomment the `<img>` inside `.portrait-photo` and delete the placeholder `<div class="portrait-ph">`.
- [ ] **Google Scholar link:** replace `https://scholar.google.com/` (in `research.html` and `contact.html`) with your profile URL.
- [ ] **ORCID link:** replace `https://orcid.org/` with your ORCID URL.
- [ ] **Project repos:** in `projects.html`, replace the "Add repo / Add case study" placeholder links (`#` or the GitHub profile URL) with real repository/demo URLs.
- [ ] **MCP-DPT arXiv:** confirm `https://arxiv.org/abs/2604.07551` resolves once the paper is public.
- [ ] **CV:** the download uses `assets/Mehrdad_Rostamzadeh_CV.pdf`. Re-copy `CVP.pdf` there whenever you update it.

## Paper PDFs (bundled locally)

Your two paper PDFs are served straight from the site, so reviewers can read them even
if a preprint link isn't live yet:

- `assets/MCP-DPT.pdf` → linked from the MCP-DPT entry on `research.html`
- `assets/Time-Series-Meta-Learning.pdf` → linked from the meta-learning entry

> The originals you dropped in the repo root (`mcp-+dpt.pdf`, `time series forecasting.pdf`)
> are now duplicated under `assets/` with clean names — you can safely delete the root copies.

## Verified working links

- MCP-DPT — arXiv:2604.07551 (+ local PDF)
- Meta-Learning forecasting — https://arxiv.org/abs/1908.08489 (+ local PDF)
- BWE demand forecasting — https://www.sciencedirect.com/science/article/pii/S2405896320336363
- GitHub — https://github.com/MehrdadRS95
- LinkedIn — https://linkedin.com/in/mehrdad-rostamzadeh-513b11ab/

## Editing tips

- Colors, fonts, and spacing live in CSS variables at the top of `assets/styles.css` (`:root` for light, `[data-theme="dark"]` for dark).
- The nav and footer are duplicated in each HTML file (no build step) — if you change a nav link, update it in all five pages.
