# ES-cadence

A day with a shape: the hard work in the morning, the daily targets tracked as you go, and a clear signal when the day is finished so the evening is yours.

Plain files, no build step. Everything you log stays on your device.

## Files

| File | What it does |
|---|---|
| `index.html` | The whole app |
| `manifest.json` | Makes it installable as a home-screen app |
| `sw.js` | Keeps it working offline |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | App icons |

## Publish on GitHub Pages

1. Create a public repo named `ES-cadence` and upload these files (the files, not the folder).
2. Settings → Pages → Source: **Deploy from a branch**, branch **main**, folder **/ (root)**, Save.
3. After a minute the app is live at `https://esthyu.github.io/ES-cadence/`.

## Install on iPhone

1. Open the link in Safari.
2. Share → Add to Home Screen.
3. Open it from the home screen from then on. It keeps its own data, separate from Safari.

## The five tabs

- **Today** — the current block, the dissertation timer, every block of the day with its counter, and the call pace.
- **Rhythm** — a week grid of what you hit, streaks, and a chart per tracker.
- **Trackers** — add, edit or archive anything you want to track. Three kinds: a number to hit, minutes of work, or a yes/no tick.
- **Schedule** — edit your time blocks and download the calendar file.
- **Settings** — name, theme, calls-per-booking rate, backup and reset.

## Alerts

A home-screen web app can't send reliable iPhone notifications. Instead, **Schedule → Download calendar file** gives you an `.ics` file. Open it on your phone and every block becomes a repeating calendar event with an alert 5 minutes before. Re-download after you change your blocks, and delete the old events first so you don't have both.

## How the numbers work

- **Done today** counts only the trackers set for today's weekday.
- **Streak** counts back day by day and skips days a tracker isn't set for. A day still open doesn't break it.
- **Call pace** = bookings still needed × calls per booking ÷ working days left in the month. Your set daily target sits next to it. The app also shows your actual calls-per-booking rate once you've logged bookings this month.
- **The timer** keeps running if you close the app. It logs the minutes when you stop it.

## Updating later

Upload the new `index.html`, then bump `VERSION` in `sw.js` so phones pick it up. Your logged days aren't touched.
