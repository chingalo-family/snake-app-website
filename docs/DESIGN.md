# Design — Brand & Visual Language

Marketing site design tokens and how they align with the Flutter app’s nature-arcade theme.

---

## Brand tokens (site)

| Token | Value | Role |
|-------|-------|------|
| Background | `#0B1F1A` | Page / deep forest surface |
| Primary | `#1FA87A` | CTAs, links, brand accent |
| Accent | `#3ECF98` | Soft highlights, success-adjacent accents |
| Display font | **Outfit** | Brand, headlines |
| Body font | **Figtree** | Body, UI chrome |

Avoid purple-indigo gradients and generic “AI default” looks. Prefer tonal greens on dark surfaces, with amber used sparingly for reward/energy (app secondary `#F0A202` when mirroring game UI in shots).

---

## Alignment with the Flutter app

The app documents a fuller palette (surfaces, text, danger, snake/food rings) in its theme doc. Shared anchors:

| Role | Hex |
|------|-----|
| Surface bg | `#0B1F1A` |
| Primary | `#1FA87A` |
| Primary light | `#3ECF98` |
| Secondary / reward | `#F0A202` |
| Danger | `#E85D4C` |

App UI type leans rounded/playful (e.g. Nunito); the **website** uses Outfit + Figtree for marketing polish. Screenshots should still read as the same product family.

**Do not** introduce purple-indigo Material demos on either surface.

---

## Typography & layout (site)

- Hero: brand name as a strong signal; one headline; one short lede; CTA group; one dominant device visual
- Sections: one job each — game screenshots, features, contact
- Prefer atmosphere (soft grid / glows) over flat single-color slabs; keep motion subtle (reveal on scroll)

---

## Screenshots

Assets under `assets/screenshots/`. **Order on the site:**

1. `splash.png` — Splash  
2. `home.png` — Home  
3. `levels.png` — Levels  
4. `play.png` — Play  

When replacing shots, keep this sequence and update captions/alt text. Prefer real product UI (dark nature-arcade), not mockups that drift from shipping theme.

Icon: `assets/app-icon.png` (favicon + header lockup).

---

## Contact presentation

Contact section and privacy page use the same numbers and Instagram handle as [About](ABOUT.md). Changing contact details requires updating HTML **and** docs in the same change set.

---

## Related

- [About](ABOUT.md)
- [Flow](FLOW.md)
- [Architecture](ARCHITECTURE.md)
- [Docs index](README.md)
