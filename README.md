# Website: IEM Mixer & Presenter

Plain static HTML/CSS with no build step. The styling follows
`IEM Mixer/Design/DESIGN.md`.

```
index.html              Home: both apps
iem-mixer/index.html    IEM Mixer feature page
iem-mixer/guide.html    IEM Mixer user guide
presenter/index.html    Presenter feature page
presenter/guide.html    Presenter user guide
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

1. Create an empty repo on GitHub, e.g. `iem-mixer-site`.
2. `git remote add origin git@github.com:dandrums/iem-mixer-site.git`
   then commit and `git push -u origin main`.
3. On GitHub: **Settings → Pages → Build and deployment → Deploy from a
   branch → `main` / root**. The site goes live at
   `https://dandrums.github.io/iem-mixer-site/`.
4. Optional custom domain: add it under Settings → Pages, which creates a
   `CNAME` file, and point your DNS at GitHub as it describes.

All links are relative, so the site works at a sub-path or on a custom domain.

## To do before launch

- **Screenshots:** save PNGs into `assets/img/` and replace each
  `<div class="placeholder">` in the two feature pages with
  `<img src="../assets/img/NAME.png" alt="…">`.
- **App Store links:** replace the `href="#"` on each
  "Coming soon to the App Store" button.
- **Name:** the header says "Small Audio". Change it in every page's
  `.brand` link if you trade under another name.
- **Guides:** update them when app features change. They describe the apps as
  of November 2026.
