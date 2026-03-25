# Screen AI

Ask Claude about your screen using vision AI.

## Deploy to Vercel

### Option A — Vercel Dashboard (easiest, no coding needed)

1. Create a free account at vercel.com
2. Go to vercel.com/new → "Import Git Repository"
3. Push this folder to a GitHub repo first, then import it
   - Or use the Vercel CLI below

### Option B — Vercel CLI

```bash
npm install -g vercel
cd screen-ai
vercel
```

Follow the prompts. When asked about settings, just press Enter for defaults.

### Set your API key (required)

After deploying:
1. Go to your project on vercel.com
2. Settings → Environment Variables
3. Add: ANTHROPIC_API_KEY = sk-ant-your-key-here
4. Redeploy (Deployments tab → ... → Redeploy)

Your site will be live at: https://your-project-name.vercel.app

## Project structure

```
screen-ai/
  api/
    ask.js          ← serverless function (proxies Anthropic API)
  public/
    index.html      ← frontend
  vercel.json       ← routing config
```

## How to use

1. Open your deployed URL
2. Click "Share screen" and pick a window or your whole screen
3. Click "Capture screenshot"
4. Ask a question and hit Send
