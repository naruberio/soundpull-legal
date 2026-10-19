# soundpull-legal

Legal & support pages for the **SoundPull** iOS app (`com.naruberio.soundpull`),
served via GitHub Pages at <https://naruberio.github.io/soundpull-legal/>.

SoundPull extracts the audio track from your own videos as M4A (AAC), fully on-device.

## Pages

English is the canonical/primary language (the App links to the unsuffixed URLs below).
Each page has a language bar linking to all 11 supported languages.

| Page | English (canonical) URL |
|------|-------------------------|
| Privacy Policy | `/privacy-policy` (`privacy-policy.html`) |
| Terms of Use | `/terms` (`terms.html`) |
| Support | `/support` (`support.html`) |
| Index / language hub | `/` (`index.html`) |

Localized variants follow the pattern `<page>-<lang>.html`, e.g. `privacy-policy-ja.html`.

### How-to guides (KAN-944, soundpull-app D-57)

Job-specific pages in en / ja / de only (not the 11 languages above). They share `guide.css`.

| Page | English URL |
|------|-------------|
| Extract audio from a video | `guide-extract-audio.html` |
| Convert a voice memo to MP3 | `guide-voice-memo-mp3.html` |
| Merge audio files | `guide-merge-audio.html` |

Button names in the steps must match the App's UI strings word for word (`soundpull-app/src/i18n/index.ts`).
When the App's labels change, update these pages in the same change.

Do not add text that points readers to free alternatives (Shortcuts, GarageBand, "you may not need MP3"),
whether in sections, FAQ answers, meta descriptions or the index blurb (KAN-948, soundpull-app D-58).
The voice-memo section explaining there is no real way without an app stays.
Limits of SoundPull itself (DRM, iOS version, no crossfade, MP3 re-compression) stay on the pages.

### Discovery files

- `sitemap.xml` lists every page. Update it when pages are added or removed
  (the guides also carry their en / ja / de alternates there).
  Search engines read it only after it is registered in Bing Webmaster Tools or Google Search Console:
  there is no robots.txt at the host root (`naruberio.github.io`) to point to it, and IndexNow does not read sitemaps.
- `<32 hex>.txt` is the IndexNow key (public by design). After publishing changed pages,
  notify IndexNow with `keyLocation` pointing at this file.

## Languages (11, D-06)

en (primary) · ja · zh-Hant · es · pt-BR · de · fr · ko · id · vi · th

## Notes

- Static HTML only — no build step. `.nojekyll` disables Jekyll so files are served as-is.
- The App (`soundpull-app`) references these URLs in `src/shared/legal.ts`.
- Publisher: naruberio · Contact: konpei.work@gmail.com
