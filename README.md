# BODY TRACK — Complete Starter Project

A responsive, bilingual (Arabic/English) wellbeing tracker with a dark interface.

## Included now
- Today dashboard: water, steps, sleep, mood, meal check-ins, movement log, personal note.
- Progress overview and weekly visual summary.
- Monthly calendar with check-in markers.
- Arabic RTL / English LTR interface.
- Local persistence in the browser (`localStorage`).
- JSON backup export and import.
- PWA manifest + service worker for installability and offline app-shell caching.
- Responsive layout for phone, tablet, and desktop.
- No calorie targets, fasting streaks, weight-loss rewards, or food restriction scoring.

## Run locally
This is a static web app. You can open `index.html` directly for basic use. For service-worker/PWA support, serve the folder over localhost:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy free (static hosting)
1. Create a GitHub repository and upload the contents of this folder.
2. In GitHub, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select `main` and `/ (root)`, then Save.
5. GitHub Pages will provide a public URL after deployment.

Other static hosts such as Cloudflare Pages or Netlify can also host these files.

## Important: what is not connected
This build does **not** include real user accounts, cloud database, multi-device sync, push notifications, or app-store binaries. Those require external services and credentials. No credentials are embedded in this package. A secure production implementation should use a backend such as Supabase (Auth + Postgres + Row Level Security), configure environment secrets on the hosting provider, and test privacy rules before storing personal data.

## Privacy
Current entries are stored only in the browser on the device used. Clearing browser site data may remove them. Use **Settings → Export backup** regularly. Import merges records by date; if two backups contain the same date, imported values replace that date's local record.

## Project files
- `index.html` — application structure
- `styles.css` — responsive dark theme and RTL support
- `app.js` — UI logic, local data model, backup/restore
- `manifest.webmanifest` — install metadata
- `sw.js` — offline app shell cache

## Safety by design
BODY TRACK is a habit and wellbeing companion, not a medical device. It intentionally avoids restrictive dieting mechanics and should not be used to support starvation or prolonged fasting. Seek qualified care for medical or eating-related concerns.
