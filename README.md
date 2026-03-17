# 🧘 Stretch Timer

A clean, minimal timer app for stretches and mobility routines — built as a Progressive Web App (PWA). Works offline, installable on your phone, no account needed.

Built with a Claude-inspired dark theme.

---

## Features

- **Flexible exercise config** — timed holds, rep-based, both sides, rest periods
- **Smart sequencing** — automatically cycles through sets, sides, and exercises
- **Live countdown ring** — animated circular timer with 3-second beep warning
- **Voice announcements** — says exercise name, side, and transitions out loud
- **Rep-based mode** — tap "Done" to advance manually, no timer needed
- **Pause / skip / back** — full playback controls during a session
- **Persistent storage** — routines saved in browser localStorage, survive refresh
- **PWA installable** — add to home screen on iOS or Android, works offline
- **Screen wake lock** — keeps screen on during your session

---

## Exercise types supported

| Type | Example | Config |
|---|---|---|
| Timed hold × sets | Curl-up, 10s × 5 sets | Duration + Reps |
| Timed hold × sets × sides | Side plank, 15s × 3 × each side | Duration + Reps + Both sides |
| Rep-based × sides | Bird dog, 6 reps each side | Reps + Rep-based + Both sides |
| Timed × rounds × sides | Hip flexor, 30s × 3 × each side | Duration + Reps + Both sides |

---

## File structure

```
stretch-timer/
├── index.html      # The entire app (HTML + CSS + JS, single file)
├── manifest.json   # PWA manifest (icons, theme, display mode)
└── README.md       # This file
```

---

## Setup on GitHub Pages (free hosting)

### Step 1 — Create a GitHub account
Go to [github.com](https://github.com) and sign up if you don't have an account.

### Step 2 — Create a new repository
1. Click the **+** icon (top right) → **New repository**
2. Name it `stretch-timer` (or anything you like)
3. Set visibility to **Public**
4. Leave everything else unchecked
5. Click **Create repository**

### Step 3 — Upload the files
1. On your new repo page, click **uploading an existing file** (or drag files into the page)
2. Upload all three files: `index.html`, `manifest.json`, `README.md`
3. Scroll down, click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to your repo → **Settings** tab
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Under **Branch**, choose `main` → folder `/root`
5. Click **Save**

### Step 5 — Get your URL
After 1–2 minutes, your app will be live at:
```
https://YOUR-USERNAME.github.io/stretch-timer/
```
GitHub will show the URL at the top of the Pages settings page.

---

## Install on your phone

### iPhone / iPad (Safari)
1. Open your GitHub Pages URL in **Safari**
2. Tap the **Share** button (box with arrow)
3. Scroll down → tap **Add to Home Screen**
4. Tap **Add**

### Android (Chrome)
1. Open your GitHub Pages URL in **Chrome**
2. Tap the **⋮ menu** (top right)
3. Tap **Add to Home Screen**
4. Tap **Add**

The app will appear on your home screen like a native app and works fully offline.

---

## Data & privacy

- All your routines are stored **locally in your browser** using `localStorage`
- Nothing is sent to any server
- Data is tied to the browser you use — to move routines to another device, use the export/import feature (if added)
- Clearing browser data for the site will erase your routines

---

## Tech stack

- Vanilla HTML / CSS / JavaScript — zero dependencies, zero frameworks
- Web Audio API — beep sounds
- Web Speech API — voice announcements
- Screen Wake Lock API — keeps screen on during sessions
- localStorage — routine persistence
- PWA manifest — installability + offline support
