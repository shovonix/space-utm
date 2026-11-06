# Space UTM

UTM link builder for creators: one video, every place it's posted. Live at https://utm.shovonix.dev (renamed from Space Links).

## How this repo works
- Everything is in `index.html`. No build step, no framework, no npm. Keep it that way unless Shovon asks.
- Recent videos are saved in the browser. No shortener, no redirects: links point straight at the site.
- Preview locally: `python3 -m http.server 8000`, then open http://localhost:8000
- `landing/space-utm/` is the landing page.
- The bundled QR library (qrcode-generator, MIT) is vendored. Don't edit it.

## Campaign format: don't change
- `utm_campaign` = short code + date as DDMMYY, e.g. `fp220726`. This is the MGD Studio team format. Old links must rebuild exactly.
- Codes are lowercased. Existing `utm_` tags are replaced.
- `utm_content` tells placements apart (description vs pinned comment) and can be switched off.
- Presets use mediums that land in GA4's default channel groups. Check GA4's channel rules before changing a medium.

## Space key (signature of every Space app)
- Uses the shared `SpaceKey` helper and the on-screen keycap (`#spacehint`). It never fires while typing in a field.
- Keep the Space key working and fun after every change.

## Design
- Black and white only. Tokens: `--bg #070707`, `--fg #F0F0EE`, `--hair #2A2A2C`. Red only for warnings.
- QR codes: black on white, or white on transparent.

## Rules
- After changing any cached file, bump `CACHE` in `sw.js` so installed copies update.
- No analytics or tracking scripts.
- Licence: all rights reserved (the QR library keeps its MIT licence). Don't add an open-source licence.
- Ask before adding a dependency, a build step, or a backend.

## Workflow
- Work on the Mac in `~/Sites/space/space-utm`. Preview locally, commit small, push to `main`.
- Deploy by pulling on the VPS (CloudPanel site for utm.shovonix.dev). The server path isn't written down yet: check CloudPanel, don't guess, then record it here.
- Never edit the live files on the VPS directly.
