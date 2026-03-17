# WeightLog — Personal Weight Tracker

A sleek, offline-capable weight tracking app. No backend required — all data is stored in your browser's localStorage.

## Features

- **Weight logging** with date and optional notes
- **Comparison stats** — vs yesterday, last week, last month
- **Progress chart** with 7-day moving average trendline + goal line
- **−2 lbs/month goal line** overlaid on chart
- **BMI calculator** built in (lbs/ft or kg/cm)
- **Goal tracking** with ETA calculator
- **Chart range filters** — 30d / 90d / 6mo / All
- **lbs ↔ kg toggle**
- **CSV export**
- **Full history table** with per-entry deletion

## Deploy to GitHub Pages

### Option 1 — New repo (quickest)

1. Go to https://github.com/new
2. Name it `weightlog` (or anything you like)
3. Make it **Public**
4. Click **Create repository**
5. Upload `index.html` via the web UI (drag & drop or "Add file")
6. Go to **Settings → Pages**
7. Source: `Deploy from a branch` → branch: `main` → folder: `/ (root)`
8. Click **Save** — your site will be live at:
   `https://<your-username>.github.io/weightlog/`

### Option 2 — GitHub CLI

```bash
git init
git add index.html README.md
git commit -m "Initial WeightLog deploy"
gh repo create weightlog --public --push --source=.
# Then enable Pages in repo Settings → Pages
```

### Option 3 — Git CLI

```bash
git init
git add index.html
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/weightlog.git
git push -u origin main
# Then enable Pages in repo Settings → Pages
```

## Data Privacy

All data is stored **locally in your browser** using `localStorage`. Nothing is sent to any server. To transfer data between devices, use the **Export CSV** button.

## Customizing the Goal Rate

The −2 lbs/month rate is fixed in the chart. To change it, open `index.html` and search for `rate =` in the `renderChart` function and update the value.
