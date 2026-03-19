# Roohi's Activity Tracker

A calm, mobile-first web app for logging a newborn's daily activities — feeding, poop, and pee.

No notifications. No accounts. No anxiety. Just a simple log.

---

## How to Access on iPhone

### Option A — Same WiFi (quick, no hosting needed)
1. On your computer, run:
   ```bash
   cd /path/to/Claude-Coding-Projects
   python3 -m http.server 8080
   ```
2. Find your computer's local IP:
   ```bash
   hostname -I
   ```
3. On iPhone (same WiFi), open Safari and go to:
   ```
   http://192.168.x.x:8080/roohi-tracker/
   ```
4. Tap **Share → Add to Home Screen** for an app icon.

### Option B — GitHub Pages (permanent link, works anywhere)
1. Go to your GitHub repo → **Settings → Pages**
2. Set source to your branch, root folder
3. Access at: `https://<your-username>.github.io/Claude-Coding-Projects/roohi-tracker/`

### Option C — iCloud / AirDrop
- Copy `index.html` to iCloud Drive, open in the Files app on iPhone, tap to open in Safari.

---

## Features

| Feature | Details |
|---------|---------|
| Log Activity | Date/time (auto-filled), feed type, poop color + size, pee size, notes |
| Today's Summary | Feeds / poops / pees count and last feed time at a glance |
| History View | Scrollable table, filterable by date |
| Delete Entries | Tap ✕ on any row |
| Export CSV | Downloads all data as a spreadsheet |

---

## Feed Types

| Option | When to use |
|--------|------------|
| Regular | Full normal feed |
| Snack | Short / small feed |
| Top-up | Small extra feed after a regular one |
| No feed | Logged poop/pee only |

---

## Log Format

| Date | Time | Feed | Poop | Pee |
|------|------|------|------|-----|
| Mar 17 | 11:00 AM | Regular | Yes · Black-green · Small | No |
| Mar 17 | 2:00 PM | Regular | No | Yes · Big |
| Mar 17 | 5:30 PM | Regular | Yes · Black-green · Small | Small |
| Mar 17 | 7:00 PM | Snack | Small · Black-green | Yes |
| Mar 18 | 1:55 AM | Regular | No | Yes |
| Mar 18 | 3:40 AM | Top-up | Yes | No |

---

## Tech

- **Pure HTML/CSS/JavaScript** — single file, no install, no build step
- **localStorage** — all data stays in the browser, nothing sent anywhere
- **Works offline** — once loaded, no internet needed

---

## Running Locally

```bash
# Open directly (no server needed):
open roohi-tracker/index.html

# Or serve via Python:
python3 -m http.server 8080
# Visit: http://localhost:8080/roohi-tracker/
```

---

## Data Backup

Use **Export CSV** in the app to download a spreadsheet of all entries at any time.
