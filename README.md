# Tushar Lab Website

Academic research lab website built with [Astro 5](https://astro.build), deployed to GitHub Pages.

**Live site:** https://tusharlabratory.github.io/

---

## Quick Start

```bash
npm install
npm run dev       # http://localhost:4321/tushar-lab/
npm run build     # outputs to dist/
```

---

## Project Structure

```
tushar-lab/
├── src/
│   ├── content/          ← ALL editable content (JSON)
│   │   ├── site.json     ← Lab name, PI info, contact
│   │   ├── research.json ← Research areas
│   │   ├── team.json     ← Team members
│   │   ├── publications.json
│   │   ├── news.json
│   │   ├── resources.json
│   │   └── opportunities.json
│   ├── pages/            ← One .astro file per page
│   ├── layouts/          ← BaseLayout (header + footer)
│   ├── components/       ← Header.astro, Footer.astro
│   └── styles/           ← global.css (UA brand colors)
├── public/               ← favicon.svg, static assets
├── .github/workflows/    ← GitHub Actions auto-deploy
└── astro.config.mjs      ← site + base URL config
```

---

## Updating Content

All content lives in `src/content/*.json` — no code changes needed.

| File | What it controls |
|------|-----------------|
| `site.json` | Lab name, PI name, email, address, social links |
| `team.json` | Add/edit team members, upload photos to `public/` |
| `publications.json` | Add papers, fill in DOI + PDF links |
| `research.json` | Research area descriptions and project lists |
| `news.json` | Lab announcements and updates |
| `resources.json` | Software, datasets, model weights |
| `opportunities.json` | Open positions and application instructions |

---

## Updating Colors

Edit CSS variables in `src/styles/global.css`:

```css
:root {
  --cardinal:  #AB0520;   /* UA Cardinal red */
  --navy:      #0C234B;   /* UA Navy */
  ...
}
```

---

## Adding Team Photos

1. Add photo to `public/photos/yourname.jpg`
2. In `src/content/team.json`, set `"photo": "/tushar-lab/photos/yourname.jpg"`

---

## Deployment to GitHub Pages

### First-time setup

1. Create repo `tusharlabratory.github.io` on GitHub at https://github.com/tusharlabratory
2. Push this code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/tusharlabratory/tusharlabratory.github.io.git
   git push -u origin main
   ```
3. In GitHub repo → **Settings → Pages → Source → GitHub Actions**
4. The workflow runs automatically on every push to `main`

### After that

Every `git push` to `main` auto-deploys to https://fitushar.github.io/tushar-lab/

---

## Pages

| Page | URL |
|------|-----|
| Home | `https://tusharlabratory.github.io/` |
| Research | `https://tusharlabratory.github.io/research/` |
| Publications | `https://tusharlabratory.github.io/publications/` |
| Team | `https://tusharlabratory.github.io/team/` |
| Resources | `https://tusharlabratory.github.io/resources/` |
| News | `https://tusharlabratory.github.io/news/` |
| Opportunities | `https://tusharlabratory.github.io/opportunities/` |
| Contact | `https://tusharlabratory.github.io/contact/` |
