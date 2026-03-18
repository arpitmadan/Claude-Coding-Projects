# CLAUDE.md

This file is read automatically by Claude at the start of every session. It provides full project context so AI assistants can work effectively without needing to re-explore the codebase each time.

---

## What This Repo Is

**Claude-Coding-Projects** is a personal monorepo containing small, focused tools built with Claude Code.

| Project | Path | Description |
|---------|------|-------------|
| Roohi Tracker | `roohi-tracker/` | Baby activity log (feeding, poop, pee) for newborn Roohi |

---

## Project: Roohi Tracker

### Purpose
A calm, mobile-first web app for logging a newborn's daily activities — feeding, poop, and pee — without anxiety-inducing notifications. Replaces Huckleberry for a simpler experience on iPhone.

### Tech Stack
- **Pure HTML/CSS/JavaScript** — single file, no build step, no dependencies
- **localStorage** — all data stored in the browser, no server needed
- **Mobile-first** — designed for iPhone, large tap targets, calm pastel colors

### How to Use / Run
```bash
# Just open in a browser — no server, no install:
open roohi-tracker/index.html

# Or serve locally if needed:
python3 -m http.server 8080
# then visit http://localhost:8080/roohi-tracker/
```

### File Structure
```
roohi-tracker/
└── index.html      # Entire app — HTML + CSS + JS in one file
```

### Features
- **Log Activity** — date/time (auto-filled), feed type, poop (color + size), pee (size), notes
- **Today's Summary** — feeds/poops/pees count and last feed time at a glance
- **History View** — scrollable table, filterable by date
- **Delete Entries** — tap ✕ on any row
- **Export CSV** — downloads all data as a spreadsheet

### Data Model
Each entry stored in `localStorage` under key `roohi-entries` as a JSON array:
```json
{
  "id": 1710000000000,
  "date": "2026-03-18",
  "time": "14:30",
  "feed": "Regular",        // "Regular" | "Snack" | "Top-up" | "No" | null
  "poop": true,             // true | false | null
  "poopColor": "Black-green", // "Black-green" | "Yellow" | "Brown" | "Green" | null
  "poopSize": "Small",      // "Small" | "Medium" | "Large" | null
  "pee": true,              // true | false | null
  "peeSize": "Big",         // "Small" | "Medium" | "Big" | null
  "notes": ""
}
```

### Design Decisions
- **No server/backend** — keeps it simple; data lives on-device
- **Single HTML file** — can be airdropped, shared, or bookmarked without any hosting
- **No notifications** — intentional; the previous app (Huckleberry) caused anxiety
- **Calm colors** — warm peach/coral palette, not clinical or high-contrast

### If Adding Features
- Keep the single-file approach unless complexity truly demands otherwise
- Do not add push notifications or reminders — explicitly not wanted
- If adding a backend/sync, prefer a simple approach (e.g. JSON file export/import)
- Test on mobile viewport (375px width) before desktop

---

## General Conventions (All Projects)

### Code Style
- Minimal — implement only what is asked
- No build tools unless the project genuinely needs them
- Prefer editing existing files over creating new ones
- Delete unused code rather than commenting it out

### Security
- Never commit API keys, tokens, or credentials
- Sanitize any user input before rendering as HTML (use `textContent`, not `innerHTML`, for user data)

### Git Workflow
```bash
# Always develop on the designated branch
git checkout claude/<description>-<session-id>

# Stage specific files (never `git add -A` blindly)
git add roohi-tracker/index.html

# Commit with clear message
git commit -m "Short description of what and why"

# Push
git push -u origin <branch-name>
```

### Commit Message Style
- Imperative mood: "Add feature" not "Added feature"
- First line ≤ 72 characters
- Describe the *why* when it isn't obvious from the *what*

---

## AI Assistant Guidelines

1. **Read files before editing** — never modify code you haven't read
2. **One file, one job** — the Roohi Tracker is intentionally a single HTML file; keep it that way unless there's a compelling reason
3. **Update this file** when new projects are added or significant changes are made to existing ones
4. **No speculative features** — only implement what is explicitly requested
5. **Confirm before destructive actions** — deleting entries, force-pushing, dropping data

---

## Getting Help

- Claude Code docs: type `/help` in the Claude Code CLI
- Report bugs: https://github.com/anthropics/claude-code/issues
