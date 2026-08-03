# Snake App Website

Marketing site for **Snake App** by [Chingalo Family](https://www.instagram.com/chingalo_family/) — an offline-first snake game with levels, collectibles, and local high scores.

Static HTML/CSS/JS. No build step required.

## Live site

Deployed with GitHub Pages on pushes to `main` (see [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml)).

## Local development

```bash
git clone https://github.com/chingalo-family/snake-app-website.git
cd snake-app-website
```

Serve the folder with any static server:

```bash
# Python
python3 -m http.server 8000

# Node
npx --yes serve -l 8000
```

Then open [http://localhost:8000](http://localhost:8000).

You can also open `index.html` directly in a browser.

## Pages

| File | Purpose |
|------|---------|
| `index.html` | Landing — hero, screenshots, features, contact |
| `privacy.html` | Privacy policy |

## Documentation

See **[docs/README.md](docs/README.md)** for about, architecture, flow, and design notes. Keep those files updated when site copy, brand, or marketed product facts change.

## Project structure

```text
.
├── index.html
├── privacy.html
├── css/styles.css
├── js/main.js
├── assets/
│   ├── app-icon.png
│   └── screenshots/
│       ├── splash.png
│       ├── home.png
│       ├── levels.png
│       └── play.png
├── docs/
│   ├── README.md
│   ├── ABOUT.md
│   ├── ARCHITECTURE.md
│   ├── FLOW.md
│   └── DESIGN.md
├── .cursor/
│   ├── rules/
│   └── skills/
└── .github/workflows/deploy-pages.yml
```

## Brand

| Token | Value |
|-------|-------|
| Background | `#0B1F1A` |
| Primary | `#1FA87A` |
| Accent | `#3ECF98` |
| Display font | Outfit |
| Body font | Figtree |

Colors follow the app’s nature-arcade palette. Screenshots are shown in order: Splash → Home → Levels → Play.

## Contact

- Phone: [+255 687 168 627](tel:+255687168627)
- WhatsApp: [+255 742 349 206](https://wa.me/255742349206)
- Instagram: [@chingalo_family](https://www.instagram.com/chingalo_family/)

## License

Proprietary — Chingalo Family. All rights reserved.
