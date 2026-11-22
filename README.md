# Clock

An offline Android alarm clock with a billable-hours work timer. Alarms that never miss, and a weekly hours text ready to paste into an invoice.

Part of Trip Point Software · by Trip Point Hardware
Android 8.0 or newer · Free · No internet access

## Why

Samsung Clock can't ring every other day, and no timer app gave me the weekly hours I bill. This one does both, and is built so an alarm never quietly fails.

## Features

### Alarms
- Repeat once, on chosen weekdays, or every N days (every other day, every 3 days…), with **Skip next**.
- Rings over the lock screen at alarm volume, even in silent mode. Volume starts quiet and rises over 20 seconds (60 with gentle wake).
- A big **Snooze** button; **Dismiss** needs a one-second hold, so it can't happen by accident.
- If nobody answers, it snoozes by itself as a backup ring, then leaves a "You missed your 6:30 alarm" notification.
- Per-alarm **Ring in Do Not Disturb**.
- Still rings after a phone restart, even before you unlock it (Samsung restarts phones overnight by default).
- Alarm history for the last 90 days: dismissed, unanswered or missed.

### Work timer (billable hours)
- Start, pause and resume; the session is saved the moment you tap Start, so it survives the app being closed or the phone restarting.
- Add, edit or delete entries for forgotten punches; one keywords line per day ("api refactor, client call").
- Today, this week, weekly target and what's left, with a progress bar.
- A weekly text for invoices, each day rounded to 0.25 h (or 0.1 h / 0.01 h), the total always adding up:
  ```
  Nov 2 - 6.5h [api refactor, client call]
  Nov 3 - 8h [testing, bug fixes]

  Total: 14.5h
  ```
- A reminder if the timer has been running too long.

### Also
- Countdown timer and stopwatch, shown live in the status bar and Samsung's Now Bar.
- Home screen widget, a Quick Settings tile for the work timer, and launcher shortcuts (long-press the icon).
- Four accent colors, light and dark mode.

## Install

1. Download `clock-<version>.apk` on your phone and tap it.
2. Allow **Install unknown apps** for your browser or file manager when asked. If Play Protect warns about an unknown developer, choose **Install anyway**.
3. Open Clock and allow notifications.
4. Settings (gear on the Alarms tab) → **Alarm reliability**: fix anything that isn't green, especially **Battery → Unrestricted**.
   On Samsung, also add Clock to **Never sleeping apps** (Settings → Battery → Background usage limits).
5. Settings → **Test alarm (rings in 10 s)**, then lock the phone. It should turn the screen on and ring.
6. Settings → **Automatic backup** → choose a folder such as Documents/Clock.

**Updating:** install the new APK over the old one. Your alarms and hours stay.

## Your data

- Everything stays on your phone. The app has no internet permission, no account, no ads and no analytics.
- **Automatic backup:** once a day you use the app, a backup is saved to the folder you chose; the newest 14 are kept.
- **Export / Import** in Settings: one JSON file. Import merges, so importing the same file twice adds nothing.
- Uninstalling deletes the app's data. Keep automatic backup on, and copy a backup off the phone now and then.

## Permissions

| Permission | Why |
|---|---|
| Notifications | The alarm and timer pages, missed-alarm notices, the running work timer |
| Alarms & reminders (exact alarms) | Ring at the exact minute, even in battery saving |
| Full-screen notifications | Show the alarm over the lock screen |
| Live notifications | Countdowns in the status bar and Now Bar (Android 16+) |
| Run at startup | Restore alarms after a restart |
| Foreground service, wake lock, vibration | Keep ringing until you snooze or dismiss |
| Ignore battery optimization (asked in Settings) | So the phone doesn't stop alarms in the background |
| Do Not Disturb access (optional) | Lets an alarm ring through "total silence" if you allow it |
| Network state | Added by Android's widget library; the app has no internet permission |

## Requirements

- Android 8.0 or newer. Tested on a Samsung Galaxy A55 (One UI 8, Android 16).

## Version history

| Version | Changes |
|---|---|
| 1.1.2 | First public release |


## License

Provided as is, without warranty.
Source code is private; this repository hosts the releases.
