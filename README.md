# Clock

An offline Android alarm clock with a billable-hours work timer. Alarms designed to never miss, and weekly hours ready to paste into an invoice.

Part of Trip Point Software · by Trip Point Hardware

Android 8.0 or newer · Free · No internet access

## Why

Samsung Clock can't ring every other day, and no timer app I tried could calculate the weekly hours I bill. This one does both. Apparently, that was too much to ask of a six-figure Korean Samsung developer.

## Features

### Alarms
- Repeat once, on selected weekdays, or every N days (every other day, every 3 days, etc.), with **Skip next**.
- Rings over the lock screen at alarm volume, even in silent mode. The volume starts low and gradually increases over 20 seconds (or 60 seconds with gentle wake).
- A big **Snooze** button; **Dismiss** requires a one-second hold to prevent accidental dismissal.
- If nobody responds, the alarm automatically snoozes as a backup ring, then displays a "You missed your 6:30 alarm" notification.
- Per-alarm **Ring in Do Not Disturb** option.
- Still rings after a phone restart, even before you unlock it (Samsung phones restart overnight by default).
- Alarm history covering the last 90 days: dismissed, unanswered, or missed.

### Work timer (billable hours)
- Start, pause, and resume sessions. Each session is saved the moment you tap Start, so it survives app closure or a phone restart.
- Add, edit, or delete entries for forgotten punches, with one keyword line per day (e.g., "API refactor, client call").
- Track today's hours, this week's hours, your weekly target, and how many hours remain, all with a progress bar.
- Generate weekly invoice text, with each day rounded to 0.25 h (or 0.1 h / 0.01 h), while ensuring the total always adds up:
  ```
  Nov 2 - 6.5h [api refactor, client call]
  Nov 3 - 8h [testing, bug fixes]

  Total: 14.5h
  ```
- A reminder if the timer has been running for too long.

### Also
- Countdown timer and stopwatch, displayed live in the status bar and Samsung's Now Bar.
- Home screen widget, Quick Settings tile for the work timer, and launcher shortcuts (long-press the app icon).
- Four accent colors, with light and dark modes.

## Install

1. Download `clock-<version>.apk` to your phone and tap it.
2. Allow **Install unknown apps** for your browser or file manager when prompted. If Play Protect warns you about an unknown developer, choose **Install anyway**.
3. Open Clock and allow notifications.
4. Go to Settings (the gear icon on the Alarms tab) → **Alarm reliability**. Fix anything that isn't green, especially **Battery → Unrestricted**.

 On Samsung devices, also add Clock to **Never sleeping apps** (Settings → Battery → Background usage limits).
5. Go to Settings → **Test alarm (rings in 10 s)**, then lock your phone. The screen should turn on and the alarm should ring.
6. Go to Settings → **Automatic backup** and choose a folder, such as Documents/Clock.

**Updating:** Install the new APK over the existing one. Your alarms and recorded hours will be preserved.

## Your data

- Everything stays on your phone. The app has no internet permission, no account requirement, no ads, and no analytics.
- **Automatic backup:** Once a day, when you use the app, a backup is saved to your chosen folder. Only the 14 most recent backups are retained.
- **Export / Import** in Settings: Export everything to a single JSON file. Imports are merged, so importing the same file twice adds nothing.
- Uninstalling deletes the app's data. Keep automatic backups enabled, and occasionally copy a backup somewhere off your phone.

## Permissions

| Permission | Why |
|---|---|
| Notifications | Alarm and timer notifications, missed-alarm notices, and the running work timer |
| Alarms & reminders (exact alarms) | Ring at the exact minute, even in battery-saving mode |
| Full-screen notifications | Display the alarm over the lock screen |
| Live notifications | Display countdowns in the status bar and Samsung's Now Bar (Android 16+) |
| Run at startup | Restore alarms after a phone restart |
| Foreground service, wake lock, vibration | Keep the alarm ringing until you snooze or dismiss it |
| Ignore battery optimization (requested in Settings) | Prevent the phone from stopping alarms in the background |
| Do Not Disturb access (optional) | Allow alarms to ring through "total silence" when enabled |
| Network state | Added by Android's widget library; the app has no internet permission |

## Requirements

- Android 8.0 or newer. Tested on a Samsung Galaxy A55 (One UI 8, Android 16).

## Version history

| Version | Changes |
|---|---|
| 1.1.2 | First public release |

## Source Code & Disclaimer

Provided as is, without warranty.

The source code is private; this repository hosts the releases.

Well, I don't mind sharing the source code, but if you're anything like me, you just download scripts and programs you find on GitHub. I couldn't give a rat's ass how they work.
