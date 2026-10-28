# Sports Stats Tracker

Offline-first mobile web app for recording live game stats (basketball, netball, soccer, volleyball, and custom sports).

## Features

- **Works fully offline** — no Wi-Fi needed after first load. Data saved on the device (localStorage).
- **Installable** as a Progressive Web App (PWA) on Android and iOS home screens.
- **Built-in sports**: Basketball, Netball, Soccer/Football, Volleyball.
- **Custom sports** — define your own scoring and stat types.
- **Live scoring** with period/quarter clock, play-by-play log, and undo.
- **Player stats** — points, rebounds, assists, etc. (configurable per sport).
- **Box scores** and full game history.
- **Export / Import** JSON backup of all games.

## How to use on your phone

### Option A — Local files (simplest)

1. Copy the entire `sports-stats-app` folder to your phone (or open the files from a computer).
2. Open `index.html` in Chrome (Android) or Safari (iOS).
3. For the best experience:
   - **Android (Chrome)**: Menu → "Add to Home screen" / "Install app".
   - **iOS (Safari)**: Share button → "Add to Home Screen".

### Option B — Host it (recommended for PWA + offline)

Serve the folder over HTTPS (or localhost) so the service worker and "Add to Home Screen" work reliably:

```bash
# From the sports-stats-app folder
npx serve -p 3000
# or
python3 -m http.server 8080
```

Then open the URL on your phone (same network) and Add to Home Screen.

### Option C — One-time transfer

Zip the folder, send it to yourself, extract, and open `index.html`.

## Using the app

1. **Home** — tap a sport to start a new game, or open a recent/in-progress game.
2. **Setup** — name teams, set period length & number of periods, add players (# and name).
3. **Live** — select Home/Away tab → select player → tap stat buttons. Clock can be started/paused. Undo appears after each action.
4. **Box Score** — full team & player totals + play-by-play.
5. **End Game** — marks the game finished and saves it.
6. **History** — view or resume past games, delete if needed.
7. **Settings** — export/import JSON, clear all data.

## Data & privacy

All data stays on the device. Nothing is sent to any server. Export a JSON backup if you want a copy elsewhere.

## Custom sport example

- Name: "Handball"
- Scoring: Goal (+1)
- Other stats: Assist, Steal, Block, Foul, Turnover

## Notes

- The period clock is a simple countdown (manual start/pause). It does not auto-advance periods.
- Missed shots (basketball) are tracked for completeness but do not affect score.
- You can resume unfinished games from Home or History.
