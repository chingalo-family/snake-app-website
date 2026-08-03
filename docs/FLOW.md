# User Flows

## Marketing site

```text
Landing (index.html)
  ├─ Hero → Contact CTA / See the game
  ├─ #play → Screenshot rail (Splash → Home → Levels → Play)
  ├─ #features → Offline / responsive / collect & climb
  ├─ #contact → Phone · WhatsApp · Instagram
  └─ Footer → Privacy Policy

Privacy (privacy.html)
  └─ Nav → Home · Contact · Privacy (current)
```

Visitors learn what Snake App is, see product screenshots in order, and reach Chingalo Family via contact links. Store download CTAs remain **coming soon** until Play / App Store listings are published — do not invent URLs.

---

## In-app journeys (Flutter companion)

Aligned with the companion app’s UX. Authoritative detail lives in that repo’s UX doc.

```text
Splash
  ├─ First launch → Onboarding (3–4 pages) → Home
  └─ Returning → Home

Home
  ├─ Play → Level select → Playground
  ├─ High scores
  ├─ Profile (create / edit)
  ├─ Settings (SFX · BGM · haptics · language · updates)
  └─ About

Playground
  ├─ Pause → Resume / Restart / Quit to levels
  └─ Game over
        ├─ No profile → prompt create profile to save
        └─ With profile → persist bests / unlocks offline
```

### Journey notes

| Step | Behavior |
|------|----------|
| Splash | Brand mark; load prefs / audio / profile; route onboarding or home |
| Onboarding | Welcome · move (swipe or arrows) · collect · profile-to-save; skippable |
| Home | Brand + Play CTA; secondary nav — not a dense dashboard |
| Levels | Thirty levels; locked/unlocked; start level |
| Play | Responsive board; swipe or arrows; HUD score / level / best |
| Profile | Required only to **save** progress; play always allowed |
| Settings | Independent SFX and BGM; EN / SW locale |

---

## Screenshot order (site)

Match marketing rails to this sequence:

1. Splash  
2. Home  
3. Levels  
4. Play  

See [Design](DESIGN.md).

---

## Related

- [About](ABOUT.md)
- [Architecture](ARCHITECTURE.md)
- [Design](DESIGN.md)
- [Docs index](README.md)
