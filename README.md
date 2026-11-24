# Website: Track Mixer & Mic Enhancer

Plain static HTML/CSS with no build step. The styling follows
`IEM Mixer/Design/DESIGN.md` (the project folder keeps its old name).

```
index.html              Home: both apps
track-mixer/index.html  Track Mixer feature page
track-mixer/guide.html  Track Mixer user guide
mic-enhancer/index.html    Mic Enhancer feature page
mic-enhancer/guide.html    Mic Enhancer user guide
assets/style.css        All styles
assets/img/             Screenshots go here
```

## Preview locally

```sh
cd "~/Documents/App Design/Website"
python3 -m http.server 8000
# open http://localhost:8000
```

## Publish on GitHub Pages

1. Create an empty repo on GitHub, e.g. `small-audio-site`.
2. `git remote add origin git@github.com:dandrums/small-audio-site.git`
   then commit and `git push -u origin main`.
3. On GitHub: **Settings → Pages → Build and deployment → Deploy from a
   branch → `main` / root**. The site goes live at
   `https://dandrums.github.io/small-audio-site/`.
4. Optional custom domain: add it under Settings → Pages, which creates a
   `CNAME` file, and point your DNS at GitHub as it describes.

All links are relative, so the site works at a sub-path or on a custom domain.

## To do before launch

- **Screenshots:** done (`assets/img/track-mixer-*.jpg`, `mic-enhancer-*.jpg`). To
  replace one, crop off the status bar, resize to 720 px wide for portrait
  or 1400 px for landscape, save as JPEG and keep the same file name.
- **App Store links:** replace the `href="#"` on each
  "Coming soon to the App Store" button.
- **Name:** the header says "Small Audio". Change it in every page's
  `.brand` link if you trade under another name.
- **Guides:** update them when app features change. They describe the apps as
  of November 2026.
