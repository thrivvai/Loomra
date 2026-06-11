# Loomra Chat

A private, static OpenRouter chat interface designed to deploy as a single-page Netlify site.

## What it does

- Runs entirely in the browser from `index.html`.
- Stores your OpenRouter API key and chat history in this browser's `localStorage` only.
- Calls OpenRouter's OpenAI-compatible chat completions endpoint directly.
- Lets you load currently-free OpenRouter models from the public models endpoint.
- Exports individual chats as JSON.

## Deploy to Netlify

1. Push this repository to GitHub.
2. Create a new Netlify site from the repository.
3. Use these settings:
   - Build command: leave blank
   - Publish directory: `.`
4. Open the deployed site, click **Settings**, paste your OpenRouter API key, and pick a model.

## Local preview

```bash
python3 -m http.server 8888
```

Then open <http://localhost:8888>.

## Security note

This is intentionally a personal static app. Because it calls OpenRouter from the browser, a key saved in settings is stored in local browser storage. Do not hard-code your API key in `index.html`, and do not use this pattern for a public multi-user application. If you want a public app, put OpenRouter behind a Netlify Function or another server-side proxy.
