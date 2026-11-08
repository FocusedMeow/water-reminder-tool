# Drink Water — Offline Web App

A single-file water reminder. No install, no account, no internet connection.

## Open it

Double-click **`Drink Water.html`** and open it with Edge, Chrome, or Firefox.

Pin the tab (right-click the tab → **Pin tab**) so it is harder to close by accident.

The HTML file is also the complete source code — open it in Notepad or VS Code if you want to read or change it. There is no build step and no dependency.

## What it does

- Reminds you every 45 minutes by default (10 minutes – 2 hours)
- Daily goal of 8 cups / 2000 ml; cup count and cup size are adjustable
- Animated glass that fills as you drink, plus ml, day streak, and next reminder
- Last 7 days of history, archived automatically at midnight
- Reminder card, soft chime, flashing tab title, and optional browser notifications
- “Snooze 10 min”, “Pause 1 hour”, and “Preview reminder”
- Everything stays on your machine — no uploads, no tracking

## Important limits

1. **Keep the tab open.** Closing the browser stops all reminders. This is the main difference between a web page and a desktop app.
2. **Background tabs can be throttled.** A reminder may arrive a little late; the page catches up as soon as the tab is active again.
3. **Browser notifications are optional.** Click “Enable notifications” and allow them. Some browsers restrict notifications for local `file://` pages; the in-page reminder, chime, and flashing title still work.
4. **Sound needs one click first.** Browsers block autoplay until you interact with the page.
5. **Data lives in this browser.** Clearing site data, using private mode, or switching browsers will lose the log.

## Settings

Open the gear icon in the top-right corner.

| Setting | Range / note |
| --- | --- |
| Interval | 10 minutes – 2 hours |
| Daily goal | 1 – 30 cups |
| Cup size | 50 – 1000 ml |
| Active hours | 08:00 – 23:00 by default; same start and end means all day |
| Sound | Soft two-note chime |
| Notifications | Optional browser permission |

At the bottom of the settings sheet you can restore defaults or clear today's log.

## Data

- Stored in `localStorage` under the key **`drinkwater.en.v1`**.
- The Chinese version uses a separate key (`drinkwater.v1`), so the two versions keep independent logs.
- No data is sent anywhere.

## Uninstall

Delete `Drink Water.html`. To remove the saved log as well, clear the site data for the file in your browser settings.

## Legacy desktop version (optional)

`旧版-桌面程序\DrinkWater.exe` is the older Windows tray app:

- Keeps reminding even when the browser is closed
- Supports launch at login, tray menu, and system notifications
- Double-click to run; right-click the tray icon for options

It is optional and completely independent from the web version. The web version is the main, cross-platform build.
