# Website Architecture

Static marketing site — no build step, no backend. GitHub Pages deploys from `main`.

---

## Site layout

```text
.
├── index.html              # Landing
├── privacy.html            # Privacy policy
├── css/styles.css          # Brand + layout
├── js/main.js              # Reveal / small UI behavior
├── assets/
│   ├── app-icon.png
│   └── screenshots/        # splash → home → levels → play
├── docs/                   # This documentation
└── .github/workflows/
    └── deploy-pages.yml    # GitHub Pages on push to main
```

| Piece | Role |
|-------|------|
| `index.html` | Hero, screenshot rail, features, contact |
| `privacy.html` | Legal copy; links back to contact |
| `css/styles.css` | Tokens, layout, components |
| `js/main.js` | Progressive enhancement (e.g. scroll reveals) |
| `assets/` | Icon + ordered product screenshots |

Relative paths only — works when opened via a static server or GitHub Pages.

---

## Deploy

- Workflow: [`.github/workflows/deploy-pages.yml`](../.github/workflows/deploy-pages.yml)
- Trigger: pushes to `main`
- Artifact: repository root as a static site

Local preview: any static server from the repo root (see [README](../README.md)).

---

## Relationship to the Flutter app

This repo is the **marketing sibling** of the companion Flutter project **`snake_app`** (display name Snake App, package `chingalo.family.snake_app`). The app is a separate git repository — do not assume in-repo paths to Flutter sources.

When both are checked out next to each other under `chingalo-family/`:

| Concern | Where |
|---------|--------|
| App architecture, UX, theme, plan, modes | Companion repo `snake_app` → its `docs/` |
| Site copy, brand on the web, privacy page | This repo → `docs/` + HTML |

### App layers (summary)

The Flutter app targets:

```text
lib/
├── app/        # MaterialApp, router, bootstrap, providers
├── core/       # theme, constants, models, services (Drift AppDatabase,
│               # PreferenceService, audio, settings), game engine, l10n helpers
├── features/   # splash, onboarding, home, levels, game, profile,
│               # scores, settings, about, …
└── shared/     # Cross-feature widgets
```

- **Offline-first:** Drift SQLite (`AppDatabase`) for profile / scores / progress; SharedPreferences via `PreferenceService` for settings flags.
- **Profile gate:** Play without a profile is allowed; persisting bests and unlocks requires a local profile.
- **Playground:** `GridMetrics` from layout constraints (aspect-aware; phone/tablet rotation).
- **Controls:** Swipe on touch; arrow keys on desktop.
- **i18n:** Flutter gen-l10n — English + Kiswahili (`lib/l10n/`).

For the authoritative technical notes, use the companion Flutter repo’s architecture doc (conceptually: `snake_app/docs/ARCHITECTURE.md`). Keep marketed claims here aligned with that product (levels count, offline/profile, platforms) — see [About](ABOUT.md).

---

## Related

- [About](ABOUT.md)
- [Flow](FLOW.md)
- [Design](DESIGN.md)
- [Docs index](README.md)
