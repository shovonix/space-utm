# Space UTM

A UTM link builder for creators: one video, every place you post it. Live at https://utm.shovonix.dev

Built by [Shovon Arifin](https://shovonix.dev). Part of the Space tools, with [Space Prompter](https://prompter.shovonix.dev).

- **Placements**: YouTube description, pinned comment, Shorts, community post, channel links, on-screen QR, Instagram, TikTok, X, LinkedIn, Facebook, Threads, Discord, newsletter, podcast notes, plus your own.
- **Short, dated campaigns**: `utm_campaign` is a short code plus the date as DDMMYY, e.g. `fp220726`. The date defaults to today and can be changed, so old links can be rebuilt exactly.
- **Per-placement tag**: `utm_content` tells the description apart from the pinned comment. Turn it off for the plain `source / medium / campaign` format.
- **Clean names**: codes are lowercased so reports don't split. Existing `utm_` tags are replaced.
- **GA4-friendly**: the presets use mediums that land in GA4's default channel groups (Organic Video, Organic Social, Email, Audio).
- **QR codes**: black on white, or white on transparent to drop onto video. 1200 px PNG.
- **Export**: copy one link, copy all, or download CSV. Recent videos are saved in the browser.

No shortener and no redirects: links point straight at your site. Everything lives in `index.html`; there is no build step.

QR encoding by [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) (MIT, Kazuhiko Arase).

## Licence

Copyright © 2026 Shovon Arifin. All rights reserved.

The code is public so you can see how Space UTM works. It is not open source: you may not copy, modify, redistribute or host it, in whole or in part, without written permission. Use the live app at the link above.

The bundled QR code library (qrcode-generator by Kazuhiko Arase) keeps its own MIT licence.
