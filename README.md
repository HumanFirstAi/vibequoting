# Vibe Quoting — Landing Page

## Local development

```bash
npm install
npm start
```

Open http://localhost:3000

## Deploy to Railway

### Option A: GitHub (recommended)

1. Push this folder to a GitHub repo
2. Go to [railway.app](https://railway.app) → New Project → Deploy from GitHub repo
3. Railway auto-detects Node.js, runs `npm install` and `npm start`
4. Add a custom domain in Settings → Networking → Custom Domain

### Option B: Railway CLI

```bash
npm install -g @railway/cli
railway login
railway init
railway up
```

## Project structure

```
vibequoting-site/
├── public/
│   └── index.html    # Landing page
├── server.js         # Express server
├── package.json
├── .gitignore
└── README.md
```

## Environment

Railway auto-assigns `PORT`. No other env vars needed.

## Google Sheets signup

The signup form posts to a Google Apps Script endpoint. The deployment URL is hardcoded in `public/index.html`. To change it, search for `GOOGLE_SHEET_URL` in the HTML file.
