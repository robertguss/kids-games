# Guss Games

Browser games for Robert's kids (ages 8, 5, 3 and 1) to play on iPads. Hosted on Cloudflare Workers at https://kids-games.howtocode.workers.dev, deployed with the `cf` CLI (`cf deploy`).

## Rules for every game
- One folder per game: `public/games/<slug>/index.html`, plain HTML/CSS/JS, no build step, no npm, no backend. Assets live in the folder.
- Add an entry `{ "slug", "title", "emoji", "ages" }` to `public/games.json` so it shows on the home screen.
- Touch first: big tap targets (at least 64px), no hover, no keyboard needed, works in landscape and portrait on iPad Safari. Prevent scroll, zoom and text selection during play.
- Works offline once loaded. No ads, no links out, no accounts, no data collection, no chat, no external scripts or trackers.
- Little ones can't read: use pictures, sound and voice cues. Sound starts only after a tap (iOS rule).
- A big home button returns to `../../`.
- Keep a game under 1 MB unless images truly need more.
