# Commonground Roastery Cafe

A pixel-art barista mini-game for the café. Scan the QR on the table, play in
the browser — no install, no app store.

**Play:** https://viter999.github.io/commonground-cafe/

## How it plays

A customer walks in and orders. Tap the ingredients **in the right order**
before their patience runs out.

- **7 drinks** — Americano and Latte (3 steps) up to Black Orange and Black
  Coconut (10 points)
- **Normal Mode** — a 120-second shift with 4 hearts. Morning pace, then Rush
  Hour at 70s where three customers wait at once, then closing.
- **Unlimited** — endless, 3 hearts, and random events: Happy Hour (double
  points), Machine Jam (slow brew), VIP guests worth double.
- Serve fast for a speed bonus, chain orders for a streak multiplier up to 3×.

High scores are saved on the phone that played, under the name you enter.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The QR target. Never changes — redirects to the game with a cache-busting query string, so a scan always gets the newest version. |
| `game.html` | The game: layout, recipes, scoring, and all state. |
| `support.js` | Template runtime. Loads React from a CDN on first visit. |
| `image-slot.js` | Image placeholder component used for the title mascot. |
| `assets/` | Sprites and the background music track. |

## Updating the game

Edit `game.html` and re-upload just that one file. The printed QR keeps
working — it points at `index.html`, which never changes.

## Note on the first load

`support.js` fetches React from unpkg.com, so the very first visit on a device
needs a working internet connection. The browser caches it afterwards.
