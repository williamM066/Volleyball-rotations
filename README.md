# 5-1 Rotation Tracker

A small website for following any player through the six rotations of a 5-1 volleyball system, with arrows showing where you move from the serve to your playing spot. No build step, no dependencies. It also works offline once it's been opened on your phone.

## Put it on GitHub Pages

1. On github.com, click **New repository**. Name it something like `volley-rotations`, set it to **Public**, and click **Create repository**.
2. On the new repo page, click **uploading an existing file**. Drag in all the files from this folder: `index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, `icon-192.png`, `icon-512.png` and `README.md`. Then click **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source** to *Deploy from a branch*, choose branch **main** and folder **/ (root)**, then click **Save**.
4. Wait a minute and refresh. The page shows your address: `https://<your-username>.github.io/volley-rotations/`

## Add it to your phone

- **iPhone (Safari):** open the address, tap **Share → Add to Home Screen**.
- **Android (Chrome):** open the address, tap **⋮ → Add to Home screen** (or *Install app*).

It opens full-screen like an app. After the first visit it works without signal, which helps in a sports hall.

## Using it

- Pick a player at the top (it remembers your choice), then a rotation 1–6.
- Choose **We receive** or **We serve**. The court plays out three steps: your rotation zone, where you stand when the serve happens, and where you run to once the ball is live. Tap a step or use **Step ›** to go through it yourself.
- Swipe left or right on the court to change rotation.
- Turn on **Everyone's moves** to see the whole team's switches at once.
- On a laptop: ← → change rotation, ↑ ↓ step, Space plays.

## Changing it later

All positions live near the top of the `<script>` in `index.html`:

- `PLAYERS` sets the lineup order (who starts in which zone).
- `RECEIVE` holds the serve-receive spots per rotation. Coordinates are metres: x from 0 (left sideline) to 9 (right), y from 0 (net) to 9 (end line).
- `PASSERS` lists who passes in each rotation.
- `BASE` is where each zone plays once the ball is live.

After editing, also change `VERSION` in `sw.js` (e.g. `rotations-v2`). Otherwise phones keep showing the cached old version.
