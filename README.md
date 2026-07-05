# Steady (v3 — personalized)

A personal strength + nutrition tracker, built around your real training history. Runs entirely
in the browser, stores data on your own phone, installs to the home screen as an offline app.

## What's in this version

- **A/B/C session rotation** (full-body, posterior-chain biased, a knee primer every session).
  Ported from the program you were already running — the smart parts (tendon rehab, more pulling
  than pushing) kept, the exercise churn trimmed. Rotates A -> B -> C -> A, so a missed day never
  zeroes out a movement pattern for the week.
- **Your real logged weights carried in** as each lift's starting reference, so progression advice
  works from day one (hip thrust 135, trap-bar 95, leg press 120, etc.).
- **Restart mode.** Because you'd had ~2 weeks off, the app opens in a "Reboot" state and suggests
  ~85% of your old weights for the first session or two, then resumes normal progression.
- **Weight + reps logged per set**, plus time and weighted-hold (timewt) metrics for isometrics.
- **Progress tab** with the weight x waist verdict matrix, strength-volume chart from your logs,
  functional milestones, and body check-ins.
- **External exercise log** (swim / pickleball / cycle) that feeds your progress readout: counts
  toward a weekly cardio target, supports the fat-loss verdict, and flags knee-provoking activity.
- **Food tab**: protein hero, gentle added-sugar awareness, veg/water habit counters, label rules.
- **Backup**: Plan tab -> Export / Import (a .json file you own).

## Files (keep them together in the repo root)

- index.html — the app + your data
- sw.js — offline caching (cache name steady-v3)
- manifest.json — installable metadata
- icon-180.png, icon-192.png, icon-512.png — app icons
- README.md

## Put it on GitHub

1. Create a repo (e.g. steady), upload all files at the root.
2. Settings -> Pages -> Deploy from a branch -> main / (root) -> Save.
3. Wait ~1 min for the https://YOURNAME.github.io/steady/ URL.

## Install on iPhone

Open the URL in Safari -> Share -> Add to Home Screen. Launches full screen, works offline.

## Your data

- Saves automatically on your phone (localStorage). No account, no cloud.
- Back it up: Plan tab -> Export backup (do this now and then).
- Restore / move phones: Plan tab -> Import backup.
- Clearing Safari data or deleting the home-screen app erases local data — keep an export safe.

## A note on the seeded history

The first time the app loads, it drops your real bests in under the date 2026-06-19 as the
"last time" reference, then never seeds again. As you log new sessions, those become the reference
and the seed just fades into history. If you ever Import a backup, that replaces everything.

## Updating later

If you edit index.html, bump const CACHE = 'steady-v3' in sw.js to -v4 so your phone pulls the
new version instead of the cached one.

## The one thing worth starting

You logged bodyweight twice and waist never — so fat-loss trend is currently invisible. Add a
waist measurement on the Progress tab every week or two. Combined with weight, it's the single
most useful signal for whether you're losing fat, gaining muscle, or recomposing.
