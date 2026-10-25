# 5-1 Rotation Tracker

**Live site:** https://williamm066.github.io/Volleyball-rotations/

Follow any player through the six rotations of a 5-1 volleyball system. For each rotation it shows your rotation zone, where you stand when the serve happens, and where you move once the ball is live, with arrows for the movement.

## On your phone

Open the live site, then add it to your home screen (iPhone: Share → Add to Home Screen; Android: ⋮ → Add to Home screen). It opens like an app and works offline after the first visit.

## Using it

- Pick a player and a rotation (1–6), then **We receive** or **We serve**.
- The court plays the three steps; tap a step or use **Step ›** to go through it yourself.
- Swipe left/right on the court to change rotation.
- **Everyone's moves** shows the whole team's switches.
- Laptop: ← → rotation, ↑ ↓ step, Space plays.

## Editing positions

Positions are near the top of the script in `index.html`: `PLAYERS` (lineup order), `RECEIVE` (serve-receive spots, in metres: x 0–9 left to right, y 0–9 net to end line), `PASSERS` and `BASE`. After a change, bump `VERSION` in `sw.js` so phones load the new version.
